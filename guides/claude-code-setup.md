# Claude Code Setup Guide

How to install Claude Code, run basic commands, and understand when to use it instead of Desktop or Cowork.

## What Is Claude Code?

Claude Code is a command-line tool that lets you work with Claude directly from your terminal. If you've never used a terminal before, don't panic. We'll walk through it.

The key difference: Claude Code is built for developers and technical work. It can edit code files, run scripts, manage git repos, and handle complex multi-step tasks. If Desktop is texting, and Cowork is having Claude at a desk in your office, then Code is having Claude sitting at the developer's workstation.

## When to Use Claude Code vs. Desktop vs. Cowork

| Situation | Best Tool |
|-----------|-----------|
| Quick questions, brainstorming, writing | Claude Desktop |
| Working with files, creating documents, using skills | Cowork |
| Writing or editing code, managing repos, technical builds | Claude Code |
| Automating multi-step technical workflows | Claude Code |
| Building MCP servers or plugins | Claude Code |

You don't have to pick just one. Most power users bounce between all three depending on what they're doing.

## Requirements

- **Node.js** version 18 or later (Claude Code runs on Node)
- **A terminal** (Terminal on Mac, Command Prompt or PowerShell on Windows)
- **A Claude account** with API access or a Pro/Team plan

## Installation

### Step 1: Install Node.js (if you don't have it)

Check if you already have it:
```bash
node --version
```

If you see a version number (v18 or higher), you're good. If not:

- **Mac:** Go to [nodejs.org](https://nodejs.org) and download the LTS version. Or if you use Homebrew: `brew install node`
- **Windows:** Go to [nodejs.org](https://nodejs.org) and download the LTS installer. Run it.

### Step 2: Install Claude Code

Open your terminal and run:
```bash
npm install -g @anthropic-ai/claude-code
```

Wait for it to finish. That's it.

### Step 3: Verify Installation

```bash
claude --version
```

You should see a version number. If you see an error, try closing and reopening your terminal.

### Step 4: Authenticate

```bash
claude
```

The first time you run it, Claude Code will walk you through authentication. Follow the prompts to connect your Claude account.

## Basic Commands

Once installed, here's what you need to know:

**Start a session:**
```bash
claude
```
This opens an interactive session where you can chat with Claude directly in your terminal.

**Give Claude a task:**
```bash
claude "create a Python script that converts CSV files to JSON"
```
This runs a one-shot task. Claude does the work and exits.

**Work in a specific directory:**
```bash
cd /path/to/your/project
claude
```
Claude automatically sees all the files in your current directory.

## Key Concepts

**CLAUDE.md:** Just like in Cowork, Claude Code reads a CLAUDE.md file in your project directory. Same format, same purpose. If you already built one in Cowork, it works here too.

**Context awareness:** When you run Claude Code in a project folder, it can see your files, understand your project structure, and make edits directly.

**Git integration:** Claude Code works with git. It can create branches, make commits, and even open pull requests. We'll get deeper into this in later sessions.

## Tips for Non-Developers

If you're not a developer, here's the honest truth: you might not need Claude Code right away. Cowork handles most business tasks. But learning the basics gives you a foundation for when you want to:

- Build custom tools
- Create MCP servers
- Automate technical workflows
- Work with developers on your team (you'll understand what they're talking about)

Start with Desktop and Cowork. Come back to Code when you're ready to level up.

## Troubleshooting

**"command not found: claude"** - Node.js might not be installed, or the installation didn't add Claude to your PATH. Try closing and reopening your terminal. If that doesn't work, reinstall with `npm install -g @anthropic-ai/claude-code`.

**Authentication issues** - Make sure your Claude account is active and you have API access enabled.

**Permission errors on Mac** - Try running the install with sudo: `sudo npm install -g @anthropic-ai/claude-code`

## Next Steps

If you're ready to connect Claude to external tools, check out the [MCP Server Basics](mcp-server-basics.md) guide.
