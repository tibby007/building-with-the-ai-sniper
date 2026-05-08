# MCP Server Basics

What MCP servers are, why they matter, and how to connect them to Claude.

## What Is MCP?

MCP stands for **Model Context Protocol**. That sounds technical, but the concept is simple: MCP is how Claude connects to outside tools and services.

Without MCP, Claude is smart but isolated. It can only work with what you paste into the conversation. With MCP, Claude can reach out and actually use your tools: your CRM, your email, your calendar, your file storage, your databases, whatever you connect.

Think of MCP servers like USB cables for Claude. Each one plugs Claude into a different tool.

## How It Works

Here's the flow:

1. **You install an MCP server** (a small program that knows how to talk to a specific tool)
2. **You configure Claude** to connect to that server
3. **Claude can now use that tool** as part of your conversations and workflows

For example, if you connect the Google Calendar MCP server, Claude can check your calendar, create events, and find open time slots. Without it, Claude would just be guessing about your schedule.

## Common MCP Servers

Some of the most useful MCP servers you'll encounter:

| Server | What It Does |
|--------|-------------|
| Google Calendar | Read/create/update calendar events |
| Gmail | Search emails, draft messages |
| Slack | Read/send messages, search channels |
| Google Drive | Read and create documents |
| Notion | Access your Notion databases and pages |
| GoHighLevel | Manage contacts, pipelines, workflows |
| GitHub | Manage repos, issues, code |
| File System | Give Claude access to specific folders |

There are hundreds more, and new ones launch regularly.

## Where MCP Servers Come From

Three main sources:

1. **Official MCP Registry** - Anthropic maintains a registry of verified MCP servers. In Cowork, you can ask Claude to search for them.
2. **Community-built** - Developers build and share MCP servers on GitHub. Quality varies.
3. **Custom-built** - You (or your developer) can build MCP servers for your specific tools. We cover this in later sessions.

## How to Connect an MCP Server

### In Cowork (Easiest)

Cowork handles a lot of the MCP setup for you through plugins. When you install a plugin, it often includes the MCP connections you need.

Ask Claude: "Search for MCP servers related to [tool name]" or "What plugins connect to [tool name]?"

### In Claude Desktop (Manual)

You'll edit your configuration file:

**Mac:** `~/Library/Application Support/Claude/claude_desktop_config.json`
**Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

The file looks something like this:

```json
{
  "mcpServers": {
    "server-name": {
      "command": "npx",
      "args": ["-y", "@some-package/mcp-server"],
      "env": {
        "API_KEY": "your-api-key-here"
      }
    }
  }
}
```

Each server needs:
- A **name** (you pick this)
- A **command** to start the server
- **Arguments** (usually the package name)
- **Environment variables** (API keys, tokens, etc.)

After editing the file, restart Claude Desktop for changes to take effect.

### In Claude Code

Claude Code can also use MCP servers. The configuration is similar but lives in a different location. We'll cover the specifics when we dig into Claude Code in later sessions.

## Security Considerations

MCP servers have access to your tools, so be thoughtful about what you connect:

- **Only install servers from trusted sources.** The official registry is safest.
- **Use API keys with limited permissions.** Don't give a server admin access when read-only works.
- **Review what each server can do** before connecting it. Check the documentation.
- **Keep servers updated.** Like any software, updates fix bugs and security issues.

## Testing a Connection

After connecting a server, verify it's working:

1. Start a new conversation with Claude
2. Ask Claude about the tool you just connected (e.g., "Can you check my Google Calendar for tomorrow's events?")
3. If Claude can access the tool, you're set. If not, check your configuration.

## Troubleshooting

**"I connected the server but Claude can't use it"** - Restart Claude Desktop after editing the config file. Double-check your API keys.

**"The server keeps crashing"** - Check if you have the right version of Node.js installed. Some servers require specific versions.

**"I don't know where to get an API key"** - Each tool has its own process. Usually you'll find it in Settings > API or Developer section of the tool's website.

## Next Steps

Once you've connected your first MCP server, check out the [Skills Explained](skills-explained.md) guide to learn how to build automated workflows on top of your connections.
