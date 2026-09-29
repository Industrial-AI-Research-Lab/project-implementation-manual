# Meeting Records — Reference

An optional reference to the [task tracking guide](student.md): how to get a good meeting transcript, how to clean it before publishing, and which prompts turn it into a meeting record.

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| Transcript, time code | The text of a meeting line by line; a time code is the time of a line from the start of the recording. | A time code lets you check any decision against the recording. |
| Diarization | Labelling a transcript by speaker: who said which line. | Without it a model cannot tell a supervisor's decision from a student's suggestion. |
| WER (word error rate) | The share of words recognised wrongly; lower is better. | Compare tools by WER on Russian speech, not by the promises on their websites. |
| Sanitization, pseudonymisation | Sanitization removes from the text what must not be published. Pseudonymisation replaces names with roles using a mapping table. | Under 152-FZ, replacing names with roles while the mapping table exists counts as depersonalisation, not full anonymisation. |

## Meeting file

```markdown
# Meeting YYYY-MM-DD

Participants: student, supervisor
Recording: <link to the recording in Talk>

## Decisions
- <decision> (12:34)

## Actions
- [ ] <action> — <owner>, <due date>, #<issue number>

## Open questions
- <question>

Next meeting: YYYY-MM-DD
```

## Transcript

Talk's built-in transcript is usually enough. If you do not trust it or recorded the meeting with another tool, pick an option from the table.

| Tool | Where it runs | Speakers | What you need |
|---|---|---|---|
| Kontur.Talk (used at ITMO) | cloud, Russia | by participant name | a cloud recording; TXT with speakers and time codes: "Artefacts → Video recordings → download → Transcription" |
| faster-whisper with the Whisper large-v3 model | locally | no | a GPU with about 3 GB of memory in int8 mode, or a long run on the CPU |
| WhisperX | locally | yes, through pyannote | a Hugging Face token and agreement to the terms of use of the pyannote model |
| GigaAM-v3 | locally | no | for recordings longer than 25 seconds, access to the pyannote/segmentation-3.0 model |

- For Russian speech the developer of GigaAM-v3 reports an average WER of 8.4 % against 25.1 % for Whisper large-v3 on its own datasets. Independent comparisons show that which model is more accurate depends on the type of recording.
- Cloud APIs such as Yandex SpeechKit are cheap, about 36 RUB per hour of two-channel audio as of September 2026, but need a billing account.

Extract the audio from a video recording:

```bash
ffmpeg -i meeting.mp4 -vn -ar 16000 -ac 1 -c:a pcm_s16le meeting.wav
```

Transcribe with faster-whisper, with time codes:

```python
from faster_whisper import WhisperModel

model = WhisperModel("large-v3", device="cuda", compute_type="int8_float16")
segments, info = model.transcribe(
    "meeting.wav",
    language="ru",
    vad_filter=True,
    initial_prompt="MLflow, baseline, ablation, <terms and names of your project>",
)
with open("meeting.txt", "w") as f:
    for s in segments:
        f.write(f"[{int(s.start // 60):02d}:{int(s.start % 60):02d}] {s.text.strip()}\n")
```

Transcribe with speaker labels through WhisperX:

```bash
whisperx meeting.wav --model large-v3 --language ru --diarize --min_speakers 2 --max_speakers 2 --hf_token "$HF_TOKEN" --output_format srt
```

How to improve the transcript:

- Speak one at a time, into a headset or a microphone close to the mouth: models recognise and attribute overlapping speech worst of all.
- Set the language explicitly: `language="ru"`.
- Pass the names of the project's libraries, models and datasets to the model as a hint (`initial_prompt`): it will garble terms less often.
- Check names, numbers and terms against the recording by hand.

## Sanitization

Tell the participants that the meeting is recorded and that you will publish part of the record in the repository; if anyone objects, do not record. Then:

- Replace the names of everyone except the student and the supervisor with roles in square brackets: [partner's expert], [classmate]. Each person has one and the same label across all files.
- Generalise indirect identifiers: instead of a job title, an age or a company name, write general labels such as [bank employee] or [industrial partner].
- Remove entirely passwords, keys and tokens, internal addresses and links, partner data under NDA, grades, mentions of health and other personal topics, and off-topic talk.
- Keep the table that maps labels to names separately and never commit it.
- Automatic search helps but may miss part of the data: Natasha finds names, organisations and places, regular expressions find e-mails and phones, `gitleaks dir docs/meetings` finds keys and tokens. Reread the text yourself afterwards.
- Process an unsanitized transcript with a local model or with a service that stores data in Russia.

What the law says (for orientation). Under 152-FZ, personal data is any information that directly or indirectly points to a person. Publishing in an open repository counts as dissemination, and dissemination needs the person's separate consent. Since 1 July 2025, personal data of Russian citizens may not be recorded or stored at collection in databases outside the country, so keeping a full transcript on a foreign platform is risky. This is our reading, not legal advice.

## Prompts

Put the long text at the start of the request and the instructions after it. Ask the model to rely only on the transcript and to give a time code for every decision.

**Cleaning the transcript.**

```text
<transcript>…</transcript>
Fix recognition errors in the terms from this list: <project terms>. Do not change the meaning, do not shorten or add lines. Mark unclear passages as [unclear, MM:SS].
```

**Sanitization.**

```text
<transcript>…</transcript>
Replace the names of all participants except the student and the supervisor with roles in square brackets; each person has the same label everywhere. Remove passwords, keys, tokens, internal addresses, partner data, grades and personal topics. Return the cleaned text and, separately, a table "original name → label".
```

**Meeting record.**

```text
<transcript>…</transcript>
Use only this transcript, not your own knowledge.
1. Quote verbatim the lines where a decision was taken or an action was set, with the time code and the speaker's name.
2. From these quotes, fill in the meeting file template: decisions with time codes, actions with owner and due date, open questions.
If an owner or a due date is not named, write "not stated". If you are unsure whether something was a decision, mark it [check].
```

**Actions for the board.**

```text
<transcript>…</transcript>
List as JSON the actions agreed at the meeting, with the fields title, owner, deadline, timecode. Take only actions both sides agreed to.
```

Then ask the assistant to open each action from the list with `gh issue create --project`.

**Checking the record.**

```text
<transcript>…</transcript>
<summary>…</summary>
Compare the meeting record in <summary> with the transcript and find errors in it: omitted decisions, invented decisions, a wrongly named speaker, wrong numbers and dates. Give a time code for each error. Then fix only the errors you found.
```

If you doubt the result, run the check twice and compare the answers: differences show where the model invented something.

## Further reading

- [Получайте готовое резюме встречи](https://kontur.ru/talk/spravka/55135-poluchajte_gotovoe_rezyume_vstrechi), Kontur.Talk help — where to find the summary and what it contains.
- [faster-whisper](https://github.com/SYSTRAN/faster-whisper) — installation, int8 mode, speed.
- [WhisperX](https://github.com/m-bain/whisperX) — transcription with speaker labels.
- [GigaAM-v3](https://huggingface.co/ai-sage/GigaAM-v3) — a model for Russian speech and its WER.
- [Anonymisation](https://dmeg.cessda.eu/Data-Management-Expert-Guide/5.-Protect/Anonymisation), CESSDA — how to de-identify qualitative data.
- [What's Wrong? Refining Meeting Summaries with LLM Feedback](https://arxiv.org/abs/2407.11919), Kirstein et al., 2024 — checking and correcting a meeting summary in two steps.
