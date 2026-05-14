# Giving Your Desktop Hands - MCPs & Connectors
## Session 2 Student Guide | Building with The AI Sniper

**Instructor:** Cheryl Tibbs
**Series:** Building with The AI Sniper | AI Junkies University

---

## Quick Note on Session 1

The Session 1 recording didn't save (technology, am I right?). But every single thing we covered is in the course repo. The student guide, templates, and folder structure examples are all there. If you missed Session 1 or need a refresher, grab the materials here:

**https://github.com/tibby007/building-with-the-ai-sniper**

---

## What You'll Walk Away With

By the end of this session, you'll have at least one external tool connected to Claude Desktop, you'll understand the difference between extensions, plugins, and MCP servers, and you'll know how to find and connect more tools as your workflow grows. Claude won't just be smart anymore. It'll be able to actually DO things.

---

## The Big Idea

In Session 1, we gave Claude a **brain**: CLAUDE.md (instructions), skills (how to do tasks), and memory (persistent knowledge about you).

In Session 2, we're giving Claude **hands**: the ability to reach into your apps and services and actually take action.

| Session 1 (Brain) | Session 2 (Hands) |
|---|---|
| CLAUDE.md | Desktop Extensions |
| Skills | Plugins |
| Memory System | MCP Servers |
| Claude knows WHO you are | Claude can DO things in your apps |
| Writes a draft email | Actually sends the email |
| Plans a calendar event | Actually creates the event |
| Describes what to post | Actually posts to LinkedIn |

**Bottom line:** Brain + Hands = a digital employee who knows you AND can execute.

---

## Part 1: Understanding MCPs

### What Is MCP?

MCP stands for **Model Context Protocol**. Fancy name, simple concept.

It's the technology that lets Claude connect to external apps and services. Think of MCPs like USB ports on your computer. Your computer is powerful on its own, but USB ports let you plug in keyboards, mice, printers, and cameras. MCPs let you plug apps INTO Claude.

### What Becomes Possible

Without MCPs, Claude can only TALK about doing things. With MCPs, Claude can actually DO things:

| Without MCPs | With MCPs |
|---|---|
| "Here's a draft email you could send" | Claude sends the email through Gmail |
| "You should block off Tuesday at 2pm" | Claude creates the calendar event |
| "Here's a LinkedIn post you could use" | Claude posts it to your LinkedIn |
| "You might want to check your CRM" | Claude pulls up the contact record |
| "Here's a Slack message you could send" | Claude sends the message to your channel |

---

## Part 2: Three Ways to Connect Tools

There are three ways to give Claude access to your tools, from easiest to most advanced.

### Method 1: Desktop Extensions (Easiest)

**What:** Pre-built integrations you install with one click inside Claude Desktop.

**Best for:** Popular tools that have official support. This is where you start.

**How it works:**
1. Open Claude Desktop
2. Go to Settings (gear icon)
3. Click Extensions
4. Browse available extensions
5. Click Install on the one you want
6. Follow the authentication prompts (sign into your account)
7. Done. Claude can now use that tool.

**Popular extensions available:**

| Extension | What Claude Can Do With It |
|---|---|
| Google Calendar | Check your schedule, create events, find free time |
| Gmail | Read emails, draft replies, search your inbox |
| Slack | Read channels, send messages, search conversations |
| Notion | Read and create pages, search your workspace |
| Google Drive | Read and create files, search documents |

**Pro tip:** Start with Google Calendar. Everyone has one, and the results are immediately visible when you ask "What's on my calendar tomorrow?"

### Method 2: Plugins (Bundled Packages)

**What:** Plugins are bundles that can include MCP connections, skills, AND tools packaged together. Think of them as "app packs" for Claude.

**Best for:** When you want a complete solution, not just a connection.

**The difference:**
- An **extension** gives Claude access to LinkedIn
- A **plugin** gives Claude access to LinkedIn PLUS skills that know how to prospect, write posts, manage connections, and send messages

**How to find plugins:**
- Ask Claude: "Search for plugins for [your tool]"
- Browse the plugin directory
- Check the community resources in our course repo

**Example from Cheryl's setup:** She doesn't just have a LinkedIn connection. She has separate skills (Jorge for prospecting/connections, Betsy for content) that work WITH the LinkedIn connection. The connection plus the skill equals the magic.

### Method 3: Manual MCP Server Configuration (Most Advanced)

**What:** For tools that don't have a one-click extension or plugin yet, you can manually configure an MCP server.

