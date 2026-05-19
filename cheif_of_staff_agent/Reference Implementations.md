### goagentflow/ai-chief-of-staff – Claude Code + M365 CoS Template

- Repo: https://github.com/goagentflow/ai-chief-of-staff  

**What this template is for**

- Claude Code–based **Chief of Staff agent** that uses a **folder structure + markdown + prompts** as an external brain.
- Designed to be your **executive assistant + persistent memory** for work.

**What it automates / supports (from the author’s description)**

- **Track everything**
  - Tracks **clients, projects, prospects, decisions, and follow-ups** using structured markdown files.
  - Gives you a single place where all ongoing work and decisions live.

- **Write in your voice**
  - Drafts **emails, LinkedIn posts, and documents** in *your* style.
  - Uses style/voice files so Claude learns your tone and applies it consistently.

- **Maintain context with persistent memory**
  - Uses **markdown files as long-term memory** between sessions so Claude doesn’t “forget”.
  - Acts as an external brain: decisions and notes are stored in files Claude can reread.

- **Run daily routines**
  - Morning check-ins
  - Standup processing
  - End-of-day (EOD) reconciliation
  - These routines read/update your markdown memory and create a daily operating rhythm.

- **Integrate with Microsoft 365 (via MCP / connectors)**
  - **Calendar**: pulls meetings and schedules; can prepare you for upcoming events.
  - **Email**: scans inbox (Outlook/M365) to find important messages and actions.
  - **Teams transcripts**: ingests Teams meeting transcripts for summaries and action items.
  - **Files**: accesses relevant documents stored in M365/OneDrive/SharePoint for context.
  - All exposed to Claude through **MCP-style connectors**, so the agent can “see” and act on your M365 data.

**How you can use this repo**

- As a **reference implementation** for:
  - Folder + markdown memory design.
  - Daily routines (check-in, standup, EOD) for a CoS agent.
  - Using Claude Code + MCP to connect to Microsoft 365.
- As a **starting template**:
  - Fork, then change the markdown structure and routines to match your own workflows.