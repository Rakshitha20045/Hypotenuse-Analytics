# Grok API Models — Free Tier Complete Guide (2026)

> **Last Updated:** June 2026 | **Status:** Consumer free tier active; API free credits available

---

## 1. Free Tier Overview: Two Different Worlds

Grok has **two separate free tiers** that are often confused:

1. **Consumer App Free Tier** (grok.com, X app): ~10 prompts per 2 hours
2. **API Free Credits** (console.x.ai): Up to $150-175/month for developers

### Critical Distinction

| Aspect | Consumer Free Tier | API Free Credits |
|---|---|---|
| **Access** | grok.com or X app | console.x.ai |
| **Cost** | $0 | $0 (promotional) |
| **Rate Limit** | ~10 prompts/2 hours | $150-175 credit budget |
| **Models** | Limited Grok 4, older variants | All API models |
| **Best For** | Casual chat, testing personality | Building apps, prototyping |
| **Reliability** | Consumer-grade | Developer-grade |

---

## 2. Consumer App Free Tier Deep Dive

### 2.1 What You Actually Get (Free)

**Rate Limits:**
- **~10 prompts per 2-hour window** (varies by demand)
- **~120 prompts/day maximum** if you perfectly time every window
- **Realistic usage:** 30-50 prompts/day due to clustering

**Model Access:**
- **Grok 4** (limited, not the latest 4.3)
- **Grok 3** and older variants (fallback routing)
- **NO Grok 4.3** (requires SuperGrok Heavy $300/mo or API)

**Features Included:**
| Feature | Free Tier | Limit |
|---|---|---|
| Text chat | ✅ | 10/2hrs |
| Real-time X data | ✅ | Slight delay on busy days |
| Basic web search | ✅ | Via X integration |
| Aurora image generation | ✅ | ~10 images/2hrs |
| Voice mode | ✅ | Basic quality |
| Memory | ✅ | Limited |
| DeepSearch | ✅ | Usage limits |
| Projects & Tasks | ✅ | Reduced level |

**Features NOT Included:**
| Feature | Requires |
|---|---|
| Grok 4.3 (latest flagship) | SuperGrok Heavy ($300) or API |
| Grok Imagine (full image gen) | SuperGrok Lite ($10+) |
| 480p+ video generation | SuperGrok Lite ($10+) |
| Document upload/PDF analysis | SuperGrok ($30+) |
| Deep reasoning mode | SuperGrok ($30+) |
| Companions (Ani, Rudy, etc.) | SuperGrok ($30+) |
| Priority queue | Any paid tier |
| Higher rate limits | Any paid tier |

---

### 2.2 Consumer Free Tier: Task-by-Task

| Task | Viable on Free? | Why / Workaround |
|---|---|---|
| **Casual Q&A** | ✅ Excellent | 10 prompts/2hrs is enough for casual use |
| **Quick coding help** | ✅ Good | Small snippets, debugging |
| **Real-time news/X analysis** | ✅ Unique | Grok's killer feature — free tier gets this |
| **Content brainstorming** | ✅ Good | 10 ideas per 2 hours |
| **Long coding sessions** | ❌ Poor | 10 prompts isn't enough for deep work |
| **Document analysis** | ❌ Impossible | No upload feature on free |
| **Image generation** | ⚠️ Limited | Basic Aurora only, ~10 images/2hrs |
| **Multi-step agents** | ❌ Impossible | Rate limits prevent agent loops |
| **Research reports** | ⚠️ Difficult | Need many prompts, hit limit fast |
| **Writing long content** | ⚠️ Difficult | 10 prompts = ~2-3 long generations |

### 2.3 Consumer Free Tier Strategy

**The "10 Prompt Budget" Framework:**

```
Per 2-hour window:
├── High Value (4 prompts): Complex questions, coding, analysis
├── Medium Value (4 prompts): Follow-ups, clarifications, refinement  
└── Experimental (2 prompts): Testing features, creative play
```

