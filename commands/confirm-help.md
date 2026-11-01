---
name: confirm-help
description: "ADRenaline. Help: catalog of plugin-action-confirmation (skills, rules, commands)."
---

# Help — ADRenaline Action Confirmation

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline Action Confirmation**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/README.md) — Lets one write through only when this turn contains the exact phrase for that target.

## Commands

- [**/confirm-help**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**confirm-action**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/skills/confirm-action/SKILL.md) — Checks that this turn contains the exact allow phrase before a write.
- [**/confirm-action**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/skills/confirm-action/references/classes.md) — Allow phrase: one class, one target, one write, typed by the person this turn.

## Skills

- [**confirm-action**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/skills/confirm-action/SKILL.md) — Checks that this turn contains the exact allow phrase before a write.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/rules/output-folder.mdc) — This plugin writes no project file.
- [**phrase-this-turn**](https://github.com/ADRenaline-Suite/plugin-action-confirmation/blob/main/rules/phrase-this-turn.mdc) — One phrase, one write, this turn. A read and a local edit are not gated.

## Output

- Repository: [**ADRenaline Action Confirmation**](https://github.com/ADRenaline-Suite/plugin-action-confirmation).
- This plugin writes no project file. The phrase is checked in the turn.

## Not in this plugin

- Security requirement → ADRenaline plugin-security.
- The write itself → ADRenaline plugin-backend.
