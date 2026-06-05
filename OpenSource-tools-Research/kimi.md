# Kimi (Moonshot AI) – Complete Guide for Builders (kimi.md)

> This document explains Kimi, its models, UI features, agent ecosystem, open‑source story, pricing/free tiers, and how to use it for company “Chief‑of‑Staff” (CoS) style agents. It’s written so any teammate (engineer, PM, founder) can understand what Kimi is and how to use it.

---

## 1. High‑Level Overview – What Kimi Is

Kimi is a chatbot product and **family of large language models (LLMs)** created by Chinese company **Moonshot AI**.[web:11][web:154]  
It is available as:

- A consumer assistant at **kimi.com** (chat, Docs, Sheets, Slides, Websites, Deep Research, etc.).[web:206][web:204]
- A **developer platform** with HTTP APIs and tool‑calling.[web:209]
- A growing **open‑weight model suite** (Kimi‑K2, Kimi‑K2.5, Kimi‑Dev, Kimi‑VL, etc.) published on GitHub / Hugging Face.[web:115][web:41][web:126]

Kimi’s main strengths:

- **Long‑context reasoning** – can work with up to ~256K tokens of context in modern K2.x models (hundreds of pages or many files at once).[web:22][web:209]
- **Strong coding & SWE** – Kimi‑Dev‑72B and K2.5/K2.6 are competitive with frontier models on SWE‑bench and other coding benchmarks.[web:41][web:154]
- **Agentic workflows** – K2 Thinking / K2.5 / K2.6 support multi‑step tool use and **Agent Swarm** for complex, multi‑agent tasks.[web:51][web:154]
- **Office automation** – Docs, Sheets, Slides, Websites features generate and manage real Word, Excel, PPT, and HTML content.[web:204][web:206]

---

## 2. Timeline and Key Milestones

A condensed timeline of Kimi’s evolution:

- **Oct 2023 – Initial Kimi chatbot**
  - First public release with a **128K‑token context window**, focused on long‑context chat and document understanding.[web:11]

- **Apr 2025 – Kimi‑VL**
  - Release of **Kimi‑VL**, a 16B‑parameter Mixture‑of‑Experts (MoE) multimodal LLM with ~3B active parameters, optimized for **vision‑language** tasks.[web:11]

- **Jun 2025 – Kimi‑VL‑Thinking & Kimi‑Dev**
  - **Kimi‑VL‑Thinking**: reasoning‑optimized VL variant, trained with chain‑of‑thought supervision and RL.[web:11]
  - **Kimi‑Dev‑72B**: coding‑oriented model based on Qwen2.5‑72B; achieves **state‑of‑the‑art on SWE‑bench Verified among open models**.[web:41][web:109]

- **Jul 2025 – Kimi‑K2**
  - Release of **Kimi K2**, a **1‑trillion‑parameter MoE** LLM with about **32B active parameters** per token.[web:115][web:108]
  - Open‑sourced under a **Modified MIT‑style license**, with very strong coding and general benchmarks.[web:89][web:160]

- **Sep 2025 – Kimi‑K2‑Instruct‑0905**
  - Upgraded K2 variant doubling context window to **256K tokens** and improving coding performance.[web:11][web:22]

- **2025–2026 – K2 Thinking / K2.5 / K2.6**
  - **K2 Thinking**: emphasizes chain‑of‑thought and heavy tool‑calling (200–300 sequential tool calls).[web:33][web:37]
  - **Kimi‑K2.5**: “Visual Agentic Intelligence” – multimodal, agent‑oriented, supports Agent Swarm with up to 100 sub‑agents.[web:154][web:121][web:48]
  - **Kimi‑K2.6**: latest flagship as of 2026; strengthens long‑horizon coding, agent swarm (up to 300 sub‑agents), and better agent coordination.[web:141][web:139][web:132]

---

## 3. Model Lineup – The Kimi Family

### 3.1 Core Chat & Reasoning Models

