---
name: confirm-action
description: Checks that this turn contains the exact allow phrase before a write.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Action Confirmation](../../README.md)

# Checks that this turn contains the exact allow phrase before a write

No phrase, no write. The class is one of the six. The target is the one in the phrase.

Source: OWASP Top 10 for LLM Applications 2025, LLM06:2025 Excessive Agency. The gate is outside the model: the person's phrase, not a sentence the model adds.

## Before writing

1. Read [classes](references/classes.md). Compare the phrase in this turn with the write about to happen.

References: [classes](references/classes.md).

## Delivery

This skill writes no file. A write proceeds only when the person's message in this turn contains the exact phrase for that one target. Do not invent the phrase. Do not reuse a phrase from an earlier turn.

## Done

- [ ] Only the reference for this command was applied.
- [ ] The output folder, the subject subfolder, `ORIGIN.json`, and `STATUS.md` match the delivery rules.
- [ ] A missing required fact is a gap. The file stays `proposed`.

## Example

A request that names the piece and its source writes one file. A request missing that source writes nothing and names the gap.
