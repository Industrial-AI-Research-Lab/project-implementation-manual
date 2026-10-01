# Finding and Saving Scientific Papers — Student Guide

This guide takes you from a topic to a verified paper collection and a reading log that the supervisor can check. Start it in the first week of the project and repeat the search before you submit.

## Terms

| Term | Meaning | What it means for you |
|---|---|---|
| DOI, version of record | A DOI is the permanent identifier of a paper. The address `https://doi.org/<DOI>` opens the publisher's page with the version of record: the final published text. | Cite the DOI. The DOI page also shows corrections and retraction notices. |
| Preprint, accepted manuscript, published version | A preprint is the authors' text before peer review (arXiv). An accepted manuscript is the text after review, before the publisher's layout. The published version is the version of record. | Conclusions can change in review. Mark which version you hold and cite the one you read. |
| Seed paper, citation chaining | A seed paper is an important paper from the supervisor or the first strong hit. Backward chaining follows its reference list to older work; forward chaining follows "Cited by" to newer work. | The systematic form of "read the referenced papers too". |
| Search saturation | The point at which new queries and chaining return papers you already have. | The stop signal. There is no fixed number of papers. |
| SJR quartile, DOAJ | SJR ranks journals by citation data from Scopus; Q1 is the top quarter of journals in a subject category, free at scimagojr.com. DOAJ lists open-access journals that meet editorial and peer-review criteria. | Free journal checks without Scopus access. They say nothing about the quality of a single article. |
| Originality, borrowing | Measures from the thesis check in the Antiplagiat system: borrowing is text that matches other sources without correct quotation; originality is the rest. | A quotation in quotation marks with a reference counts as citation. Text copied into notes and then into the thesis counts as borrowing. Thresholds are set by the programme. |
| Reading log, synthesis matrix | One table with a row per paper read and fixed columns. | The checkable artifact of reading. Comparing rows shows agreements, contradictions, and gaps. |

## Search

Sources, in order of trust:

1. Seed papers from the supervisor.
2. Databases and search engines: Google Scholar; publisher sites available through ITMO (ScienceDirect, IEEE Xplore, and the others on the library's list); arXiv; Semantic Scholar. For Russian-language work: eLIBRARY.RU (citation index and full texts, personal registration) and CyberLeninka (open-access Russian journals).
3. LLM-based search: arXiv Xplorer (semantic search over arXiv), alphaXiv, Perplexity, Elicit. They propose candidates. Each candidate passes the check from the LLM assistants section before it enters the collection.

Build the query: write the research question as two to four concepts, list synonyms for each, join synonyms with OR and concepts with AND, put exact phrases in quotes, refine after the first results. In Google Scholar pin a known paper by its exact title in quotes, then use "Cited by" and "Related articles"; narrow the query instead of paging.

Chain from every seed paper: backward through its reference list, forward through "Cited by". Citation-graph tools such as Connected Papers, Litmaps, or ResearchRabbit show the neighbourhood of a seed; use them for exploration only, their ranking is opaque and changes.

Set a Google Scholar e-mail alert for the main query and a "cited by" alert for each seed; keep alerts narrow.

Stop when search saturation is reached: the same papers keep reappearing, chaining returns papers you already have, new terms add nothing.

Before a paper becomes evidence in your work, check where it was published: a peer-reviewed journal or conference, or a preprint, with a DOAJ listing or an SJR quartile as a free journal check, because Google Scholar also indexes unreviewed and predatory items and citation count measures visibility, not quality.

## Full text

Access through ITMO, as of September 2026: three routes lead to subscribed resources, My Loft (sign in with ITMO.ID and install the browser extension, no VPN needed), the campus network, and VPN. The current list of subscribed collections is at [lib.itmo.ru/resources](https://lib.itmo.ru/resources); it includes ScienceDirect, IEEE Xplore, Wiley, Springer Nature e-books, SPIE, and Optica, and it excludes Scopus and Web of Science. Foreign access comes through the national subscription decided per organisation, so the list changes yearly; re-check it at the start of each semester. Files downloaded through subscriptions are for scientific and educational use; do not pass them to third parties.

Ways to get the PDF:

- the DOI page while signed in through My Loft or on campus;
- the Unpaywall extension (a green tab appears when a legal free copy exists) and the "All versions" and [PDF] links in Google Scholar;
- a preprint or accepted manuscript on arXiv or the author's page;
- eLIBRARY.RU or CyberLeninka for Russian papers;
- an e-mail to the corresponding author with the DOI; publishers usually allow authors to send the paper to colleagues on request;
- Sci-Hub, a pirate resource: its mirrors move often, so search for a current address each time, and it lacks many recent papers.

Record which version you hold, preprint, accepted manuscript, or published, in the manager.

## Reference manager

Choose one reference manager and keep everything in it.

- **Mendeley**, the default choice: Mendeley Reference Manager (desktop and web library, cloud-first), Mendeley Web Importer (browser extension), Mendeley Cite (Word add-in, needs a Microsoft account). Sign in with a free Elsevier account; there is no ITMO login. Mendeley Desktop is legacy and receives security fixes only.
- **Zotero**, if you write in LibreOffice, Google Docs, or LaTeX: Zotero desktop with the Connector extension; plugins for Word, LibreOffice, and Google Docs; BibTeX export for LaTeX through the Better BibTeX plugin. The ITMO library recommends it as the simpler tool.

Tips for working with collections:

- one collection per project with sub-collections by theme keeps things findable;
- a status tag on each record (to-read, skimmed, read, cite) shows at a glance what is done;
- PDFs, highlights, and notes kept inside the manager save you from hunting through loose files;
- imported records usually deserve a quick check of authors, year, journal, volume, pages, and DOI against the article page;
- a shared group (Mendeley: up to 25 members; Zotero: a group library) lets the supervisor see the collection as it grows;
- an export to BibTeX or RIS is handy for LaTeX or hand-over, but it is not a backup, so keep the library synced.

Reference list in the thesis: both managers ship the GOST R 7.0.5-2008 style (in Mendeley Cite: Citation Settings → Change citation style → "GOST"). The generated list still needs a manual pass against your programme's thesis requirements.

## Reading and notes

Before opening a paper, write down in one line what you need from it: a method, a baseline, a dataset, an argument for relevance. That line sets how deep you read.

1. **Abstract triage.** Read the abstract of every saved paper and record the decision, keep or skip, with a one-line reason as a tag or note in the manager. Only "keep" items go to the reading list.
2. **Reading order for a kept paper.** Introduction: whether the problem matches yours and what the authors promise. Discussion and conclusions: what they conclude and which limitations they admit. Results, tables and figures first: whether the numbers support the promise. Methods: only if you will build on the work or reproduce it, then sketch the pipeline. Papers differ in structure; the order stays the same.
3. **Pace.** A hard paper takes several sittings. Keep a running list of unfamiliar terms and close it as you go. Take unclear points to peers or the supervisor.
4. **Per-paper note.** In the manager, attached to the paper's record: context in up to five sentences, method, results as facts with numbers without the authors' interpretation, your assessment, link to your question. Write in your own words. Put any verbatim fragment in quotation marks with the page: text copied into a note and then into the thesis counts as borrowing in the originality check.
5. **Reading log.** One table, one row per paper read, fixed columns. Comparing rows shows where authors agree, where they contradict each other, and what nobody has tested. This table is your synthesis matrix.

| Citation | Year | Paper's question | Method | Findings | Link to my work | My assessment |
|---|---|---|---|---|---|---|
| Author et al. | 2024 | … | … | … | … | … |

## LLM assistants

An LLM assistant helps to propose candidate papers, to summarise or question a paper after your own pass through the abstract and introduction, and to explain an unfamiliar term or method. Responsibility for errors stays with you, as the [general requirements](../../general/student.md#use-of-generative-ai) state.

| Risk | What to do |
|---|---|
| Invented or distorted references that mix real and fake elements | Open the DOI of every proposed reference and confirm that it resolves to that paper; a record counts as verified when you have the full text. Discard what you cannot find. |
| Wrong numbers, units, or claims in a summary | Re-read every number and claim you reuse in the original. |
| Agreement with the assumption built into your prompt; a weak study summarised as confidently as a strong one | Ask for evidence on the opposite side; judge the paper by its venue and methods, not by the summary. |
| Answers from the model's memory instead of your documents | Prefer tools that answer only from uploaded documents and cite the passage; instruct any tool to use only the provided sources. |

Prompt templates:

- Summary: "Using only the attached paper, summarise the problem, method, data, main quantitative results, and the limitations the authors admit. Quote the passage for each number."
- Questions: "Using only the attached paper, answer: what is the baseline, how was it compared, and what would break the method in my setting: <your setting>. Cite the section for each answer."
- Candidates: "List papers on <topic> from <year> onward with title, authors, venue, and DOI. Mark any item you are not certain exists."

## Minimum expected result

By the agreed checkpoint, show the supervisor:

1. The collection in the reference manager, as a shared group or an exported BibTeX or RIS file: every record opened by DOI or full text and tagged with a status.
2. The reading log: one row per paper read, with the fixed columns from the section above.

## Further reading

- [Literature searching explained: develop a search strategy](https://library.leeds.ac.uk/info/1404/literature_searching/14/literature_searching_explained/4), University of Leeds Library — concept lists, OR and AND, phrases.
- [When to stop searching](https://pressbooks.library.torontomu.ca/graduatereviews/chapter/when-to-stop-searching/), Toronto Metropolitan University Library — the saturation signals.
- [Zotero](https://lib.itmo.ru/tpost/ctjtofay21-zotero) and [Mendeley](https://lib.itmo.ru/tpost/mo22ghu5a1-mendeley), ITMO University Library — installation, plugins, the GOST style.
- [Как читать научные статьи: советы учёных](https://habr.com/ru/companies/spbifmo/articles/336672/), ITMO University on Habr — reading strategies and a note template.
- [Literature Review Matrix](https://www.sjsu.edu/writingcenter/docs/handouts/Literature%20Review%20Matrix.pdf), San José State University Writing Center — a synthesis matrix template.
- [AI hallucinated citations](https://guides.library.charlotte.edu/hallucinatedcitations), UNC Charlotte Atkins Library — how to verify a reference.