#### Kimi K2 / K2.5 / K2.6

- **Kimi K2**
  - ~1T total parameters, ~32B active parameters per token (MoE).[web:115][web:108]
  - Focus: strong general reasoning, coding, long context (up to 128K/256K tokens).[web:22][web:90]

- **Kimi K2.5**
  - Open‑weight, **multimodal agentic** model trained on ~15T mixed visual + text tokens.[web:126][web:154]
  - Supports:
    - Text + images (and some video contexts via frames)
    - Agent Swarm (up to 100 sub‑agents, ~1,500 tool calls)[web:48][web:130]
    - Visual coding (from UI mockups / screenshots to code and full apps).[web:154]

- **Kimi K2.6**
  - Latest model focused on:
    - More stable long‑term coding
    - Enhanced Agent Swarm (up to ~300 sub‑agents, ~4,000 steps)[web:141][web:132][web:139]
    - Stronger performance across reasoning and coding benchmarks.[web:209][web:154]

#### K2 Thinking / “Thinking”‑style Modes

- “Thinking” variants emphasize:
  - Explicit chain‑of‑thought
  - Heavy tool‑calling (code, web, docs)
  - Up to ~200–300 tool calls in complex workflows[web:33][web:37]
- Designed for:
  - Deep research
  - Multi‑step analyses (finance, law, science)
  - Agentic, tool‑rich environments

#### Moonshot V1

- Original generative model on the Kimi API:
  - Context window: ~131,072 tokens.[web:8]
  - Higher per‑token cost than newer K2 models; now mainly legacy / fallback.

---

### 3.2 Open Models and Specialization

#### Kimi K2 (open‑weight)

- July 2025 release exposing model weights under a **Modified MIT license**:
  - Can be downloaded and self‑hosted.[web:115][web:89]
  - Commercial use allowed, with attribution requirements only for very large products.[web:89]
- Community notes that **later K2.x variants (e.g., some K2.5 API versions) are not fully open‑source**; they’re open for use via API, but weights may not be publicly released.[web:14][web:160]

#### Kimi‑VL

- 16B‑parameter MoE VL model (~3B active parameters):
  - Designed for **image understanding and reasoning** over diagrams, tables, and documents.[web:11]
  - **Kimi‑VL‑Thinking** is a reasoning‑optimized variant with chain‑of‑thought and RL.[web:11][web:6]

#### Kimi‑Dev (72B coding model)

- 72B‑parameter, open‑weight coding model based on **Qwen2.5‑72B**, tuned for SWE tasks.[web:41][web:109]
- Achieves **60.4% on SWE‑bench Verified**, SOTA among open‑source coding LLMs.[web:41][web:39]
- Focus areas:
  - Code generation across multiple languages
  - Refactoring and bug fixing in real repositories
  - Multi‑file, repo‑level understanding and test generation[web:41][web:109]

---

## 4. Architecture & Training

### 4.1 Mixture‑of‑Experts (MoE)

- Kimi’s K2 family uses a **Mixture‑of‑Experts** architecture:
  - Very large total parameter count (~1T), but only ~32B active parameters per token.[web:115][web:22]
  - This design allows scaling to trillion‑parameter models while keeping inference costs manageable.[web:1][web:12]
- Compared to DeepSeek‑R1:
  - Kimi K2 uses fewer attention heads but more experts per MoE layer.
  - Supports larger vocabulary and longer context windows, tuned for long‑context performance and reasoning.[web:1][web:12]

### 4.2 Reinforcement Learning for Reasoning

- Inspired by DeepSeek‑R1, Kimi k1.5 and K2‑family reasoning models use **reinforcement learning (RL)** on top of supervised pretraining and CoT finetuning.[web:6]
- RL objective:
  - Rewards sequences of reasoning that lead to correct outcomes on math, coding, and scientific problems, not just token‑level likelihood.[web:6]