**Best for:** Specialized tools, custom APIs, or cutting-edge integrations.

**What you need:**
- The MCP server package name or URL
- An API key from the service (usually)
- Basic comfort with settings configuration

**Where to configure:**
- Claude Desktop > Settings > Integrations
- Or through a `.mcp.json` file in your project (advanced)

**Don't stress about this one.** If your tool has an extension, use that. If not, plugins are the next step. Manual MCP configuration is for when you need something specific and you're ready for a little more setup. We'll touch on this more in future sessions.

### Quick Comparison

| Method | Ease of Setup | Flexibility | Best For |
|---|---|---|---|
| Desktop Extensions | One click | Uses what's available | Popular tools (Google, Slack, Notion) |
| Plugins | Install + configure | Connections + skills bundled | Complete workflows |
| Manual MCP Config | Technical setup | Maximum flexibility | Custom or specialized tools |

---

## Part 3: Step-by-Step - Connect Your First Tool

### Step 1: Choose Your First Extension

Open Claude Desktop and go to **Settings > Extensions**.

Browse what's available and pick ONE that fits your workflow:

- **Google Calendar** - Great first choice. Everyone has one.
- **Gmail** - If email is your lifeline.
- **Slack** - If you live in Slack.
- **Notion** - If you use Notion for project management.
- **Google Drive** - If you need Claude to access your documents.

**Rule:** Start with ONE. Get it working. Then add more. Don't try to connect everything at once.

### Step 2: Install the Extension

1. Click **Install** on your chosen extension
2. A browser window will open for authentication
3. Sign into your account (Google, Slack, etc.)
4. Grant the permissions Claude needs
5. Wait for confirmation that the connection is active
6. Close the settings and return to Claude

### Step 3: Test Your New Connection

Switch to **Cowork mode** and try one of these prompts:

**If you connected Google Calendar:**
```
What's on my calendar for the rest of this week?
```

**If you connected Gmail:**
```
Show me my most recent emails from today.
```

**If you connected Slack:**
```
What's the latest activity in my most active channel?
```

**If you connected Notion:**
```
What pages do I have in my Notion workspace?
```

**The moment Claude responds with REAL data from YOUR app is the moment it clicks.** Claude just reached outside the chat window and grabbed actual information from your tool. That's MCP in action.

### Step 4: Update Your CLAUDE.md

Go back to your CLAUDE.md file and add your new connection under the Connected Tools section:

```markdown
## Connected Tools
- Google Calendar (via Desktop Extension) - can check schedule, create events, find availability
```

This helps Claude know what tools are available without having to discover them each time. Keep this section updated as you add more connections.

### Step 5: Try a Real Task

Now let's use the connection for something practical, not just a test:

**Google Calendar examples:**
```
Block off 30 minutes tomorrow morning for deep work.
```
```
Do I have any conflicts next Tuesday afternoon?
```

**Gmail examples:**
```
Draft a reply to the most recent email from [name]. Keep it short and professional.
```

**Slack examples:**
```
Send a message in #general: "Team standup notes are posted. Check the thread."
```

**Important:** Claude will ask for your confirmation before taking actions like sending messages, creating events, or posting content. It won't just do things without your approval.

---

## Part 4: The MCP Ecosystem

The world of available connections is growing fast. Here's a snapshot of what's out there:

### Productivity & Communication
- Google Calendar, Gmail, Google Drive
- Slack
- Notion
- Microsoft 365 (Outlook, Teams, SharePoint)

### CRM & Sales
- GoHighLevel
- HubSpot
- Salesforce
- Apollo (prospecting)
- ZoomInfo (data enrichment)

### Social Media & Content
- LinkedIn
- Blotato (multi-platform scheduling)
- Canva (design)

### Development & Data
- GitHub
- Supabase (database)
- Vercel (deployment)
- Netlify (deployment)

### Creative & Media
- HeyGen (AI video)
- Gamma (presentations)

### Automation
- n8n (workflow automation)

**The question isn't IF your tool can connect. It's WHEN.** New MCP servers and extensions are being added regularly by both Anthropic and the community.

---

## Part 5: Security & Best Practices

Real talk about connecting Claude to your apps.

### API Keys Are Like Passwords
Some connections (especially manual MCP configs) require API keys. Treat these like passwords. Don't share them. Don't paste them in public documents or chat messages. Claude stores them securely, but you should still handle them with care.

### Start With Minimum Permissions
When authenticating a new connection, start with the minimum permissions Claude needs. If you only need Claude to READ your calendar, don't give it permission to DELETE events. You can always expand permissions later.

