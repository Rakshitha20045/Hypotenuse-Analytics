## GitHub Repositories – AI Chief of Staff / CoS Agents 

> These projects as references for architecture, prompts, memory design, and integrations when designing your own CoS agent.

---

### 1. rs-ai/ChiefOfStaff
- Repo: https://github.com/rs-ai/ChiefOfStaff  
- Focus:
  - AI Chief of Staff for startup / executive workflows.
  - Emphasis on strategy, metrics, and operations support.
- Likely Features:
  - Executive dashboards and decision support.
  - Task and follow-up generation from notes and meetings.
- Likely Integrations:
  - Check repo for concrete connectors (calendar, email, PM tools, metrics systems).

---

### 2. davekilleen/Dex – “Your AI Chief of Staff” [web:54]
- Repo: https://github.com/davekilleen/dex  
- Focus:
  - Personal operating-system (OS) starter kit.
  - CoS-style assistant for individuals.
- Features:
  - Opinionated structure for personal workflows.
  - Daily planning, task management, and review flows.
- Integrations:
  - Designed to hook into your local/hosted tools (see repo for supported apps).

---

### 3. mimurchison/claude-chief-of-staff [web:152][web:153][web:164]
- Repo: https://github.com/mimurchison/claude-chief-of-staff  
- Focus:
  - Claude-based CoS used by a CEO in real work.
- Features:
  - Persistent memory via structured markdown files.
  - Morning briefs, meeting prep, inbox triage, weekly review.
  - Many “skills” (commands) like `/morning-brief`, `/meeting-prep`.
- Integrations:
  - Claude Code environment.
  - Google Workspace–style tools (email, calendar, docs) via scripts/tools (see repo + blog).[web:90]

---

### 4. jimprosser/claude-code-cos  [web:154]
- Repo: https://github.com/jimprosser/claude-code-cos  
- Focus:
  - How to configure Claude Code as a personal CoS.
- Features:
  - Folder structure and prompts for commitments, projects, decisions.
  - Routines for daily and weekly reviews.
- Integrations:
  - Claude Code.
  - Local file system (markdown memory).

---

### 5. tronmongoose/chiefofstaff – “Chief of Staff AI” [web:101]
- Repo: https://github.com/tronmongoose/chiefofstaff  
- Focus:
  - Privacy-first autonomous CoS with voice.
- Features:
  - Always-on assistant that can run workflows.
  - Voice interface for interaction.
- Integrations:
  - Likely speech (STT/TTS), calendar, tasks; check repo for exact services.

---

### 6. mboverell/ai-chief-of-staff [web:159][web:165]
- Repo: https://github.com/mboverell/ai-chief-of-staff  
- Focus:
  - Turn meeting notes, priorities, and reflections into executive insight.
  - Built around an Obsidian/markdown vault.
- Features:
  - Meeting capture and action extraction.
  - Relationship and commitment tracking.
  - Daily/weekly summaries from your notes.
- Integrations:
  - Obsidian vault / markdown file structure.
  - Local indexing / search daemons.

---

### 7. JoshuaSeidel/ai-chief-of-staff [web:169]
- Repo: https://github.com/JoshuaSeidel/ai-chief-of-staff  
- Focus:
  - AI productivity assistant with microservices architecture.
- Features:
  - Processes meeting transcripts.
  - Generates tasks, summaries, and follow-ups.
- Integrations:
  - Meeting platforms (Zoom/Teams transcripts).
  - Task / PM tools (see repo for specifics).

---

### 8. goagentflow/ai-chief-of-staff – Claude Code + M365 [web:49]
- Repo: https://github.com/goagentflow/ai-chief-of-staff  
- Focus:
  - Claude Code–based CoS template with Microsoft 365.
- Features (per description):
  - Track: clients, projects, prospects, decisions, follow-ups.
  - Write in your voice: emails, LinkedIn posts, docs.
  - Maintain context: markdown files as persistent memory.
  - Run routines: morning check-ins, standups, EOD reconciliation.
- Integrations:
  - Microsoft 365: calendar, email, Teams transcripts, files via MCP/connectors.
  - Cloud scheduling via Supabase/edge functions.

---

### 9. tairona717-code/Cybertron-Agentic-AI [web:146]
- Repo: https://github.com/tairona717-code/Cybertron-Agentic-AI  
- Focus:
  - Multi-agent system with COO / CoS-like agents.
- Features:
  - Agents for standups, reports, and follow-ups.
  - Orchestrated workflows across projects/teams.
- Integrations:
  - Designed to interface with PM and communication tools (see repo).

---

### 10. tomochang/ai-chief-of-staff [web:94]
- Repo: https://github.com/tomochang/ai-chief-of-staff  
- Focus:
  - Chief-of-staff skill used with Claude Code.
- Features:
  - Routing, decision logging, orchestration as a “skill”.
- Integrations:
  - Claude Code.
  - File-based memory / tools defined in the repo.

---

### 11. alirezarezvani/claude-skills – `cs-chief-of-staff` [web:87]
- Repo: https://github.com/alirezarezvani/claude-skills  
- Focus:
  - Collection of Claude skills; includes `cs-chief-of-staff`.
- Features:
  - CoS agent for “virtual boardroom” orchestration.
  - Decision summaries and logging to memory.
- Integrations:
  - Claude Code + MCP tools defined in the skills repo.

---

### 12. AINative-Studio/founderhouse – CoS Agile Backlog [web:144]
- Repo: https://github.com/AINative-Studio/founderhouse  
- Focus:
  - Not a full agent; **spec/backlog** for an AI CoS.
- Features:
  - `backlog.md` with “AI Chief of Staff — Agile Backlog (MCP Edition)”.
  - User stories for sprints, standups, and agile SaaS CoS features.
- Integrations:
  - Serves as a requirements doc for MCP + tools, not an implementation.

---

### 13. chainyo/staff-ai – AI Workforce Framework [web:88]
- Repo: https://github.com/chainyo/staff-ai  
- Focus:
  - Framework for an “AI workforce” (multi-agent).
- Features:
  - Spawns multiple specialized agents.
  - Coordinates work across tasks/roles (can emulate CoS behavior).
- Integrations:
  - Designed to plug into arbitrary APIs and tools you define.

---

### 14. langchain-ai/langchain – Agent Templates [web:22]
- Repo: https://github.com/langchain-ai/langchain/tree/master/templates  
- Focus:
  - General agent templates, not CoS-specific.
- Features:
  - Multi-agent routing, tool use, memory patterns.
  - Good starting point for CoS orchestration logic.
- Integrations:
  - Large ecosystem: databases, vector stores, external APIs, etc.

---

### 15. Akshat2430/ai-chief-of-staff – Claude Code Tutorial Build [web:175]
- Repo: https://github.com/Akshat2430/ai-chief-of-staff  
- Focus:
  - “Build your AI Chief of Staff in 45 minutes with Claude Code”.
- Features:
  - Tutorial-style CoS agent: inbox triage, meeting prep, task generation.
  - Prompts and folder structure aimed at beginners.
- Integrations:
  - Runs inside Claude Code with local files.
  - Optional connections to email/calendar depending on tutorial steps.