- RL is also used to optimize **answer length**:
  - Trade‑off between extremely long explanations and concise but accurate ones.
  - Reported reductions of ~10–20% in response length on math benchmarks with similar or better accuracy.[web:6]

### 4.3 Data Scale & Training Tokens

- Kimi K2 is reported to be trained on **~15.5T tokens**, comparable to DeepSeek V3/R1 at ~14.8T tokens.[web:12]
- This large, diverse corpus underpins:
  - Strong generalization across code, math, and scientific text
  - Good multilingual performance
  - Robustness on long‑form documents[web:12][web:160]

---

## 5. Kimi UI Features (Sidebar)

Kimi’s web UI groups features by workflow. Each item here is visible in the sidebar and backed by K2.x models.[web:206][web:135]

### 5.1 Slides

- **Text → Slides**:
  - Paste an article, outline, or notes → Kimi generates a slide deck with titles, bullets, and basic design.[web:47][web:59]
- Use cases:
  - Tech talks, internal updates, teaching decks, sales slides.

### 5.2 Websites

- **Prompt → Website**:
  - Describe your product / design → Kimi creates copy + layout + HTML/CSS/JS.[web:154][web:206]
- Supports visual coding:
  - From screenshots / wireframes to front‑end code.[web:154][web:48]

### 5.3 Docs

- **Kimi Docs**:
  - Strong text adaptation and structured understanding of Word/PDF workflows.[web:204][web:206]
  - Can create:
    - Reports, white papers, RFPs
    - Meeting notes, SOPs, contracts
  - Handles headings, tables, references, and exports to Word/PDF.[web:204][web:205]

### 5.4 Sheets

- **Kimi Sheets**:
  - AI spreadsheet agent that can:
    - Generate tables from prompts or web data
    - Extract data from PDFs to Excel
    - Merge department sheets into a single summary with formulas[web:204][web:205]
  - Exports to `.xlsx` for Excel or WPS.

### 5.5 Deep Research

- Dedicated mode for **multi‑step web research**:
  - Automatically searches web, opens pages, reads, and synthesizes across sources.
  - Outputs structured reports and outlines.
- Under the hood, uses tool‑calling and agentic strategies (K2 Thinking / K2.5 Agent modes).[web:154][web:159][web:53]

### 5.6 Agent Swarm

- Button opens **Agent Swarm** interface:
  - Lets K2.5/K2.6 decompose a large task and spin up many sub‑agents in parallel.[web:51][web:125][web:132]

See Section 6 for deeper explanation.

### 5.7 Kimi Code

- Opens the **developer‑focused coding agent**:
  - Tight integration with Kimi Code CLI / IDE plugins.
  - Focuses on software‑engineering tasks: implementing features, refactoring, debugging, writing tests.[web:123][web:208]

### 5.8 Kimi Claw

- Connects to **Kimi Claw**, the managed OpenClaw agent:
  - One‑click deployment of a persistent 24/7 AI assistant.[web:46][web:200]
  - Supports **Claw Groups** (multi‑user multi‑agent collaboration) and messaging channels.[web:46][web:190]

---

## 6. Agent Swarm – Skills & Behavior

**Agent Swarm** = Kimi’s multi‑agent system:

- K2.5: up to **100 sub‑agents**, ~1,500 tool calls.[web:48][web:130]
- K2.6: up to **300 sub‑agents** and ~4,000 steps per request.[web:141][web:125][web:136]

Skill *types* inside a swarm (not fixed names, but roles):

1. **Search & browse**
   - Sub‑agents call web search, open pages, scrape data in parallel.[web:125][web:132]

2. **Reading & analysis**
   - Agents read PDFs, web pages, docs; extract key points, tables, and structured info.[web:125][web:137]

3. **Data & reasoning**
   - Build comparison tables, calculate metrics, synthesize numeric insights.[web:125][web:141]

4. **Coding**
   - Generate, refactor, and debug code; run tools to validate changes.[web:125][web:139]

