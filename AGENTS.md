# Repository Instructions

## Status and Purpose

This repository is a working collection of materials, requirements, recommendations, templates, and methodological guidance for student projects. It is not currently an official instruction or regulatory document. Formal decisions must be checked against the current rules of the responsible academic program and confirmed with the appropriate supervisor or coordinator.

The current iteration contains NIR project descriptions, requirements, assessment guidance, and LLM-assistant context under `nir-requirements/`, and a research-methodology template set under `research-templates/`.

## Repository Structure

- `README.md` — English repository entry point.
- `README.ru.md` — Russian repository entry point.
- `nir-requirements/general/` — requirements shared by all project types.
- `nir-requirements/assessment/` — grading principles, rubrics, matrices, and defense checklists.
- `nir-requirements/project-types/` — student and supervisor guidance for scientific, technological, industrial, and collaborative projects.
- `nir-requirements/llm-assistant/` — reusable context for an LLM assisting with NIR projects.
- `research-templates/` — research templates for planning, conducting, documenting, and reviewing a study, with a glossary at the end of each page.
- `research-templates/agent-guide.md` — instructions for an LLM agent on how to use the research templates when helping a researcher. Read it before using or editing the templates; the Russian edition is `research-templates/agent-guide.ru.md`.
- Future materials may add top-level sections for recommendations, templates, and methodological manuals. Do not create empty placeholder sections unless the user requests them.

## Naming Conventions

- Use lowercase English kebab-case for directories and descriptive filenames.
- Do not add numeric ordering IDs to filenames.
- Do not repeat a parent directory's meaning in a filename. Prefer `scientific/student.md` over `scientific/scientific-project-student.md`.
- English content uses `<name>.md`; the Russian counterpart uses `<name>.ru.md` in the same directory.
- `README.md` is English and `README.ru.md` is Russian.
- `AGENTS.md` is intentionally English-only.

## Bilingual Content SOP

1. Treat every English/Russian content pair as one logical document.
2. When changing either language, update its counterpart in the same working change so both editions remain semantically equivalent.
3. Preserve heading hierarchy, lists, tables, examples, links, grading labels, and normative strength across the pair.
4. Prefer natural phrasing over literal translation, but do not summarize, weaken, expand, or silently reinterpret requirements.
5. A one-language-only change is permitted only after the user explicitly agrees to that exception. Record the exception in the task report or change description.
6. Infrastructure files, `LICENSE`, and this English-only `AGENTS.md` are not bilingual content documents.

## README and Navigation SOP

1. Every directory under `nir-requirements/` and `research-templates/` must contain `README.md` and `README.ru.md`.
2. Each README briefly summarizes its section and links every immediate child document or subsection.
3. English README files link only to English content and English child README files. Russian README files link only to Russian content and Russian child README files.
4. The root README pair links to each other as the language switch.
5. When adding, moving, renaming, or removing content, update both affected README editions in the same change.
6. Use relative links and verify that every target exists.

## Content and Terminology SOP

- Treat the two Google Docs linked from `nir-requirements/README.md` and `nir-requirements/README.ru.md` as the primary sources of truth for student-facing and committee-facing requirements. When repository content conflicts with either source, update both Markdown language editions to match the relevant source.
- Keep local DOCX copies of the primary sources untracked. Publish links to the Google Docs, not copied DOCX files.
- Preserve substantive academic and organizational information during editing or migration.
- Do not present these materials as formally approved, binding, or current official policy.
- Use `LLM` or `LLM assistant` for product-neutral assistant guidance. Do not introduce a vendor-specific assistant name unless the user explicitly requests product-specific instructions.
- Do not restore attribution to the removed dated source. State retained requirements directly and neutrally.
- Keep the established project-type terms consistent across the repository: scientific, technological, industrial, and collaborative project.

## Research Templates SOP

- Link template pages to each other with relative links to the matching language edition.
- When a page gains a non-obvious term, abbreviation, or framework name, add its explanation to the `Glossary` section of both language editions, using the same wording as other pages that define the term.
- Follow [research-templates/agent-guide.md](research-templates/agent-guide.md) when using the templates to help a researcher.

## Git and Change-Control SOP

- Never create a Git commit unless the user explicitly approves committing the current changes.
- Permission to edit, migrate, translate, verify, or finish a task is not permission to commit.
- Before any approved commit, show or summarize the intended commit scope and exclude unrelated user files.
- Never modify, stage, delete, or reformat unrelated files.
- Keep local IDE and agent state ignored through `.gitignore`.

## Verification Checklist

Before reporting a content change as complete:

1. Confirm every content file has its language counterpart.
2. Confirm every `nir-requirements/` and `research-templates/` directory has both README editions.
3. Resolve all relative Markdown links.
4. Confirm English indexes do not link to Russian content and Russian indexes do not link to English content.
5. Compare the structure and meaning of every modified language pair.
6. Scan for obsolete vendor-specific assistant wording and attribution to the removed dated source.
7. Run `git diff --check`.
8. Run `git status --short`, confirm nothing is staged, and do not commit without explicit user approval.
