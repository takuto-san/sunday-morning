# Sunday Morning

[日本語](README.md)

An AI-hosted weekly news program skill. Bring your own news and saved links, review the week by day, agree on discussion topics with the host, and exchange opinions. Finish by choosing your highlight of the week.

## Installation

Clone this repository, then copy the skill into the directory for your agent.

```bash
git clone https://github.com/takuto-san/sunday-morning.git
cd sunday-morning
```

**Codex** (available across projects):

```bash
mkdir -p ~/.agents/skills
cp -R skills/sunday-morning ~/.agents/skills/
```

**Claude Code** (available across projects):

```bash
mkdir -p ~/.claude/skills
cp -R skills/sunday-morning ~/.claude/skills/
```

For a single project, copy it into `.agents/skills/` or `.claude/skills/` inside that project instead. If a skill with the same name already exists, check it before replacing it. Start a new agent session to use the skill.

## Usage

After installation, start a new session:

- **Claude Code**: enter `/sunday-morning`. You can add the week or source material after the command.
- **Codex**: open `/skills` and select `sunday-morning`, or invoke it explicitly with `$sunday-morning`. Codex does not register `/sunday-morning` as a custom slash command.

Provide the week and your news or saved links. You can use separate lists for news and discussion. If they are missing, the host will ask for them when starting.

```text
Week: 2026-01-05 to 2026-01-11
News:
- 2026-01-05 (listed date) | Article title | https://example.com/news
Discussion topics:
- Date unknown | Saved post | https://example.com/post
```

Use any source, such as RSS output, bookmark exports, or link lists. If a date is available, specify whether it is the publication, save, or listing date. You can also change the program name, language, subject, and number of stories.

This skill provides the workflow; it does not include automatic news retrieval or scheduling. Available sources depend on your environment's tools and permissions. It does not post or publish automatically.