5. **Long‑form writing**
   - Draft chapters, reports, CVs, proposals, and other long documents.[web:132][web:134]

6. **Visual generation**
   - Create Slides, Websites, and formatted Docs from the gathered information.[web:132][web:154][web:50]

Workflow example for a big request (e.g., market report):

- Orchestrator: designs plan and spawns:
  - Search agents → gather info
  - Analysis agents → build tables
  - Writer agents → draft sections
  - Visual agents → build slides and site
- Then merges everything into final deliverables.[web:51][web:132][web:134]

---

## 7. Kimi Claw & OpenClaw

### 7.1 Kimi Claw (Managed OpenClaw)

- **Kimi Claw** is Moonshot’s **one‑click managed OpenClaw**:
  - An AI assistant with memory and personality, deployed via Kimi’s infrastructure.[web:189][web:200]
  - Runs 24/7, across multiple messaging platforms (WhatsApp/Telegram/etc.).[web:46][web:190]

Key points:

- Requires **Allegretto tier (~$39/month) or higher**; not fully free.[web:194][web:55]
- Integrates deeply with Kimi’s models (K2.5/K2.6), Agent Swarm, and Kimi desktop/web apps.[web:46][web:192]

Deployment options in UI:

- **On Cloud Server** – Kimi deploys and hosts OpenClaw in its cloud, always on.[web:189]
- **On My Computer** – runs an OpenClaw runtime on your PC via the Kimi Desktop App; still uses Kimi cloud models for intelligence.[web:202][web:188]
- **On Android Phone** – runs OpenClaw on your Android device.[web:189]

> “On My Computer” controls where the **agent runtime** lives (local vs cloud), not whether the model is free.

### 7.2 OpenClaw (Open‑Source)

- **OpenClaw** itself is an **open‑source AI agent**:
  - Runs scripts, manages files, and automates tasks.
  - Can be self‑hosted on your machine or a server.[web:199][web:190]
- **OpenClaw Desktop App / Windows Hub**:
  - Free desktop companion that shows tasks, status, and chat interface.[web:193][web:181]

You can connect OpenClaw to any model provider:

- Kimi K2.5 (via API)
- Claude, GPT‑style APIs
- Local LLMs running via vLLM/Ollama/TGI

Kimi Claw = “managed OpenClaw with Kimi models & billing”;  
OpenClaw alone = “DIY agent with whatever model you configure”.

---

## 8. Kimi Code & Kimi Code CLI

### 8.1 Kimi Code (Developer Product)

- Kimi Code is a **toolkit for developers**:
  - Fast coding models and tools
  - CLI agent (Kimi Code CLI)
  - IDE integration for VS Code and others[web:123][web:208]
- Use cases:
  - Implementing features from specs
  - Large‑scale refactorings
  - Generating tests and scripts
  - Debugging complex issues

Official docs:  
- Kimi Code overview: https://www.kimi.com/code/docs/en/[web:208]

### 8.2 Kimi Code CLI (Command‑Line Coding Agent)

- **Kimi Code CLI** (`kimi-cli`) is an AI agent that runs in your terminal:

Capabilities:[web:118][web:122][web:149]

- Reads and edits code files in your repo
- Runs shell commands (tests, builds, scripts)
- Fetches web content for research
- Plans multi‑step tasks and reacts to errors

Modes:

- `kimi` – interactive terminal chat.
- `kimi web` – local browser UI for code agent.
- `kimi acp` – Agent Client Protocol mode to connect IDEs (VS Code, Cursor, etc.).[web:118][web:127]

Install & quick start (simplified):[web:118]

```sh
# Install (Linux/macOS)
curl -LsSf https://code.kimi.com/install.sh | bash

# Or Windows (PowerShell)
Invoke-RestMethod https://code.kimi.com/install.ps1 | Invoke-Expression

# Use in a repo
cd /path/to/your/project
kimi
# inside kimi prompt:
#   /login – authenticate with Kimi Code
#   then start asking coding tasks
```

