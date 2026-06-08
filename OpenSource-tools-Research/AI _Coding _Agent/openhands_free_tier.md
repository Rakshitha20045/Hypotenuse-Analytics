# OpenHands — Free Tier Guide (2026)

> **Last Updated:** June 2026 | **Status:** Active — Fully open source (MIT), self-hosted only

---

## 1. Free Tier Overview

OpenHands is an **AI-powered software development agent** that can write, edit, debug, and run code. It is **100% open source (MIT license)** — there is no cloud service, no paid plan, no API fees to OpenHands itself.

### How "Free" Works

| Component | Cost | What You Pay For |
|---|---|---|
| **OpenHands software** | **$0** | Nothing — MIT open source |
| **LLM API (required)** | **Variable** | You bring your own API key (OpenAI, Anthropic, Google, etc.) |
| **Compute (required)** | **Your hardware** | Runs on your machine or cloud VM |

> **Important:** OpenHands itself is free. You only pay for the LLM API calls it makes and the compute you run it on.

---

## 2. What You Need to Run (Costs)

### Option A: Local Machine (Free except LLM API)

| Requirement | Spec | Cost |
|---|---|---|
| **Docker** | Installed | $0 |
| **RAM** | 8GB+ recommended | Your hardware |
| **LLM API Key** | OpenAI, Anthropic, Google, etc. | Per-token pricing |

```bash
# Run locally (free software, you pay for LLM calls)
docker run -it --rm --pull=always   -e SANDBOX_RUNTIME_CONTAINER_IMAGE=docker.all-hands.dev/all-hands-ai/runtime:0.26-nikolaik   -v /var/run/docker.sock:/var/run/docker.sock   -v ~/.openhands-state:/.openhands-state   -p 3020:3000   --name openhands-app   docker.all-hands.dev/all-hands-ai/openhands:0.26
```

### Option B: Cloud VM (Free tier eligible)

| Provider | Free Tier | Specs | Good For |
|---|---|---|---|
| **GitHub Codespaces** | 120 core-hours/mo | 2 cores, 8GB RAM | Light coding tasks |
| **Google Cloud Shell** | Always free | 1.7GB RAM, ephemeral | Testing only |
| **Oracle Cloud Free Tier** | Always free | 4 cores, 24GB RAM | Serious use |
| **AWS Free Tier** | 750 hrs/mo (12mo) | t2.micro | Light use |

---

## 3. LLM API Costs (What You Actually Pay)

OpenHands needs an LLM to function. Here are cheap/free options:

| LLM Provider | Free Tier | Cost When Paid | Best For |
|---|---|---|---|
| **Google Gemini 2.5 Flash** | 1,500 RPD free | $0.30/1M tokens | Best free option |
| **OpenRouter (free models)** | 50 RPD free | Per-token | Model variety |
| **Groq** | Generous free tier | Very cheap | Fast inference |
| **Ollama (local)** | $0 (your GPU) | $0 | Full privacy, no API |
| **OpenAI GPT-4o** | No free API | $5/1M input | Best quality |
| **Anthropic Claude** | No free API | $3/1M input | Best reasoning |

**Typical Cost per Coding Session:**
- Small task (bug fix): ~$0.05-0.20
- Medium task (feature): ~$0.50-2.00
- Large task (refactor): ~$2.00-10.00

---

## 4. Task-by-Task: What Can You Build?

### ✅ Excellent (Low LLM Cost)

| Task | Example | Est. Cost | Why |
|---|---|---|---|
| **Bug fixes** | Fix a TypeError | $0.05-0.20 | Small context, targeted |
| **Code review** | Review a PR | $0.10-0.50 | Single file focus |
| **Refactor small functions** | Extract method | $0.10-0.30 | Limited scope |
| **Write tests** | Generate unit tests | $0.20-0.80 | Pattern-based |
| **Documentation** | Generate docstrings | $0.05-0.20 | Structured output |
| **Dependency updates** | Update package versions | $0.10-0.50 | Simple changes |

### ⚠️ Moderate Cost (Watch Your Budget)

| Task | Example | Est. Cost | Tip |
|---|---|---|---|
| **Add features** | New API endpoint | $0.50-3.00 | Use cheaper LLM |
| **Debug complex issues** | Race condition | $1.00-5.00 | Limit iterations |
| **Code migration** | Python 2→3 | $2.00-10.00 | Break into chunks |
| **Architecture changes** | Refactor monolith | $5.00-20.00 | Use Gemini Flash |

### ❌ Expensive / Slow (Not Recommended on Tight Budget)

| Task | Why Expensive | Alternative |
|---|---|---|
| **Full app from scratch** | Many iterations, large context | Break into milestones |
| **Large codebase refactoring** | Massive context window needed | Do module by module |
| **Complex algorithm design** | Requires deep reasoning | Use Claude/GPT-4 sparingly |
| **Multi-file coordination** | Many API calls | Use cheaper LLM |

---

## 5. Free Tier Strategy

### The "Cheap LLM First" Approach

```
Step 1: Configure OpenHands with Gemini 2.5 Flash (free tier)
Step 2: Try task with free LLM
Step 3: If fails, switch to better LLM for that specific step
Step 4: Track API costs per session
```

### Cost Control Tips

1. **Use Gemini 2.5 Flash free tier** — 1,500 RPD covers most sessions
2. **Set iteration limits** — Prevent runaway agent loops
3. **Start with small scopes** — Fix one bug, not refactor entire app
4. **Use local LLMs (Ollama)** for simple tasks — $0 cost
5. **Monitor token usage** — Check dashboard after each session

---

## 6. Quick Cheat Sheet

```
OPENHANDS FREE TIER CHEAT SHEET

SOFTWARE: 100% FREE (MIT open source)
  • Download: docker pull (free)
  • No license fees, no subscription

WHAT YOU PAY FOR:
  • LLM API calls (bring your own key)
  • Compute (your machine or cloud VM)

CHEAPEST LLM SETUP:
  • Google Gemini 2.5 Flash: 1,500 RPD free
  • Ollama (local): $0, needs GPU
  • OpenRouter free models: 50 RPD free

TYPICAL COSTS PER SESSION:
  • Bug fix: $0.05-0.20
  • Feature add: $0.50-3.00
  • Large refactor: $2.00-10.00

BEST FREE TASKS:
  • Bug fixes and debugging
  • Code reviews
  • Writing tests
  • Documentation generation
  • Small refactors
  • Dependency updates

COST CONTROL:
  • Use Gemini Flash free tier first
  • Set max iterations
  • Start small, expand scope
  • Track tokens per session

FREE CLOUD OPTIONS:
  • GitHub Codespaces: 120 hrs/mo
  • Oracle Cloud: Always free (4 cores, 24GB)
  • AWS Free Tier: 750 hrs (first 12mo)
```

---

## 7. Summary

**OpenHands is completely free software.** Your only costs are:
1. **LLM API calls** — Use Gemini 2.5 Flash free tier (1,500 RPD) to stay at $0
2. **Compute** — Run on your existing machine or free cloud tier

**Best Strategy:** Configure with Gemini 2.5 Flash → do small tasks → track costs → upgrade LLM only when necessary.
