# Claude Desktop Setup Guide

A step-by-step walkthrough for installing and configuring Claude Desktop on your computer.

## What Is Claude Desktop?

Claude Desktop is the standalone app version of Claude. Instead of using claude.ai in your browser, you get a dedicated app on your Mac or Windows machine. The big advantage? It can connect to tools on your computer and work with your local files. The browser version can't do that.

## Requirements

- **Mac:** macOS 12 (Monterey) or later
- **Windows:** Windows 10 or later
- **Account:** A Claude account (free works, but Pro or Team unlocks the features we use in this course)
- **Internet:** Required for Claude to function (it's not running locally)

## Installation

### Mac

1. Go to [claude.ai/download](https://claude.ai/download)
2. Click **Download for Mac**
3. Open the downloaded `.dmg` file
4. Drag Claude to your Applications folder
5. Open Claude from Applications
6. Sign in with your Claude account

### Windows

1. Go to [claude.ai/download](https://claude.ai/download)
2. Click **Download for Windows**
3. Run the installer
4. Follow the prompts
5. Open Claude from your Start menu
6. Sign in with your Claude account

## First Run Configuration

When you first open Claude Desktop:

1. **Sign in** with your Anthropic account credentials
2. **Choose your model** - Select Claude Sonnet for everyday tasks, Claude Opus for complex work
3. **Allow permissions** when prompted (Claude may ask for file access)

## The Configuration File

Claude Desktop uses a configuration file to know which MCP servers (tools) to connect to. This is where the real power comes from.

**Where to find it:**

- **Mac:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

To open this file on a Mac:
1. Open Finder
2. Press `Cmd + Shift + G`
3. Paste: `~/Library/Application Support/Claude/`
4. Open `claude_desktop_config.json` in any text editor

Don't worry about editing this file right now. We'll walk through it when we cover MCP servers in a later session.

## Tips for Getting Started

- **Be specific in your prompts.** "Help me write an email" is okay. "Help me write a follow-up email to a prospect who requested equipment financing info but hasn't responded in 5 days" is way better.
- **Tell Claude about yourself.** The more context you give, the better the output. Don't make Claude guess.
- **Use the conversation.** Claude remembers everything within a single conversation. Build on previous messages instead of starting over.
- **Start new chats for new topics.** Don't try to do everything in one conversation. Context from unrelated tasks can confuse things.

## Troubleshooting

**Claude won't open:** Make sure you're running a supported OS version. Try restarting your computer.

**Can't sign in:** Check your internet connection. Try signing in at claude.ai first to verify your credentials work.

**Responses seem limited:** Check if you're on the free plan. Pro and Team plans give you significantly more usage and access to more powerful models.

**App feels slow:** Claude processes in the cloud, so a slow connection means slow responses. Try switching to a stronger internet connection.

## Next Steps

Once Claude Desktop is running, move on to the [Cowork Setup Guide](claude-cowork-setup.md) to unlock the real power of working with Claude on your actual files and projects.
