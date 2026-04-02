# manyfaced

> A catalog of agent skills where every step is run by a specialized face.

Manyfaced skills are agent skills (Claude Code, OpenClaw) where the generic AI
voice has been replaced with faces — cognitive primitives that change how an LLM
composes language. Each step that requires judgment is routed to a face or team
of faces. Mechanical steps stay faceless.

Every skill includes a **circuit diagram** showing the routing logic at a glance:
rectangles are faceless plumbing, rounded boxes are solo faces, hexagons are
teams. The diagram is the architecture.

## Browse the catalog

| Skill | What it does | Circuit |
|-------|-------------|---------|
| *your skill here* | — | — |

## Install a manyfaced skill

Each skill is a directory with a `SKILL.md`, FACE.md recipes, and TEAM.md files.

```bash
# Clone the catalog
git clone --depth 1 https://github.com/facessh/manyfaced.git ~/.manyfaced

# Copy a skill to your skills directory
cp -r ~/.manyfaced/<skill-name> ~/.claude/skills/<skill-name>
```

Before using a manyfaced skill, compile its faces. Each skill has a Setup
section listing which faces need compilation and where the recipes are.

## Requirements

- [faces-skill](https://github.com/facessh/faces-skill) — the `/faces`, `/face`,
  `/faceteam`, and `/manyface` slash commands
- [faces CLI](https://www.npmjs.com/package/faces-cli) — `npm install -g faces-cli`
- A [faces.sh](https://faces.sh) account (Free or Connect plan)

## Contributing

Built a manyfaced skill? Submit a PR.

### Directory structure

```
manyfaced-<skillname>/
  SKILL.md              # the skill — must include a circuit diagram
  recipes/              # FACE.md and TEAM.md files
    <alias>-FACE.md
    <team-name>-TEAM.md
  README.md             # what the skill does, who it's for, example usage
```

### Requirements for submission

- [ ] Directory named `manyfaced-<skillname>`
- [ ] `SKILL.md` with YAML frontmatter (`name`, `description`)
- [ ] Circuit diagram in mermaid after the Setup section — uses standard
      notation: `[faceless]`, `([solo face])`, `{{team}}`
- [ ] Setup table listing all faces and teams with recipe paths
- [ ] All FACE.md recipes included in `recipes/` with queued sources
- [ ] All TEAM.md files included in `recipes/` with mermaid protocol diagrams
- [ ] `README.md` explaining the skill, who it's for, and example output
- [ ] No compiled face data — only recipes. Users compile locally.
- [ ] No API keys, tokens, or credentials in any file

### How to create a manyfaced skill

Use the `/manyface` slash command from [faces-skill](https://github.com/facessh/faces-skill).
It walks you through decomposing a skill into roles, casting faces, and
producing the output directory.

---

[faces.sh](https://faces.sh) · [faces-skill](https://github.com/facessh/faces-skill) · [docs](https://docs.faces.sh)
