# Commit Messages — Student Guide

Optional. A good message makes the history readable for the supervisor now and for you in three months. Nothing here is checked at the defence.

## Seven rules

1. Separate the subject from the body with a blank line.
2. Keep the subject to about 50 characters.
3. Capitalize the subject.
4. No period at the end of the subject.
5. Imperative mood: the subject completes the sentence "If applied, this commit will ...".
6. Wrap the body at 72 characters.
7. The body explains what and why; the diff shows how.

## Types

An optional prefix from Conventional Commits, matching the branch types: `feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `chore:`; a `!` after the type marks a breaking change. With squash and merge the PR title becomes the commit on `main`, so the title follows the same rules.

## Examples

```
feat: add contrastive loss for the retrieval baseline

Replaces the triplet loss chosen in ADR-0003. The metric on the dev
split rises from 0.61 to 0.68 (MLflow run 4f2c...). Batch size stays 64.
```

Messages that say nothing: `fix`, `finally works`, `changes`, `WIP`.

## Further reading

- [How to Write a Git Commit Message](https://cbea.ms/git-commit/), Chris Beams — the seven rules with reasons.
- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) — the type prefixes.
- [Version Control with Git: Tracking Changes](https://swcarpentry.github.io/git-novice/04-changes.html), Software Carpentry — staging in logical portions.