**Tips to Maximize Free Consumer Tier:**
1. **Batch questions:** Ask multiple things in one prompt
2. **Use DeepSearch wisely:** One DeepSearch = multiple regular prompts in value
3. **Time your usage:** Plan around the 2-hour reset windows
4. **Use X integration:** Ask Grok to analyze specific threads/profiles
5. **Don't waste on simple tasks:** Use free tier for Grok's unique features (X data, personality)

---

## 3. API Free Credits Deep Dive

### 3.1 What Are API Free Credits?

xAI offers **promotional free API credits** for developers:

| Program | Amount | Requirements | Status |
|---|---|---|---|
| **Data Sharing Program** | Up to $150/month | Enable "Share API Inputs for Model Training" | Verify current availability |
| **New User Promotion** | One-time credit | New console.x.ai signup | Subject to change |
| **Startup/Research Grants** | Custom | Application required | Check xAI console |

> **Important:** These programs are subject to change. Verify current terms at console.x.ai before building dependencies.

### 3.2 API Pricing: What $150 Gets You

With $150/month in free credits, here's what you can build:

| Model | Price (Input/Output per 1M) | $150 Budget Gets You |
|---|---|---|
| **Grok 4.1 Fast** | $0.20 / $0.50 | ~75M input tokens + 150M output tokens |
| **Grok 4.3** | $1.25 / $2.50 | ~12M input tokens + 24M output tokens |
| **Grok Build 0.1** | $1.00 / $2.00 | ~15M input tokens + 30M output tokens |
| **Grok 4.20 Multi-Agent** | $1.25 / $2.50 | ~12M input tokens + 24M output tokens |

**Real-World Translation:**
- **Grok 4.1 Fast:** ~50,000 average API calls (3,000 tokens each)
- **Grok 4.3:** ~8,000 average API calls
- **Grok Build 0.1:** ~10,000 coding-focused API calls

### 3.3 API Rate Limits (Even with Credits)

| Limit | Free/Promo Tier | Paid Tier |
|---|---|---|
| **Requests Per Minute** | ~20-60 RPM | Custom |
| **Tokens Per Minute** | ~100,000 TPM | 1M+ TPM |
| **Concurrent Requests** | Limited | Higher |
| **Burst Handling** | Deprioritized | Guaranteed |

### 3.4 API Free Tier: Task-by-Task

| Task | Best Model | $150/Month Capacity | Viability |
|---|---|---|---|
| **Production chatbot** | Grok 4.1 Fast | 50K calls | ✅ Excellent |
| **Coding assistant API** | Grok Build 0.1 | 10K calls | ✅ Good |
| **Agent orchestration** | Grok 4.20 Multi-Agent | 8K calls | ✅ Good for prototype |
| **High-volume extraction** | Grok 4.1 Fast | 50K calls | ✅ Excellent |
| **Complex reasoning API** | Grok 4.3 | 8K calls | ⚠️ Moderate |
| **Long document processing** | Grok 4.20 Multi-Agent | 8K calls | ⚠️ Context eats budget |
| **Real-time search + API** | Grok 4.3 + Tools | 5K calls | ⚠️ Tools cost extra |

**Tool Costs (Billed Separately):**
- Web Search: $5 per 1,000 calls
- X Search: $5 per 1,000 calls
- Code Execution: $5 per 1,000 calls
- File Attachments: $10 per 1,000 calls

---

## 4. Model Selection: Free Tier Edition

### 4.1 Consumer App: Which Model Do You Actually Get?

**The Opacity Problem:**
Grok's consumer app uses **Auto Mode** that dynamically routes to different models. You cannot reliably know which model served your query.

