# Lindo AI Agent Skill

An [Agent Skill](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) for [Lindo AI](https://lindo.ai) — the AI website builder for agencies.

This skill teaches AI agents how to create websites, pages, and blog posts using the Lindo platform. It works with Claude Code, Codex, Cursor, and any tool that supports the Agent Skills standard.

## Install

```bash
npx skills add lindoai/agent-skill
```

Works with Claude Code, Codex, OpenCode, Cursor, Windsurf, and any agent that supports the skills standard.

### Manual

Copy the `SKILL.md` file to your project's skills directory:

```bash
mkdir -p .claude/skills/lindo-ai
curl -o .claude/skills/lindo-ai/SKILL.md https://raw.githubusercontent.com/lindoai/agent-skill/main/SKILL.md
```

## Prerequisites

This skill requires the Lindo MCP server to be configured:

```bash
npx -y @lindoai/mcp-server
```

The MCP server provides 43 tools for managing websites, pages, blogs, clients, and credits.

## What it does

- Creates websites from text prompts using AI
- Creates and publishes pages and blog posts
- Manages clients, assigns websites, generates login links
- Checks and allocates credits
- Views workspace and website analytics

## Links

- [Lindo AI](https://lindo.ai)
- [MCP Server](https://github.com/lindoai/mcp-server)
- [API Documentation](https://api.lindo.ai/v1/docs)
- [npm: @lindoai/mcp-server](https://www.npmjs.com/package/@lindoai/mcp-server)