Command‑line coding agent mental model:

> “An AI dev buddy living in your terminal that can **actually change files and run commands**, not just suggest code.”

---

## 9. Open‑Source Kimi Ecosystem

### 9.1 Main Repositories (MoonshotAI GitHub)

Moonshot’s GitHub: https://github.com/MoonshotAI[web:107][web:110]

Key repos:

- **Kimi‑K2** – base MoE LLM (1T parameters, 32B active).[web:115]
- **Kimi‑K2.5** – open‑weight multimodal agentic model.[web:126]
- **Kimi‑Dev** – coding LLM (72B).[web:41]
- **kimi‑cli** – Kimi Code CLI.[web:149]
- Additional infra: checkpoint‑engine, agent building blocks, etc.[web:107][web:110]

### 9.2 Licenses & Openness

- **Kimi‑K2 / K2.5**: Modified MIT‑style license:
  - Free to use, copy, modify, and distribute.
  - Very large products (100M+ MAU or >$20M/month revenue) must show “Kimi K2.5” attribution and comply with additional conditions.[web:82][web:89]
- **Kimi‑Dev, Kimi‑VL, Kimi‑Audio**: open‑weight with permissive licenses; see each repo for exact terms.[web:41][web:109][web:11]

Important:

- Open‑source = **open weights**, not necessarily full training code/data.
- Some K2.5 variants are API‑only (hosted) despite the base model being open‑weight.[web:14][web:160]

---

## 10. Free vs Paid – Practical View

### 10.1 Web App (kimi.com)

- Free tier: around **30–50 messages/day** in the main chat UI, depending on usage.[web:104]
- Underlying limit: documentation and third‑party analyses indicate about **1.5M tokens/day** for lower tiers (input + output combined).[web:60][web:66][web:100]
- Limits reset every 24 hours; pro plans raise caps and unlock features (Docs/Slides/Code limits, Kimi Claw, etc.).[web:72][web:103]

### 10.2 API

- API pricing is **per‑token** (per 1M tokens for input and output), plus fees for some tools (e.g., web search).[web:76][web:67]
- External trackers list K2.5 pricing in the competitive range compared to GPT‑5.x and other frontier models.[web:79][web:98]

### 10.3 Kimi Claw

- Kimi Claw managed OpenClaw requires **Allegretto tier (~$39/month)** at launch; it uses your membership credits and has usage limits.[web:194][web:55][web:200]

### 10.4 Open‑Source Models

- Downloading and running **Kimi‑K2.5** or **Kimi‑Dev** locally has **no per‑token fee to Moonshot**.
- You still pay for:
  - Hardware (GPUs/CPUs, RAM, storage)
  - Cloud instances (if you host in cloud)
  - Any external APIs the agent uses (Slack, Notion, financial APIs, etc.)[web:126][web:164][web:199]

---

## 11. CoS (Chief‑of‑Staff) Use Cases

Kimi’s strengths match CoS‑style work for a company:

1. **Research & decision briefs**
   - Agent Swarm + Deep Research can scan markets, competitors, regulations, and internal docs to produce concise executive briefs.[web:51][web:159][web:160]

2. **Docs & decks**
   - Kimi Docs & Slides generate strategies, OKRs, PRDs, proposals, investor decks from rough notes.[web:204][web:47][web:206]

3. **Sheets & reporting**
   - Kimi Sheets builds and maintains KPI tables, financial models, and consolidated cross‑team status sheets.[web:204][web:205]

4. **Ops & project tracking**
   - With connections to Jira/Notion/Drive, Kimi can summarize project status, highlight risks, and propose next actions.[web:159][web:160]

5. **Light engineering support**
   - Kimi‑Dev + Kimi Code CLI generate scripts, small tools, ETL glue, and automation to support operations.[web:41][web:118][web:139]

Two deployment patterns:

- **Hosted CoS** – Use Kimi web/app + API + n8n/Zapier to orchestrate jobs.
- **Self‑hosted CoS** – Use open‑weight K2.5/Kimi‑Dev inside your own infra or via OpenClaw, paying only for compute.

---

## 12. Local Hosting & Hardware Considerations

### 12.1 Full K2.5/K2.6 (very heavy)

- Guides suggest:
  - **~240–250 GB RAM** for K2.5 CPU/hybrid setups.[web:163][web:171]
  - DGX‑class multi‑GPU setups (e.g., 8× H100) for high‑throughput serving.[web:168][web:172][web:175]

This is **data‑center scale**, not consumer.

### 12.2 More realistic setups

- **Experimenting at home**:
  - 1× 24 GB GPU (RTX 4090/3090/5090)
  - 128–256 GB RAM
  - 1.8–4‑bit quantization + offload to RAM/SSD[web:174][web:163]

- **Strong coding with Kimi‑Dev‑72B**:
  - 2× 24 GB GPUs or 1× 48 GB GPU with 4‑bit quant.
  - 64–128 GB RAM.[web:164][web:167][web:173]

For most builders, it’s more efficient to:

- Run **smaller local models** for routine stuff, and
- Call K2.5/K2.6 via API for heavy reasoning and Agent Swarm.

---

## 13. Quick‑Start Recipes

### 13.1 As a normal user

1. Go to **https://kimi.com** and create an account.
2. Use:
   - **Chat** for general Q&A.
   - **Deep Research** for multi‑step research.
   - **Docs/Sheets/Slides/Websites** for office tasks.[web:206][web:204]
   - **Kimi Code** for dev work.
   - **Agent Swarm** for very big tasks.

### 13.2 As a developer – API

1. Register on **Kimi API platform** and get an API key.[web:209][web:76]
2. Follow the chat/completions examples in the docs (OpenAI‑style JSON).
3. Add tools (web search, HTTP fetch, DB queries) and let K2.6 coordinate them.

### 13.3 As an agent builder – OpenClaw + Kimi

**Option A – OpenClaw + Kimi API (semi‑free CoS)**

1. Install **OpenClaw Desktop or CLI** from openclaw.ai.[web:193][web:187][web:199]
2. Configure **Kimi K2.5** as an OpenAI‑compatible provider with your Kimi API key.[web:191]
3. Give OpenClaw access to:
   - Local folders (docs, code)
   - SaaS APIs (e.g., Notion, Google Drive, Jira, Slack)
4. Define:
   - Daily briefing workflow
   - Weekly status report workflow
   - On‑demand doc/deck creation workflows

**Option B – OpenClaw + Local LLM (fully local)**

1. Run a local model (via vLLM/Ollama) exposing an OpenAI‑compatible API.[web:175]
2. Configure OpenClaw to use `http://localhost:...` as provider.
3. Use same CoS workflows; everything runs on your hardware.

---

## 14. Official Kimi & Kimi Code / Docs Links

These links are the canonical references for more details:

- **Kimi Claw (Kimi bots / OpenClaw integration)**  
  https://www.kimi.com/bot[web:46][web:200]

- **Kimi API Platform Overview**  
  https://platform.kimi.ai/docs/overview[web:209]

- **Kimi Code – Overview & Docs**  
  https://www.kimi.com/code/docs/en/[web:208][web:123]

- **Kimi Code CLI – Getting Started**  
  https://www.kimi.com/code/docs/en/kimi-code-cli/guides/getting-started.html[web:118][web:208]

- **Kimi Docs & Kimi Sheets – Overview**  
  https://www.kimi.com/help/docs-and-sheets/docs-and-sheets-overview[web:204]

Use this `kimi.md` as the shared reference so that anyone joining the team quickly understands:

- What Kimi is
- What each sidebar feature does
- How Agent Swarm, Kimi Claw, and Kimi Code CLI fit together
- How open‑source Kimi models can be used in our own agents, including CoS‑style systems.