| Tier | Likely Model | Grok 4.3 Access | Transparency |
|---|---|---|---|
| **Free** | Grok 4 (limited) + older | ❌ No | None |
| **X Premium ($8)** | Grok 4 inside X | ⚠️ Limited | None |
| **SuperGrok Lite ($10)** | Grok 4 | ⚠️ Limited | None |
| **SuperGrok ($30)** | Grok 4 + 4.3 (staged) | ⚠️ Rolling rollout | None |
| **SuperGrok Heavy ($300)** | Grok 4 Heavy + full 4.3 | ✅ Confirmed | Limited |

**For Free Users:**
- Expect **Grok 4-level** capability, not 4.3
- For guaranteed model version: **Use the API** with dated model IDs

### 4.2 API: Explicit Model Selection

```python
# API free tier lets you CHOOSE the model
# Use dated IDs for reproducibility

MODELS = {
    # Free tier with $150 credits - most efficient
    "fast_cheap": "grok-4.1-fast",        # $0.20/$0.50 per 1M

    # Free tier with $150 credits - balanced  
    "balanced": "grok-4.3",                # $1.25/$2.50 per 1M

    # Free tier with $150 credits - coding specialist
    "coding": "grok-build-0.1",            # $1.00/$2.00 per 1M

    # Free tier with $150 credits - multi-agent
    "agents": "grok-4.20-multi-agent-0309", # $1.25/$2.50 per 1M
}
```

---

## 5. Task-by-Task: Free Tier Recommendations

### 5.1 General Chat & Q&A

| Use Case | Best Free Option | Why | Limitation |
|---|---|---|---|
| Casual conversation | Consumer free | Personality, X data | 10/2hrs |
| Chatbot prototype | API + 4.1 Fast | 50K calls/month | Need credits |
| Research assistant | Consumer free | DeepSearch | Rate limited |
| High-volume FAQ | API + 4.1 Fast | Cheapest | Credit budget |

### 5.2 Coding & Development

| Use Case | Best Free Option | Why | Capacity |
|---|---|---|---|
| Quick debug | Consumer free | Fast access | 10 snippets/2hrs |
| Code review API | API + Build 0.1 | Tuned for code | ~10K reviews/month |
| Generate tests | API + Build 0.1 | Specialized | ~10K test suites/month |
| Architecture design | Consumer free | Long-form reasoning | Very limited |
| Production IDE | API + 4.1 Fast | Fast, cheap | 50K completions/month |

### 5.3 Agents & Automation

| Use Case | Best Free Option | Why | Architecture |
|---|---|---|---|
| Simple API agent | API + 4.1 Fast | Tool use, cheap | 50K agent steps/month |
| Multi-agent system | API + 4.20 Multi-Agent | Built for orchestration | 8K orchestrations/month |
| Consumer agent | ❌ Not viable | Rate limits too tight | Need SuperGrok |
| Research agent | API + 4.3 | DeepSearch integration | 8K runs/month |

### 5.4 Reasoning & Analysis

| Use Case | Best Free Option | Why | Note |
|---|---|---|---|
| Math/logic | API + 4.3 | Configurable reasoning | Budget ~8K calls |
| Data analysis | API + 4.1 Fast | High volume | Budget ~50K calls |
| Scientific research | Consumer free | DeepSearch | 10 queries/2hrs |
| Competitive analysis | Consumer free | X data unique | Grok's killer feature |

### 5.5 Multimodal (Image/Video/Voice)

| Use Case | Best Free Option | Why | Limit |
|---|---|---|---|
| Image description | Consumer free | Basic Aurora | 10 images/2hrs |
| Image generation | Consumer free | Aurora basic | 10 images/2hrs |
| Video generation | ❌ Not free | Requires SuperGrok Lite | $10/month minimum |
| Voice mode | Consumer free | Basic | 10 sessions/2hrs |
| API image analysis | API + 4.3 | Token-based | Credit budget |

---

## 6. Rate Limits: Complete Reference

### Consumer App Free Tier

