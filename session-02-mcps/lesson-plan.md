# AIJU Session 2: Giving Your Desktop Hands - MCPs & Connectors
## Lesson Plan | Building with The AI Sniper

**Instructor:** Cheryl Tibbs, The AI Sniper
**Series:** Building with The AI Sniper | AI Junkies University
**Session:** 2 of 6 | MCP Servers and Connecting Your Tools

---

## Pre-Session Checklist

- [ ] Claude Desktop app open and visible for screen share
- [ ] Student Guide link ready to drop in chat
- [ ] AIJU room open for questions
- [ ] Have at least 2-3 MCP connections visible in your Settings for demo
- [ ] Course repo ready: https://github.com/tibby007/building-with-the-ai-sniper
- [ ] Note for students: Session 1 recording did not save. The student guide and repo materials cover everything from Session 1. Direct students to the repo.

---

## Session Flow (Estimated 60-75 minutes)

### OPENING (7 min)

**Talking Points:**

- Welcome back. Quick housekeeping: the Session 1 recording didn't save. I know, I know. BUT the student guide and all the materials are in the course repo. Everything you need from Session 1 is there. If you missed it or want to review, grab it from the repo.
- Drop the repo link again: https://github.com/tibby007/building-with-the-ai-sniper
- Quick recap of Session 1 (since the recording didn't save, spend an extra minute here):
  - We set up our project folder structure
    - Created our CLAUDE.md (project instructions file)
      - Built our first skill (email drafter)
        - Set up our memory system
          - Cloned the course repo
          - "Last session we gave Claude a brain. Today we're giving it HANDS."
          - The big idea: Right now, Claude can think and write. After today, Claude can actually DO things in your apps. Send emails. Check your calendar. Post to LinkedIn. Update your CRM. That's what MCPs and connectors do.

          ---

          ### SECTION 1: The "Hands" Concept (8 min)

          **Key Metaphor to Drive Home:**

          Session 1 = Brain (CLAUDE.md, skills, memory). Session 2 = Hands (MCPs, connectors, extensions).

          **Talking Points:**

          - Think about it this way: after Session 1, Claude knows who you are, how you like things done, and has skills to do specific tasks. But it's still stuck inside the chat window. It can WRITE an email draft, but it can't SEND it. It can PLAN a calendar event, but it can't CREATE one.
          - MCPs are what give Claude access to the outside world. They're the bridge between "Claude wrote something nice" and "Claude actually did the thing."
          - MCP stands for Model Context Protocol. Don't let the name scare you. All it means is: a standardized way for Claude to talk to your apps and services.
          - Think of MCPs like USB ports on your computer. Your computer is powerful on its own, but USB ports let you plug in a keyboard, a mouse, a printer, a camera. MCPs let you plug apps INTO Claude.

          **What becomes possible with MCPs:**

          - "Send a Slack message to the team" (Claude actually sends it)
          - "What's on my calendar tomorrow?" (Claude actually checks)
          - "Create a contact in my CRM for this new lead" (Claude actually creates it)
          - "Post this to LinkedIn" (Claude actually posts it)
          - "Draft a reply to that email from Sarah" (Claude actually pulls up the email and drafts in Gmail)

          ---

          ### SECTION 2: Three Ways to Connect Tools (15 min)

          **Transition:** "Now there are three ways to give Claude these hands. Let's break them down from easiest to most advanced."

          #### 2A. Desktop Extensions (One-Click Installs) (5 min)

          **What they are:** Pre-built, vetted integrations you can install with one click right inside Claude Desktop.

          **Talking Points:**

          - This is the easiest way to connect tools. Anthropic (the company behind Claude) has a growing library of extensions.
          - You find them in Settings > Extensions inside Claude Desktop.
          - One click to install, then you authenticate (sign into your Google account, your Slack workspace, etc.), and you're connected.
          - These are curated and tested. They just work.
          - Examples: Google Calendar, Gmail, Slack, Notion

          **Show them (live demo):**

          - Open Claude Desktop > Settings > Extensions
          - Browse what's available
          - Show one that's already installed and what it can do
          - "If your tool has an extension available, start here. This is the easiest path."

          #### 2B. Plugins (Bundled Packages) (5 min)

          **What they are:** Plugins are bundles that can include MCP servers, skills, and tools packaged together. Think of them as "app packs" for Claude.

          **Talking Points:**

          - A plugin might give you an MCP connection PLUS skills that know how to use it well
          - Example: A LinkedIn plugin might include the MCP connection to LinkedIn AND skills for prospecting, posting, and messaging
          - You can find plugins in the plugin directory or get them recommended
          - Plugins are a step up from basic extensions because they come with intelligence built in, not just the connection
          - "This is how my setup works. I don't just have a LinkedIn connection. I have Jorge, who knows HOW to prospect on LinkedIn, and Betsy, who knows HOW to write posts. The connection plus the skill equals the magic."

          **Show them:**

          - Show how plugins appear in your setup
          - Explain that plugins bundle multiple capabilities together
          - "We'll go deeper on building custom plugins later in the series. For now, just know they exist and they're powerful."

          #### 2C. Manual MCP Server Configuration (5 min)

          **What they are:** For tools that don't have a one-click extension or plugin, you can manually configure an MCP server.

          **Talking Points:**

          - This is the most flexible but most technical option
          - You're essentially telling Claude: "Here's an app, here's the API key, here's how to talk to it"
          - Configuration happens through a file called `.mcp.json` or through Settings > Integrations
          - You need the MCP server URL or package name, and usually an API key from the service
          - "This is how I connected GoHighLevel, HeyGen, and some of my more specialized tools. Not everything has a one-click extension yet."
          - Don't scare them: "You don't need to do this today. But I want you to know it exists so when you need a tool that doesn't have an extension, you know there's a path."

          **Show the concept (don't deep dive into code):**

          - Show Settings > Integrations briefly
          - Show what a configured MCP server looks like in your setup
          - "The community is building new MCP servers constantly. If your tool has an API, someone has probably built or is building an MCP server for it."

          ---

          ### SECTION 3: Hands-On - Connect Your First Tool (15 min)

          **Transition:** "Enough talking. Let's actually connect something. Open your Claude Desktop."

          #### Step 1: Pick Your First Extension (3 min)

          **Talking Points:**

          - Open Settings > Extensions
          - "Pick one that's relevant to YOUR workflow. If you use Google Calendar, start there. If you live in Slack, start there."
          - If they're not sure, recommend Google Calendar as a great first one because everyone has a calendar and the results are immediately visible
          - "Don't try to connect everything today. ONE tool. Get it working. Then add more."

          #### Step 2: Install and Authenticate (5 min)

          **Walk them through:**

          - Click Install on their chosen extension
          - Follow the authentication flow (sign into Google, Slack, etc.)
          - Wait for confirmation that it's connected
          - "If you hit a snag, drop it in the chat. We'll troubleshoot together."

          #### Step 3: Test It (5 min)

          **Walk them through testing:**

          - Switch to Cowork mode
          - Ask Claude something that requires the new connection:
            - Google Calendar: "What's on my calendar tomorrow?"
              - Gmail: "Show me my recent emails"
                - Slack: "What's happening in my #general channel?"
                  - Notion: "What pages do I have in my workspace?"
                  - "When Claude answers with REAL data from your app, that's the moment. That's when it clicks. Claude just reached outside the chat and grabbed real information from YOUR tool."

                  #### Step 4: Update Your CLAUDE.md (2 min)

                  **Talking Points:**

                  - Now that you have a tool connected, go back to your CLAUDE.md and add it under your Connected Tools section
                  - This helps Claude know what's available without having to discover it every time

                  ```markdown
                  ## Connected Tools
                  - Google Calendar (via Desktop Extension) - can check schedule, create events
                  ```

                  - "Keep this updated as you add more connections. It's like updating your employee's access list."

                  ---

                  ### SECTION 4: What's Out There - The MCP Ecosystem (10 min)

                  **Transition:** "Now let me show you the landscape. What tools can Claude connect to?"

                  **Talking Points:**

                  - The MCP ecosystem is growing fast. New servers and extensions are being added regularly.
                  - Categories of available connections:

                  **Productivity & Communication:**
                  - Google Calendar, Gmail, Slack, Notion, Microsoft 365

                  **CRM & Sales:**
                  - GoHighLevel, HubSpot, Salesforce, Apollo, ZoomInfo

                  **Social Media:**
                  - LinkedIn, Blotato (multi-platform scheduling)

                  **Development & Data:**
                  - GitHub, Supabase, Vercel, Netlify

                  **Creative & Content:**
                  - Canva, HeyGen (video), Gamma (presentations)

                  **Automation:**
                  - n8n, Zapier

                  - "The question isn't IF your tool can connect. It's WHEN. The ecosystem is moving fast."
                  - "And here's the real power move: when you combine MULTIPLE connections, Claude becomes a command center. I can say 'check my calendar, prep me for my 2pm call, pull up the prospect in my CRM, and draft a follow-up email' and Claude does ALL of that because it has hands in all of those apps."

                  **Show your ecosystem (high level):**

                  - "I have connections to Google Calendar, Gmail, Slack, LinkedIn, GoHighLevel, HeyGen, n8n, Supabase, Notion, Apollo, Gamma, and more. That's how I run three businesses from one Claude project."
                  - "You don't need all of this. Start with one. Add as your workflow demands it."

                  ---

                  ### SECTION 5: Security & Best Practices (5 min)

## Lesson Plan | Building with The AI Sniper

**Instructor:** Cheryl Tibbs, The AI Sniper
**Series:** Building with The AI Sniper | AI Junkies University
**Session:** 2 of 6 | MCP Servers and Connecting Your Tools

---

## Pre-Session Checklist

- [ ] Claude Desktop app open and visible for screen share
- [ ] Student Guide link ready to drop in chat
- [ ] AIJU room open for questions
- [ ] Have at least 2-3 MCP connections visible in your Settings for demo
- [ ] Course repo ready: https://github.com/tibby007/building-with-the-ai-sniper
- [ ] Note for students: Session 1 recording did not save. The student guide and repo materials cover everything from Session 1. Direct students to the repo.

---

## Session Flow (Estimated 60-75 minutes)

### OPENING (7 min)

**Talking Points:**

- Welcome back. Quick housekeeping: the Session 1 recording didn't save. I know, I know. BUT the student guide and all the materials are in the course repo. Everything you need from Session 1 is there. If you missed it or want to review, grab it from the repo.
- Drop the repo link again: https://github.com/tibby007/building-with-the-ai-sniper
- Quick recap of Session 1 (since the recording didn't save, spend an extra minute here):
  - We set up our project folder structure
  - Created our CLAUDE.md (project instructions file)
  - Built our first skill (email drafter)
  - Set up our memory system
  - Cloned the course repo
- "Last session we gave Claude a brain. Today we're giving it HANDS."
- The big idea: Right now, Claude can think and write. After today, Claude can actually DO things in your apps. Send emails. Check your calendar. Post to LinkedIn. Update your CRM. That's what MCPs and connectors do.

---

### SECTION 1: The "Hands" Concept (8 min)

**Key Metaphor to Drive Home:**

Session 1 = Brain (CLAUDE.md, skills, memory). Session 2 = Hands (MCPs, connectors, extensions).

**Talking Points:**

- Think about it this way: after Session 1, Claude knows who you are, how you like things done, and has skills to do specific tasks. But it's still stuck inside the chat window. It can WRITE an email draft, but it can't SEND it. It can PLAN a calendar event, but it can't CREATE one.
- MCPs are what give Claude access to the outside world. They're the bridge between "Claude wrote something nice" and "Claude actually did the thing."
- MCP stands for Model Context Protocol. Don't let the name scare you. All it means is: a standardized way for Claude to talk to your apps and services.
- Think of MCPs like USB ports on your computer. Your computer is powerful on its own, but USB ports let you plug in a keyboard, a mouse, a printer, a camera. MCPs let you plug apps INTO Claude.

**What becomes possible with MCPs:**

- "Send a Slack message to the team" (Claude actually sends it)
- "What's on my calendar tomorrow?" (Claude actually checks)
- "Create a contact in my CRM for this new lead" (Claude actually creates it)
- "Post this to LinkedIn" (Claude actually posts it)
- "Draft a reply to that email from Sarah" (Claude actually pulls up the email and drafts in Gmail)

---

### SECTION 2: Three Ways to Connect Tools (15 min)

**Transition:** "Now there are three ways to give Claude these hands. Let's break them down from easiest to most advanced."

#### 2A. Desktop Extensions (One-Click Installs) (5 min)

**What they are:** Pre-built, vetted integrations you can install with one click right inside Claude Desktop.

**Talking Points:**

- This is the easiest way to connect tools. Anthropic (the company behind Claude) has a growing library of extensions.
- You find them in Settings > Extensions inside Claude Desktop.
- One click to install, then you authenticate (sign into your Google account, your Slack workspace, etc.), and you're connected.
- These are curated and tested. They just work.
- Examples: Google Calendar, Gmail, Slack, Notion

**Show them (live demo):**

- Open Claude Desktop > Settings > Extensions
- Browse what's available
- Show one that's already installed and what it can do
- "If your tool has an extension available, start here. This is the easiest path."

#### 2B. Plugins (Bundled Packages) (5 min)

**What they are:** Plugins are bundles that can include MCP servers, skills, and tools packaged together. Think of them as "app packs" for Claude.

**Talking Points:**

- A plugin might give you an MCP connection PLUS skills that know how to use it well
- Example: A LinkedIn plugin might include the MCP connection to LinkedIn AND skills for prospecting, posting, and messaging
- You can find plugins in the plugin directory or get them recommended
- Plugins are a step up from basic extensions because they come with intelligence built in, not just the connection
- "This is how my setup works. I don't just have a LinkedIn connection. I have Jorge, who knows HOW to prospect on LinkedIn, and Betsy, who knows HOW to write posts. The connection plus the skill equals the magic."

**Show them:**

- Show how plugins appear in your setup
- Explain that plugins bundle multiple capabilities together
- "We'll go deeper on building custom plugins later in the series. For now, just know they exist and they're powerful."

#### 2C. Manual MCP Server Configuration (5 min)

**What they are:** For tools that don't have a one-click extension or plugin, you can manually configure an MCP server.

**Talking Points:**

- This is the most flexible but most technical option
- You're essentially telling Claude: "Here's an app, here's the API key, here's how to talk to it"
- Configuration happens through a file called `.mcp.json` or through Settings > Integrations
- You need the MCP server URL or package name, and usually an API key from the service
- "This is how I connected GoHighLevel, HeyGen, and some of my more specialized tools. Not everything has a one-click extension yet."
- Don't scare them: "You don't need to do this today. But I want you to know it exists so when you need a tool that doesn't have an extension, you know there's a path."

**Show the concept (don't deep dive into code):**

- Show Settings > Integrations briefly
- Show what a configured MCP server looks like in your setup
- "The community is building new MCP servers constantly. If your tool has an API, someone has probably built or is building an MCP server for it."

---

### SECTION 3: Hands-On - Connect Your First Tool (15 min)

**Transition:** "Enough talking. Let's actually connect something. Open your Claude Desktop."

#### Step 1: Pick Your First Extension (3 min)

**Talking Points:**

- Open Settings > Extensions
- "Pick one that's relevant to YOUR workflow. If you use Google Calendar, start there. If you live in Slack, start there."
- If they're not sure, recommend Google Calendar as a great first one because everyone has a calendar and the results are immediately visible
- "Don't try to connect everything today. ONE tool. Get it working. Then add more."

#### Step 2: Install and Authenticate (5 min)

**Walk them through:**

- Click Install on their chosen extension
- Follow the authentication flow (sign into Google, Slack, etc.)
- Wait for confirmation that it's connected
- "If you hit a snag, drop it in the chat. We'll troubleshoot together."

#### Step 3: Test It (5 min)

**Walk them through testing:**

- Switch to Cowork mode
- Ask Claude something that requires the new connection:
  - Google Calendar: "What's on my calendar tomorrow?"
  - Gmail: "Show me my recent emails"
  - Slack: "What's happening in my #general channel?"
  - Notion: "What pages do I have in my workspace?"
- "When Claude answers with REAL data from your app, that's the moment. That's when it clicks. Claude just reached outside the chat and grabbed real information from YOUR tool."

#### Step 4: Update Your CLAUDE.md (2 min)

**Talking Points:**

- Now that you have a tool connected, go back to your CLAUDE.md and add it under your Connected Tools section
- This helps Claude know what's available without having to discover it every time
- "Keep this updated as you add more connections. It's like updating your employee's access list."

---

### SECTION 4: What's Out There - The MCP Ecosystem (10 min)

**Transition:** "Now let me show you the landscape. What tools can Claude connect to?"

**Talking Points:**

- The MCP ecosystem is growing fast. New servers and extensions are being added regularly.
- Categories of available connections:

**Productivity & Communication:**
- Google Calendar, Gmail, Slack, Notion, Microsoft 365

**CRM & Sales:**
- GoHighLevel, HubSpot, Salesforce, Apollo, ZoomInfo

**Social Media:**
- LinkedIn, Blotato (multi-platform scheduling)

**Development & Data:**
- GitHub, Supabase, Vercel, Netlify

**Creative & Content:**
- Canva, HeyGen (video), Gamma (presentations)

**Automation:**
- n8n, Zapier

- "The question isn't IF your tool can connect. It's WHEN. The ecosystem is moving fast."
- "And here's the real power move: when you combine MULTIPLE connections, Claude becomes a command center. I can say 'check my calendar, prep me for my 2pm call, pull up the prospect in my CRM, and draft a follow-up email' and Claude does ALL of that because it has hands in all of those apps."

**Show your ecosystem (high level):**

- "I have connections to Google Calendar, Gmail, Slack, LinkedIn, GoHighLevel, HeyGen, n8n, Supabase, Notion, Apollo, Gamma, and more. That's how I run three businesses from one Claude project."
- "You don't need all of this. Start with one. Add as your workflow demands it."

---

### SECTION 5: Security & Best Practices (5 min)

**Talking Points:**

- Real talk about security. When you connect Claude to your apps, you're giving it access. Treat that seriously.
- **API Keys:** Some MCP connections require API keys. These are like passwords. Don't share them. Don't put them in public files. Claude stores them securely, but be mindful.
- **Permissions:** Most connections ask what Claude can do. Read-only vs. read-and-write. Start with the minimum you need.
- **Review what's connected:** Periodically check Settings > Integrations to see what Claude has access to. Remove anything you're not using.
- "Think of it like giving an employee keys to the office. You give them what they need to do their job, and you know what they have access to."
- **One thing to remember:** Claude will always ask before taking major actions. It won't just start sending emails or deleting things without your approval. There's a confirmation step built in.

---

### SECTION 6: The Bigger Picture - Where This Goes (5 min)

**Transition:** "Let me show you what happens when you put Session 1 and Session 2 together."

**Talking Points:**

- Session 1 gave Claude a brain (CLAUDE.md, skills, memory)
- Session 2 gave Claude hands (MCPs, connectors, extensions)
- When you combine brain + hands, you get an AI that knows who you are AND can take action
- "That's the difference between a chatbot and a digital employee."

**Quick preview of what's coming:**

- Session 03: Building Custom Skills - teaching Claude HOW to use those hands
- Session 04: Memory Systems and Context Management - making Claude remember everything
- Session 05: Advanced Workflows and Automation - chaining it all together
- Session 06: Putting It All Together - Your AI Command Center

- "Next session we go deep on skills. You've built one basic skill. Next time we're building REAL skills that work with your connected tools."

---

### Q&A + WRAP (10 min)

**Talking Points for Close:**

- "Reminder: Session 1 recording didn't save, but ALL the materials are in the course repo." Drop link: https://github.com/tibby007/building-with-the-ai-sniper
- "Today's student guide has everything we covered, including the step-by-step for connecting your first tool."
- "Your homework: Connect at least ONE tool via Desktop Extensions. Test it. Update your CLAUDE.md to reflect the new connection. Drop your results in the Building with The AI Sniper room."
- "If you want extra credit, try connecting a SECOND tool and see how Claude uses them together."
- Tease Session 3: "Next time we build real custom skills. The kind that make Claude work like a specialist, not a generalist."

**Common questions to anticipate:**

- "Is it safe to connect my email/calendar?" - Yes, Anthropic's extensions use standard OAuth authentication. Claude doesn't store your password. You can revoke access anytime.
- "What if my tool doesn't have an extension?" - Check if there's a plugin or community MCP server. If not, it may come soon. The ecosystem is growing fast.
- "Can Claude access my tool without me being in the conversation?" - No. Claude only uses your connections during active conversations. It doesn't run in the background accessing your apps without you.
- "Do I need to pay extra for MCP connections?" - The connections themselves are included with your Claude plan. Some third-party tools may require their own API keys or subscriptions.
- "What's the difference between an extension and a plugin?" - An extension is usually a single connection to one service. A plugin is a bundle that can include connections, skills, and other tools packaged together.

---

## Post-Session Tasks

- [ ] Drop the student guide link in the AIJU room
- [ ] Post a "show your first connection" challenge
- [ ] Announce Session 3 date and topic (Building Custom Skills)
- [ ] Save Q&A highlights for future content
- [ ] Note: Record this session! (Session 1 recording was lost)
