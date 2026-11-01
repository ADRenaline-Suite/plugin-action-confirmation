<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="README.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

# Action Confirmation (`plugin-action-confirmation`)

Lets one write through only when this turn contains the exact allow phrase for that target.

The instructions are in English. The file the plugin saves follows the language of the request. This plugin writes no file.

## /confirm-action

One class, one target, one write. The line is `allow-<class>: <target> — <what>`. A hint, a plan, or "when you can" is not the phrase.

## Help

## /confirm-help

The catalog of this plugin. It does not write a file.

## Who it is for

Someone who wants a human phrase before a database write, a push, a GitHub write, a deploy, or an infrastructure change. The security requirement stays with `plugin-security`. The write itself stays with the plugin that performs it. This plugin does not copy their skills.

## What it includes

Portable, for any agent that follows [Agent Skills](https://agentskills.io/specification):

- `confirm-action` checks the phrase before the write.

Cursor and Claude Code: the commands above. In Cursor, `/confirm-action`. In Claude Code, `/plugin-action-confirmation:confirm-action`.

Cursor only: rules `output-folder`, `phrase-this-turn`. Claude Code does not load rules. The same restrictions are in the skills.

## Install

In Cursor, install the plugin from this repository in Customize.

In Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-action-confirmation
claude plugin install plugin-action-confirmation@plugin-action-confirmation
```

To try a local copy, start Claude Code with `claude --plugin-dir <path to this repository>`.

## Example

A Postgres `UPDATE` waits until this turn contains `allow-db-update: <database> — <what>`. A `DELETE` uses `allow-db-delete`. There is no `postgres` class. A `SELECT`, a local edit, `git add`, and `git commit` are not gated.

## Configuration

This plugin writes no file and has no output folder. The classes are `db-update`, `db-delete`, `git-push`, `github-write`, `deploy`, and `infra`.

## License

MIT. Copyright (c) 2026 Ricardo Plascencia.