### Review Your Connections Regularly
Periodically check **Settings > Integrations** to see what Claude has access to. Remove connections you're not actively using. It's like reviewing who has keys to your office.

### Claude Asks Before Acting
This is important: Claude will always ask for your confirmation before taking significant actions. It won't send emails, post to social media, or delete anything without your explicit approval. There's a safety net built in.

### What Claude Can't Access
- Claude only uses your connections during active conversations
- It doesn't run in the background accessing your apps when you're not there
- Each Cowork session is independent. Claude uses what you've connected, but only when you're in the conversation

---

## Part 6: Putting It All Together

Here's where your project should stand after Sessions 1 and 2:

```
my-project/
|
|-- CLAUDE.md                    (Updated with connected tools)
|
|-- skills/
|   |-- email-drafter/
|       |-- SKILL.md             (Your first skill from Session 1)
|
|-- memory/
    |-- business-context.md      (Your business info from Session 1)
```

And your CLAUDE.md should now include something like:

```markdown
# My Project

## About Me
[Your info from Session 1]

## Preferences
[Your style preferences from Session 1]

## Connected Tools
- Google Calendar (via Desktop Extension) - schedule management, event creation
- [Any other tools you connected today]

## Reference Files
- For detailed business context, see memory/business-context.md
```

---

## Part 7: Quick Reference Card

### Where to Find Things

| What | Where |
|---|---|
| Desktop Extensions | Settings > Extensions |
| Integrations/MCP Config | Settings > Integrations |
| Plugin Directory | Ask Claude: "Search for plugins for [tool]" |
| Community MCP Servers | https://github.com/anthropics/claude-code |

### Commands to Test Your Connections

| Connection | Test Prompt |
|---|---|
| Google Calendar | "What's on my calendar this week?" |
| Gmail | "Show me my recent emails" |
| Slack | "What's the latest in #general?" |
| Notion | "Search my Notion for [topic]" |
| Google Drive | "Find files related to [topic] in my Drive" |

### Troubleshooting Quick Fixes

| Problem | Fix |
|---|---|
| Claude says it can't access a tool | Check Settings > Extensions/Integrations to confirm it's connected |
| Authentication failed | Try removing and re-installing the extension |
| Claude doesn't know about your connection | Update your CLAUDE.md with the connected tool |
| Getting permission errors | Check that you granted the right permissions during setup |
| Extension not showing up | Make sure you're on a paid Claude plan (Pro or higher) |

---

## Homework Before Session 3

1. **Connect at least ONE tool** via Desktop Extensions if you haven't already
2. **Test it** with real prompts in Cowork mode
3. **Update your CLAUDE.md** to reflect your connected tools
4. **Extra credit:** Connect a SECOND tool and try a prompt that uses BOTH (e.g., "Check my calendar for tomorrow and draft a Slack message to my team about what's coming up")
5. **Drop your results** in the Building with The AI Sniper room. Show us what you connected and what Claude did with it!

---

## Coming Up Next

Full series (check the repo for updates):

- **Session 01:** Setup and First Run - Claude Desktop, Cowork, and Code
- **Session 02 (TODAY):** MCP Servers and Connecting Your Tools
- **Session 03:** Building Custom Skills
- **Session 04:** Memory Systems and Context Management
- **Session 05:** Advanced Workflows and Automation
- **Session 06:** Putting It All Together - Your AI Command Center

---

## Resources

**Our Course Repo (the main one):**
- [Building with The AI Sniper](https://github.com/tibby007/building-with-the-ai-sniper)

**Official Anthropic Docs:**
- [Claude Desktop Download](https://claude.ai/download)
- [Desktop Extensions](https://www.anthropic.com/engineering/desktop-extensions)
- [MCP Setup Guide](https://docs.claude.com/en/docs/claude-code/mcp)
- [Claude Skills Documentation](https://docs.claude.com/en/docs/claude-code/skills)

**Community Resources:**
- [Claude Code GitHub (Anthropic's official repo)](https://github.com/anthropics/claude-code)
- [Official Plugins Directory](https://github.com/anthropics/claude-plugins-official)
- [Awesome Claude Code (community skills, hooks, plugins)](https://github.com/hesreallyhim/awesome-claude-code)
- [MCP Server Directory](https://github.com/modelcontextprotocol/servers)

---

*Built by The AI Sniper | AI Junkies University | Building with The AI Sniper Room*
*Questions? Drop them in the room. Cheryl's got you.*