| Limit | Value | Notes |
|---|---|---|
| **Prompts per 2 hours** | ~10 | Varies by demand, can be lower |
| **Images per 2 hours** | ~10 | Aurora basic |
| **DeepSearch per day** | Limited | Unspecified soft limit |
| **Voice sessions** | ~10/2hrs | Basic quality |
| **Context window** | Unknown | Likely 128K or less |
| **Reset mechanism** | 2-hour sliding window | Not daily |

### API Free/Promo Tier

| Limit | Value | Notes |
|---|---|---|
| **Credit budget** | $150-175/month | Promotional, verify current |
| **RPM** | 20-60 | Lower than paid |
| **TPM** | 100,000 | Sufficient for most apps |
| **Concurrent requests** | Limited | Queue behavior |
| **Model availability** | All models | Including 4.3 |
| **Tool usage** | Billed separately | Search, code exec, files |

### Error Handling

| Error | Meaning | Solution |
|---|---|---|
| **Rate limit exceeded** | 2-hour window hit | Wait for reset, upgrade |
| **Credit exhausted** | $150 budget spent | Add payment method |
| **Model unavailable** | Staged rollout gap | Retry with different model |
| **Content policy** | $0.05 fee per violation | Fix prompt design |

---

## 7. Free Tier Strategy: Maximizing Value

### Consumer App Strategy

