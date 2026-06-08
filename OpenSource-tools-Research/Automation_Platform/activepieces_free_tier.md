# Activepieces — Free Tier Guide (2026)

> **Last Updated:** June 2026 | **Status:** Active — Cloud free + Self-hosted (MIT open source)

---

## 1. Free Tier Overview

Activepieces is an **open-source no-code automation platform** (MIT license). You can use it **completely free** by self-hosting, or use the **Cloud Free plan** with limits.

### Two Ways to Use Free

| Option | Cost | Limits | Best For |
|---|---|---|---|
| **Cloud Free (Standard)** | $0 | 10 active flows, unlimited runs, AI agents, MCP servers, tables | Testing, small automations |
| **Self-Hosted (Community Edition)** | $0 | Unlimited everything | Production, teams, privacy |

---

## 2. Cloud Free Plan (Standard) — Limits Explained

### What You Get (Free)

| Feature | Limit | What It Means |
|---|---|---|
| **Active Flows** | **10** | 10 workflows can be ON/running at once |
| **Runs** | **Unlimited** | No limit on how many times flows execute |
| **AI Agents** | **Included** | AI-powered steps available |
| **MCP Servers** | **Unlimited** | Model Context Protocol servers |
| **Tables** | **Unlimited** | Database tables for data storage |
| **Users** | **1** | Only you |
| **Projects** | **1** | One workspace |
| **Support** | Community | Discord/forum only |

### What Is an "Active Flow"?

An **Active Flow** = a workflow that is **turned ON and running**.

**Examples:**
- Gmail → AI → Slack (enabled) = **1 active flow**
- Google Form → Sheets (enabled) = **1 active flow**
- Instagram DM → AI Reply (enabled) = **1 active flow**

If all 3 are ON, that's **3 active flows**.

> **Free plan allows 10 active flows.** You can build unlimited flows, but only 10 can be enabled at once.

### Paid: $5 per active flow per month

After the 10 free active flows, each additional active flow costs **$5/month**.

Example:
- 10 active flows = **$0** (free)
- 15 active flows = **$25/month** (5 extra × $5)
- 20 active flows = **$50/month** (10 extra × $5)

---

## 3. AppSumo Lifetime Deal (LTD) — For Reference

| Feature | LTD | Standard Free |
|---|---|---|
| **Flows** | Unlimited | 10 active |
| **AI Agents** | 5 | Included |
| **AI Credits** | 200 | Uses your own API keys |
| **MCP Servers** | 1 | Unlimited |
| **Tables** | 1 | Unlimited |
| **Human In The Loop** | ✅ | ❌ |
| **Tasks** | As bought | Unlimited runs |

> LTD is a one-time purchase deal. Standard Free is the ongoing free tier.

---

## 4. Task-by-Task: What Can You Build on Free?

### ✅ Excellent on Free (10 Active Flows + Unlimited Runs)

| Use Case | Flow Example | Why It Works |
|---|---|---|
| **Email auto-reply** | Gmail → AI → Send reply | Low volume, high value |
| **Form to spreadsheet** | Google Form → Sheets | Simple, reliable |
| **Slack notifications** | Trigger → Filter → Slack | Internal alerts |
| **Social media cross-post** | RSS → Buffer/Twitter | Scheduled, predictable |
| **Lead capture** | Landing page → CRM | Low frequency |
| **Daily report** | Scheduler → API → Email | Once per day |
| **Instagram DM auto-reply** | Instagram → AI → Reply | Social automation |
| **Customer support ticket** | Email → AI → Ticket system | Support workflow |
| **Data sync** | API → Transform → Database | Background sync |
| **Alert monitoring** | Monitor → Filter → Alert | DevOps/ops |

### ⚠️ Tight on Free (May Need More Than 10 Flows)

| Use Case | Why Tight | Workaround |
|---|---|---|
| **Agency managing 20+ clients** | Each client needs multiple flows | Self-host or pay per flow |
| **Complex multi-department org** | Sales, marketing, ops all need flows | Combine into fewer flows |
| **Micro-SaaS with user automations** | Each user = potential flow | Self-host |

### ❌ Not Possible on Free

| Use Case | Why | Solution |
|---|---|---|
| **11+ simultaneous automations** | Only 10 active flows free | Pay $5/flow or self-host |
| **Team collaboration** | 1 user only | Upgrade or self-host |
| **Priority support** | Community only | Upgrade |

---

## 5. Self-Hosted: The Real Free Tier

Since Activepieces is **MIT open source**, you can self-host with **zero limits**:

```bash
# Docker self-host (completely free)
docker run -d   -p 3000:3000   -v activepieces_data:/root/.activepieces   activepieces/activepieces:latest
```

**Self-Hosted Gets You:**
- ✅ Unlimited active flows
- ✅ Unlimited runs
- ✅ Unlimited AI agents (bring your own API keys)
- ✅ Unlimited MCP servers
- ✅ Unlimited tables
- ✅ Unlimited users
- ✅ Full data privacy

**What You Need:**
- A server (VPS ~$5-10/mo or home server)
- Docker knowledge (basic)
- Your own AI API keys (OpenAI, Gemini, etc.)

---

## 6. Free Tier Strategy

### The "10 Flow Budget" Framework

```
Flow 1-3 (Critical): Your most important automations
  • Customer email → AI → Reply
  • Lead capture → CRM
  • Daily reports

Flow 4-7 (Important): Supporting workflows
  • Slack notifications
  • Social media posting
  • Form handling

Flow 8-10 (Utility): Nice-to-have
  • Personal reminders
  • Backup tasks
  • Testing/experimental
```

**Tips:**
1. **Build many, enable 10:** Draft unlimited flows, only turn on the 10 most critical
2. **Combine flows:** One flow with multiple branches > multiple separate flows
3. **Use conditional logic:** One flow can handle multiple scenarios with if/else
4. **Self-host for real work:** Cloud free is for testing; self-host for production

---

## 7. Quick Cheat Sheet

```
ACTIVEPIECES FREE TIER CHEAT SHEET

CLOUD FREE (STANDARD) — $0:
• 10 active flows (ON/running workflows)
• Unlimited runs (no execution limit)
• AI agents included
• Unlimited MCP servers
• Unlimited tables
• 1 user, 1 project
• Community support
• Paid: $5 per extra active flow/month

APPSUMO LTD (One-time purchase):
• Unlimited flows
• 5 AI agents
• 200 AI credits
• 1 MCP server
• 1 table
• Human In The Loop

SELF-HOSTED ($0 + server cost):
• Unlimited everything
• Bring your own API keys
• Full privacy
• Needs Docker + VPS (~$5-10/mo)

BEST FREE USES:
• Email auto-replies
• Form to spreadsheet
• Slack notifications
• Social media scheduling
• Instagram DM replies
• Lead capture
• Daily/weekly reports
• Alert monitoring

UPGRADE WHEN:
• Need 11+ active flows ($5/flow)
• Need team collaboration
• Want priority support
```

---

## 8. Summary

**Cloud Free** is generous: **10 active flows + unlimited runs + AI agents + MCP servers + tables**.

**Self-Hosted** is the **true unlimited free tier** — just need a server and your own API keys.

**Best Strategy:** Use all 10 free active flows on Cloud → if you need more, either pay $5/flow or self-host.
