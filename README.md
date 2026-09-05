# Agent Toolkit

A Toolkit for coding agents: shape reusable commands, skills, and plugins you can use across any agent.

Works with any coding agent that supports custom skills, slash commands, or plugins (for example: OpenCode, Claude Code, Cursor, Codex, Windsurf, Continue, Aider, and similar tools).

## Structure

```text
.
├── commands/   Custom slash commands
├── plugins/    Agent plugins
├── mcps/    Agent mcp
└── skills/     Reusable agent skills and references
```

## Clone

```bash
git clone https://github.com/ideapedyudi/agent-toolkit.git
cd agent-toolkit
```

Optional: pin to a specific folder name for your agent:

```bash
git clone https://github.com/ideapedyudi/agent-toolkit.git ~/.config/agent-toolkit
```

## Use with any coding agent

Point your agent to this repository (or copy the folders it supports):

| Folder | What it provides | Typical agent support |
|---|---|---|
| `skills/` | Workflow guides (`SKILL.md`) | Most agents with skill loading |
| `commands/` | Slash-command prompts | Agents with custom commands |
| `plugins/` | Runtime hooks / helpers | Agents with plugin systems |
| `mcps/` | External tools, resources, and integrations via MCP | Agents with MCP support |

### Option A: Link the whole repo

Use this when your agent can load external skill/command directories.

```bash
# example paths — adjust to your agent
ln -s "$(pwd)/skills" ~/.agents/skills/agent-toolkit
ln -s "$(pwd)/commands" ~/.agents/commands/agent-toolkit
```

### Option B: Copy only what you need

```bash
cp -R skills/* ~/.agents/skills/
cp -R commands/* ~/.agents/commands/
```

### Option C: Project-local install

From any project:

```bash
git clone https://github.com/ideapedyudi/agent-toolkit.git .agent-toolkit
```

Then configure your coding agent to read:

- `.agent-toolkit/skills`
- `.agent-toolkit/commands`
- `.agent-toolkit/plugins`
- `.agent-toolkit/mcps`

## Keep it updated

```bash
cd agent-toolkit
git pull
```

If you used copies instead of links, re-copy after pull.

## Notes

- Keep machine-specific secrets and local config outside this repository.
- Skills and commands here are meant to be shared and versioned.
- Plugin availability depends on your coding agent runtime.