**The "Grok Difference" Approach:**
Don't waste free prompts on tasks other AIs do well. Use Grok free for:
1. **X/Twitter analysis** (unique real-time data)
2. **Live event tracking** (sports, markets, news)
3. **Personality-driven chat** (Grok's humor/style)
4. **Quick takes** on trending topics

**Avoid on Free:**
- Long document analysis (no upload)
- Deep coding sessions (rate limited)
- Image generation (basic Aurora only)
- Production workloads (unreliable)

### API Strategy with $150 Credits

**The "Budget Burn" Framework:**

```
Month 1: Prototype Phase
├── 40% Grok 4.1 Fast (20K calls) - Testing, simple tasks
├── 40% Grok Build 0.1 (4K calls) - Coding experiments  
└── 20% Grok 4.3 (1.6K calls) - Reasoning benchmarks

Month 2: Scale Phase  
├── 70% Grok 4.1 Fast (35K calls) - Production load
├── 20% Grok Build 0.1 (2K calls) - Code pipeline
└── 10% Grok 4.3 (800 calls) - Complex fallback
```

**Optimization:**
1. **Use prompt caching:** Cuts input cost by ~85% ($0.05 vs $0.20-1.25)
2. **Batch non-urgent work:** Async processing discounts
3. **Avoid tool overuse:** $5/1K calls adds up fast
4. **Monitor credit burn:** Set alerts at 50%, 75%, 90%

---

## 8. Free vs Paid: Complete Comparison

| Feature | Consumer Free | API Free Credits | SuperGrok ($30) | API Paid |
|---|---|---|---|---|
| **Cost** | $0 | $0 (promo) | $30/mo | Per-token |
| **Rate Limit** | 10/2hrs | $150/mo budget | ~100/2hrs | Custom |
| **Grok 4.3** | ❌ | ✅ | ⚠️ Staged | ✅ |
| **Document Upload** | ❌ | ✅ (API) | ✅ | ✅ |
| **Image Gen** | Basic Aurora | Token-based | Full Imagine | Token-based |
| **Video Gen** | ❌ | ❌ | 480p | ❌ |
| **Deep Reasoning** | ❌ | ✅ | ✅ (Big Brain) | ✅ |
| **Priority** | Lowest | Medium | High | Custom |
| **SLA** | None | None | None | Enterprise |
| **Support** | Community | Community | Priority | Dedicated |

---

## 9. Code Examples: Free Tier Usage

### 9.1 Consumer Free Tier: Rate Limit Tracker

```python
import time
from datetime import datetime, timedelta

class GrokConsumerTracker:
    def __init__(self, prompts_per_window=10, window_hours=2):
        self.limit = prompts_per_window
        self.window = timedelta(hours=window_hours)
        self.history = []  # List of (timestamp, prompt_count)

    def can_prompt(self):
        now = datetime.now()
        cutoff = now - self.window
        recent = [t for t, _ in self.history if t > cutoff]
        return len(recent) < self.limit

    def record_prompt(self, count=1):
        now = datetime.now()
        self.history.append((now, count))
        cutoff = now - self.window
        self.history = [(t, c) for t, c in self.history if t > cutoff]

    def get_status(self):
        now = datetime.now()
        cutoff = now - self.window
        recent = [t for t, _ in self.history if t > cutoff]
        used = len(recent)

        return {
            'window_limit': self.limit,
            'used_this_window': used,
            'remaining': self.limit - used,
            'next_reset': (recent[0] + self.window) if recent else now,
            'status': 'OK' if used < self.limit else 'LIMITED'
        }

# Usage
tracker = GrokConsumerTracker()

if tracker.can_prompt():
    tracker.record_prompt()
    print(f"Prompt sent! Status: {tracker.get_status()}")
else:
    status = tracker.get_status()
    print(f"Rate limited. Wait until {status['next_reset']}")
```

### 9.2 API Free Credits: Budget Manager

```python
class GrokAPIBudget:
    MODEL_RATES = {
        'grok-4.1-fast': {'input': 0.20, 'output': 0.50},
        'grok-4.3': {'input': 1.25, 'output': 2.50},
        'grok-build-0.1': {'input': 1.00, 'output': 2.00},
        'grok-4.20-multi-agent': {'input': 1.25, 'output': 2.50},
    }

    TOOL_COSTS = {
        'web_search': 5.00,
        'x_search': 5.00,
        'code_execution': 5.00,
        'file_attachment': 10.00,
    }

    def __init__(self, monthly_budget=150.00):
        self.budget = monthly_budget
        self.spent = 0.0
        self.usage_log = []

    def estimate_cost(self, model, input_tokens, output_tokens, tools=None):
        rates = self.MODEL_RATES.get(model, self.MODEL_RATES['grok-4.3'])
        input_cost = (input_tokens / 1_000_000) * rates['input']
        output_cost = (output_tokens / 1_000_000) * rates['output']
        total = input_cost + output_cost

        if tools:
            for tool, count in tools.items():
                cost_per_1k = self.TOOL_COSTS.get(tool, 0)
                total += (count / 1000) * cost_per_1k

        return total

    def can_afford(self, model, input_tokens, output_tokens, tools=None):
        cost = self.estimate_cost(model, input_tokens, output_tokens, tools)
        return (self.spent + cost) <= self.budget

    def record_usage(self, model, input_tokens, output_tokens, tools=None):
        cost = self.estimate_cost(model, input_tokens, output_tokens, tools)
        self.spent += cost
        self.usage_log.append({
            'model': model,
            'input_tokens': input_tokens,
            'output_tokens': output_tokens,
            'cost': cost,
            'remaining_budget': self.budget - self.spent
        })
        return cost

    def get_budget_report(self):
        remaining = self.budget - self.spent
        percentage = (self.spent / self.budget) * 100

        return {
            'total_budget': self.budget,
            'spent': round(self.spent, 2),
            'remaining': round(remaining, 2),
            'percentage_used': round(percentage, 1),
            'status': 'HEALTHY' if percentage < 50 else 'WARNING' if percentage < 80 else 'CRITICAL',
            'estimated_calls_remaining': {
                model: int(remaining / ((rates['input'] + rates['output']) / 1_000_000 * 3000))
                for model, rates in self.MODEL_RATES.items()
            }
        }

# Usage
budget = GrokAPIBudget(monthly_budget=150.00)

if budget.can_afford('grok-4.1-fast', input_tokens=500, output_tokens=1000):
    budget.record_usage('grok-4.1-fast', input_tokens=500, output_tokens=1000)
    print(budget.get_budget_report())
else:
    print("Budget exhausted! Switch to cheaper model or add payment method.")
```

### 9.3 Smart Model Router for Free Tier

```python
def select_grok_model(task_type: str, budget_remaining: float, urgency: str = 'normal') -> str:
    if budget_remaining < 10:
        return 'grok-4.1-fast'

    if budget_remaining < 50:
        if task_type in ['code']:
            return 'grok-build-0.1'
        return 'grok-4.1-fast'

    model_map = {
        'chat': 'grok-4.1-fast',
        'code': 'grok-build-0.1',
        'reasoning': 'grok-4.3',
        'agent': 'grok-4.20-multi-agent',
        'fast': 'grok-4.1-fast',
    }

    if urgency == 'high' and budget_remaining > 100:
        if task_type == 'chat':
            return 'grok-4.3'
        if task_type == 'code':
            return 'grok-4.3'

    return model_map.get(task_type, 'grok-4.1-fast')

# Example usage
budget = GrokAPIBudget(150.00)
model = select_grok_model('code', budget_remaining=120, urgency='high')
print(f"Task: code, Urgency: high → Using {model}")
```

---

## 10. Migration Path: Free → Paid

### Phase 1: Consumer Free User
- Use grok.com for casual chat, X analysis
- Hit 10 prompts/2hrs? Wait or upgrade to SuperGrok ($30)

### Phase 2: API Developer (Free Credits)
- Build prototypes with $150/month credits
- Use 4.1 Fast for volume, 4.3 for quality
- Monitor credit burn carefully

### Phase 3: API Developer (Paid)
- Add payment method when credits run out
- Cost: ~$30-200/month for light usage
- Scale to $500+/month for production

### Phase 4: Enterprise
- Custom contracts, SLA, dedicated support
- Volume discounts, custom rate limits

---

## 11. Quick Reference: Free Tier Cheat Sheet

```
GROK FREE TIER CHEAT SHEET (June 2026)

CONSUMER APP (grok.com):
• 10 prompts per 2-hour window
• Access: Grok 4 (limited), NO 4.3
• Features: Chat, X data, basic Aurora, voice, DeepSearch
• NO: Document upload, video gen, full Imagine, 4.3

API FREE CREDITS (console.x.ai):
• Up to $150-175/month promotional credits
• Access: ALL models including 4.3
• Best value: Grok 4.1 Fast ($0.20/$0.50 per 1M)
• ~50K calls/month on 4.1 Fast, ~8K on 4.3

BEST FREE MODELS BY TASK:
• Casual chat/X analysis → Consumer free (unique data)
• API chatbot prototype → API 4.1 Fast (50K calls)
• Coding/IDE → API Build 0.1 (10K calls)
• Complex reasoning → API 4.3 (8K calls)
• Multi-agent → API 4.20 Multi-Agent (8K calls)
• High-volume extraction → API 4.1 Fast (50K calls)

UPGRADE SIGNALS:
• Consumer: Hitting 10/2hrs consistently
• API: Burning $150 before month end
• Need: Document upload, video gen, guaranteed 4.3
• Building: Production app with SLA requirements
```

---

## 12. Summary: The Free Tier Winner

**For consumer use:** Grok's free tier is **excellent for casual chat and X/Twitter analysis** — the 10 prompts/2hrs is genuinely usable if you batch questions and use Grok's unique real-time data features.

**For developers:** The **API free credits ($150/month)** make Grok one of the most generous free tiers for building prototypes. With 4.1 Fast at $0.20/$0.50, you can make ~50,000 API calls — enough for serious prototyping.

**Key Strategy:**
- **Consumer free:** Use for Grok's unique features (X data, personality)
- **API free:** Use for volume, coding, agents, production prototypes
- **Upgrade to SuperGrok ($30)** when you need document upload, image generation, or higher consumer limits
- **Upgrade to API paid** when you need guaranteed capacity, SLA, or burn through $150/month
