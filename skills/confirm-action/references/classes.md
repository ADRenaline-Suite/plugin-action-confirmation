# Allow phrase

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="classes.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Action Confirmation](../../../README.md)

A model writes to a database or a remote because the task implied it.

## Steps

1. Find the phrase in the person's message this turn. If it is absent, do not call the tool. Say which class is required.
2. The class matches the effect. Update versus delete follows the SQL verb, not the product name of the database.
3. The target in the phrase is the target of the call. A different database, branch, or environment is a different phrase.
4. Do not write a file to record the approval.

## Rules

1. Do not invent the phrase. Do not accept a phrase from a previous turn.
2. A hint is not the phrase. "Push it", "when you can", "we should migrate", a plan, or an analysis does not authorize the write. The line has to be `allow-<class>: <target> — <what>`.

## Template

## Class

## Target

## What

## Phrase found

## Done

- [ ] The phrase was in this turn, or the tool was not called.
- [ ] The class matches the effect and the target matches the call.
- [ ] No file was written.

Close by saying whether the write proceeded, and the class that was required when it did not.
