# OpenRouter — Free Tier Complete Guide (2026)

> **Last Updated:** June 2026 | **Status:** Active — 50 requests/day free, 1000 with $10 credits

---

## 1. Free Tier Overview: The Unified Gateway

OpenRouter's free tier is unique: **it's not a model provider, it's a router.** This means you get access to **hundreds of models** from dozens of providers through one free tier.

### Two Free Tiers

| Tier | Cost | Request Limit | Model Access | Best For |
|---|---|---|---|---|
| **Free Plan** | $0 | 50 requests/day | `:free` model variants | Learning, testing, tiny prototypes |
| **Pay-as-you-go (with $10+ credits)** | $10 minimum | 1000 free requests/day | `:free` + paid models | Serious prototyping, small production |

### The `:free` Magic

OpenRouter negotiates free access with providers. Models ending in `:free` cost $0:
- `google/gemini-2.5-flash:free`
- `meta-llama/llama-4-scout:free`
- `mistralai/mistral-small-3.2:free`
- `deepseek/deepseek-chat:free`
- `nvidia/llama-3.1-nemotron-70b:free`

> **Note:** Free-tier usage of popular models can be subject to **additional rate limiting by the provider** during peak times. Failed attempts still count toward your daily quota.

---

## 2. Free Tier Rate Limits: Complete Breakdown

### Free Plan ($0)

| Limit | Value | Notes |
|---|---|---|
| **Requests Per Day (RPD)** | 50 | Hard limit |
| **Requests Per Minute (RPM)** | 20 | Burst protection |
| **Models** | `:free` variants only | No paid models |
| **Fallbacks** | Enabled | Automatic failover |
| **Streaming** | Supported | Real-time responses |
| **Context** | Model-dependent | Up to model's max |

### Pay-as-you-go (with $10+ credits)

| Limit | Value | Notes |
|---|---|---|
| **Free model RPD** | 1000 | 20x more than free plan |
| **Free model RPM** | 20 | Same burst limit |
| **Paid model limits** | None | Use any model, pay per token |
| **Priority** | Higher than free | Better routing |
| **Fallback reliability** | Better | Less likely to hit provider limits |

### Provider-Side Limits (Beyond OpenRouter)

Even with OpenRouter's limits, the **underlying provider** may impose additional restrictions:

| Provider | Free Tier Quirk | Impact |
|---|---|---|
| **Google** | 1,500 RPD direct | OpenRouter free = subset of this |
| **Anthropic** | No free tier direct | OpenRouter `:free` may be limited |
| **Mistral** | Generous free | Usually reliable on OpenRouter |
| **Meta/Llama** | Open weights | Often stable free access |
| **DeepSeek** | Free tier exists | Can be rate-limited during peak |
| **NVIDIA** | Free tier | Usually good availability |

---

## 3. `:free` Model Catalog: What's Actually Available

### High-Quality Free Models (As of June 2026)

| Model | Provider | Strength | Context | Reliability |
|---|---|---|---|---|
| `google/gemini-2.5-flash:free` | Google | General purpose, 1M context | 1M | 5/5 |
| `google/gemini-2.5-flash-lite:free` | Google | High volume, cheap | 1M | 5/5 |
| `meta-llama/llama-4-scout:free` | Meta | Open model, good reasoning | 128K | 4/5 |
| `meta-llama/llama-4-maverick:free` | Meta | Better than Scout | 128K | 4/5 |
| `mistralai/mistral-small-3.2:free` | Mistral | Fast, efficient | 32K | 4/5 |
| `deepseek/deepseek-chat:free` | DeepSeek | Coding, reasoning | 64K | 3/5 |
| `nvidia/llama-3.1-nemotron-70b:free` | NVIDIA | Strong reasoning | 128K | 4/5 |
| `qwen/qwen-3-235b-a22b:free` | Alibaba | Multilingual, coding | 128K | 3/5 |
| `microsoft/phi-4:free` | Microsoft | Small, efficient | 16K | 4/5 |
| `huggingfaceh4/zephyr-7b-beta:free` | Hugging Face | Lightweight | 32K | 3/5 |

### Model Availability Warning

> **`:free` models rotate.** Providers add and remove free access based on capacity. Always check the OpenRouter models page for current availability. A model that was free yesterday may not be free today.

---

## 4. Task-by-Task: Free Tier Model Recommendations

### 4.1 General Chat & Q&A

| Use Case | Best Free Model | Why | Daily Capacity (Free Plan) |
|---|---|---|---|
| **Casual chatbot** | `gemini-2.5-flash:free` | Best quality on free tier | 50 conversations |
| **High-volume FAQ** | `gemini-2.5-flash-lite:free` | Fastest, most reliable | 50 answers |
| **Multilingual chat** | `qwen/qwen-3:free` | Strong non-English | 50 conversations |
| **Offline-capable** | `llama-4-scout:free` | Open weights, self-hostable | 50 conversations |
| **Simple Q&A** | `mistral-small-3.2:free` | Fast, efficient | 50 answers |

### 4.2 Coding & Development

| Use Case | Best Free Model | Why | Notes |
|---|---|---|---|
| **Code completion** | `gemini-2.5-flash:free` | Strong coding benchmarks | 50 completions/day |
| **Debug small snippets** | `deepseek-chat:free` | Specialized for code | Can be slow |
| **Generate tests** | `gemini-2.5-flash:free` | Reliable output | 50 test files/day |
| **Code review** | `llama-4-maverick:free` | Good reasoning | 50 reviews/day |
| **Architecture advice** | `gemini-2.5-flash:free` | 1M context for large codebases | 50 queries/day |
| **Production IDE** | Not viable | 50/day too few | Need $10+ credits |

### 4.3 Agents & Automation

| Use Case | Best Free Model | Why | Architecture |
|---|---|---|---|
| **Simple tool agent** | `gemini-2.5-flash:free` | Tool use, 1M context | 50 agent runs/day |
| **Router/classifier** | `gemini-2.5-flash-lite:free` | Ultra-fast | 50 classifications/day |
| **Multi-step workflow** | `gemini-2.5-flash:free` | Reliable reasoning | Chain 2-3 steps max |
| **Complex agent** | Not viable | 50/day insufficient | Need $10+ credits |
| **Fallback agent** | `openrouter/free` router | Auto-selects best free | 50 runs/day |

### 4.4 RAG & Document Processing

| Use Case | Best Free Model | Why | Limit |
|---|---|---|---|
| **Small RAG (1-50 docs)** | `gemini-2.5-flash:free` | 1M context fits docs | 50 queries/day |
| **Large RAG (1000+ docs)** | `gemini-2.5-flash:free` | Long context reduces chunks | 50 queries/day |
| **Document Q&A** | `gemini-2.5-flash:free` | Direct long-context | 50 docs/day |
| **Embedding + RAG** | `gemini-2.5-flash:free` | Use external embeddings | 50 RAG queries/day |
| **Production RAG** | Not viable | 50/day too few | Need $10+ credits |

### 4.5 Reasoning & Analysis

| Use Case | Best Free Model | Why | Note |
|---|---|---|---|
| **Math problems** | `gemini-2.5-flash:free` | Good reasoning | 50 problems/day |
| **Logic puzzles** | `llama-4-maverick:free` | Strong reasoning | 50 puzzles/day |
| **Data analysis** | `gemini-2.5-flash:free` | 1M context for datasets | 50 analyses/day |
| **Scientific research** | `nvidia-nemotron-70b:free` | Strong STEM | 50 queries/day |
| **Deep reasoning** | `deepseek-chat:free` | Chain-of-thought | Can be slow |

### 4.6 Multimodal (Image/Vision)

| Use Case | Best Free Model | Why | Limit |
|---|---|---|---|
| **Image description** | `gemini-2.5-flash:free` | Native multimodal | 50 images/day |
| **Chart analysis** | `gemini-2.5-flash:free` | Visual understanding | 50 charts/day |
| **PDF analysis** | `gemini-2.5-flash:free` | 1M context for long PDFs | 50 PDFs/day |
| **Video understanding** | `gemini-2.5-flash:free` | Video input support | 50 videos/day |
| **Image generation** | Limited free | Few `:free` image models | Usually paid |

---

## 5. The `openrouter/free` Router

### 5.1 What Is It?

Instead of specifying a model, use the `openrouter/free` router. OpenRouter automatically picks the best available free model.

**Benefits:**
- Always routes to an available free model
- Automatic fallback if one free model is down
- Load balancing across free providers
- No need to track which `:free` models are currently active

**Drawbacks:**
- Non-deterministic — you don't know which model you'll get
- Quality varies based on current availability
- Harder to debug (unknown model version)
- Not suitable for reproducible research

### 5.2 When to Use `openrouter/free`

| Scenario | Recommendation |
|---|---|
| **Quick testing** | Use `openrouter/free` |
| **Learning/experimentation** | Use `openrouter/free` |
| **Production app** | Specify exact model |
| **Benchmarking** | Specify exact model |
| **Debugging** | Specify exact model |
| **High reliability** | Specify exact model + fallback |

---

## 6. Fallback Strategy: Free Tier's Secret Weapon

### 6.1 How Fallbacks Work on Free Tier

OpenRouter's strongest feature is **automatic fallback**. Even on free tier, if your primary model fails, it tries alternatives.

**Free Tier Fallback Chain Example:**

```python
models = [
    "google/gemini-2.5-flash:free",
    "meta-llama/llama-4-scout:free",
    "mistralai/mistral-small-3.2:free",
    "openrouter/free"
]
```

### 6.2 Fallback Rules on Free Tier

| Rule | Behavior |
|---|---|
| **Same provider fallback** | If Gemini fails, try another Google model |
| **Cross-provider fallback** | If Google fails, try Meta, then Mistral |
| **Free-only fallback** | Only routes to other `:free` models |
| **Error counting** | Failed attempts count toward your 50 RPD |
| **Timeout** | 30-second default, then fallback |

### 6.3 Best Free Tier Fallback Chains by Task

**General Chat:**
1. google/gemini-2.5-flash:free
2. meta-llama/llama-4-maverick:free
3. mistralai/mistral-small-3.2:free
4. openrouter/free

**Coding:**
1. google/gemini-2.5-flash:free
2. deepseek/deepseek-chat:free
3. meta-llama/llama-4-scout:free
4. openrouter/free

**Reasoning:**
1. google/gemini-2.5-flash:free
2. nvidia/llama-3.1-nemotron-70b:free
3. meta-llama/llama-4-maverick:free
4. openrouter/free

---

## 7. Free Tier Strategy: Maximizing 50 Requests/Day

### 7.1 The "50 Request Budget" Framework

```
Daily Allocation (Free Plan):
├── Critical (20 requests): Core functionality, user-facing
├── Development (20 requests): Testing, debugging, iteration
└── Experimental (10 requests): New models, features, exploration
```

### 7.2 Optimization Techniques

1. **Batch Multiple Tasks:**
   - Instead of: 5 separate requests (5 RPD)
   - Do: 1 batched request with all 5 questions (1 RPD)

2. **Use Long Context:**
   - Gemini 2.5 Flash free has 1M context
   - Fit multiple documents in one request
   - Ask multiple questions about same context

3. **Implement Caching:**
   - Cache identical prompts
   - Use conversation history efficiently
   - Don't re-ask similar questions

4. **Use `openrouter/free` for Exploration:**
   - Test new models without burning specific model quota
   - Discover which free models work best for your task

5. **Upgrade to $10 Credits When:**
   - You need 1000 RPD (20x more)
   - You want access to paid models
   - You're building something real

---

## 8. Free vs Paid: Complete Comparison

| Feature | Free Plan ($0) | Pay-as-you-go ($10+) | Enterprise |
|---|---|---|---|
| **Cost** | $0 | $10 min + usage | Custom |
| **Free Model RPD** | 50 | 1000 | Custom |
| **Paid Model Access** | No | Yes | Yes |
| **Rate Limits** | 20 RPM | 20 RPM (free) / None (paid) | Custom |
| **Fallbacks** | Yes | Yes | Yes + Custom |
| **Priority** | Lowest | Medium | Highest |
| **Support** | Community | Email | Dedicated |
| **SSO** | No | No | Yes |
| **Regional Routing** | No | Yes | Yes |
| **App Leaderboards** | Yes | Yes | Yes |

---

## 9. Code Examples: Free Tier Usage

### 9.1 Basic Free Tier Request with Fallback

```python
import requests
import json

OPENROUTER_API_KEY = "YOUR_FREE_API_KEY"

MODELS_TO_TRY = [
    "google/gemini-2.5-flash:free",
    "meta-llama/llama-4-scout:free",
    "mistralai/mistral-small-3.2:free",
    "openrouter/free"
]

def ask_with_fallback(prompt, models=MODELS_TO_TRY):
    for model in models:
        try:
            response = requests.post(
                url="https://openrouter.ai/api/v1/chat/completions",
                headers={
                    "Authorization": f"Bearer {OPENROUTER_API_KEY}",
                    "HTTP-Referer": "https://your-app.com",
                    "X-Title": "My Free Tier App"
                },
                data=json.dumps({
                    "model": model,
                    "messages": [{"role": "user", "content": prompt}],
                    "max_tokens": 1000
                }),
                timeout=30
            )

            if response.status_code == 200:
                data = response.json()
                print(f"Success with {model}")
                return data['choices'][0]['message']['content']
            else:
                print(f"Failed with {model}: {response.status_code}")
                continue

        except Exception as e:
            print(f"Error with {model}: {e}")
            continue

    return "All models failed. Check rate limits or try later."

# Usage
answer = ask_with_fallback("Explain quantum computing in simple terms")
print(answer)
```

### 9.2 Rate Limit Tracker for Free Tier

```python
import time
from datetime import datetime, timedelta

class OpenRouterFreeTracker:
    def __init__(self, rpd_limit=50, rpm_limit=20):
        self.rpd_limit = rpd_limit
        self.rpm_limit = rpm_limit
        self.daily_history = []
        self.minute_history = []

    def can_request(self):
        now = datetime.now()
        day_ago = now - timedelta(days=1)
        minute_ago = now - timedelta(minutes=1)

        self.daily_history = [t for t in self.daily_history if t > day_ago]
        self.minute_history = [t for t in self.minute_history if t > minute_ago]

        if len(self.daily_history) >= self.rpd_limit:
            return False, "RPD limit exceeded"
        if len(self.minute_history) >= self.rpm_limit:
            return False, "RPM limit exceeded"

        return True, "OK"

    def record_request(self):
        now = datetime.now()
        self.daily_history.append(now)
        self.minute_history.append(now)

    def get_status(self):
        can_req, reason = self.can_request()
        return {
            'daily_used': len(self.daily_history),
            'daily_remaining': self.rpd_limit - len(self.daily_history),
            'minute_used': len(self.minute_history),
            'minute_remaining': self.rpm_limit - len(self.minute_history),
            'can_request': can_req,
            'status': 'HEALTHY' if len(self.daily_history) < 35 else 'WARNING' if len(self.daily_history) < 45 else 'CRITICAL'
        }

# Usage
tracker = OpenRouterFreeTracker()
can_req, reason = tracker.can_request()
if can_req:
    tracker.record_request()
    print(f"Request sent! Status: {tracker.get_status()}")
else:
    print(f"Cannot request: {reason}")
```

### 9.3 Smart Model Selector for Free Tier

```python
def select_openrouter_free_model(task_type, daily_used, prefer_reliability=True):
    remaining = 50 - daily_used

    if remaining < 5:
        return "openrouter/free"

    reliable_models = {
        'chat': 'google/gemini-2.5-flash:free',
        'code': 'google/gemini-2.5-flash:free',
        'reasoning': 'nvidia/llama-3.1-nemotron-70b:free',
        'multimodal': 'google/gemini-2.5-flash:free',
        'fast': 'google/gemini-2.5-flash-lite:free',
    }

    capability_models = {
        'chat': 'meta-llama/llama-4-maverick:free',
        'code': 'deepseek/deepseek-chat:free',
        'reasoning': 'deepseek/deepseek-chat:free',
        'multimodal': 'google/gemini-2.5-flash:free',
        'fast': 'mistralai/mistral-small-3.2:free',
    }

    if prefer_reliability or remaining < 15:
        return reliable_models.get(task_type, 'google/gemini-2.5-flash:free')
    else:
        return capability_models.get(task_type, 'google/gemini-2.5-flash:free')

# Example usage
model = select_openrouter_free_model('code', daily_used=20, prefer_reliability=True)
print(f"Selected: {model} (20/50 used, reliability preferred)")
```

---

## 10. Migration Path: Free → Paid

### Phase 1: Free Plan ($0)
- 50 requests/day for learning and testing
- Use `:free` models only
- Discover which models work for your task

### Phase 2: Pay-as-you-go ($10+ credits)
- 1000 free requests/day on `:free` models
- Access to paid models (GPT-4, Claude, etc.)
- No limits on paid models (just pay per token)
- Best for: Prototypes, small production apps

### Phase 3: Enterprise
- Custom rate limits
- SSO, dedicated support
- Regional routing
- Volume discounts

---

## 11. Quick Reference: Free Tier Cheat Sheet

```
OPENROUTER FREE TIER CHEAT SHEET (June 2026)

FREE PLAN ($0):
• 50 requests per day (hard limit)
• 20 requests per minute (burst limit)
• :free models only
• Fallbacks enabled

PAY-AS-YOU-GO ($10+ credits):
• 1000 free requests/day on :free models
• Access to ALL models (paid per token)
• No limits on paid models

TOP FREE MODELS:
• General purpose → google/gemini-2.5-flash:free
• High volume → google/gemini-2.5-flash-lite:free
• Coding → deepseek/deepseek-chat:free
• Reasoning → nvidia/llama-3.1-nemotron-70b:free
• Open/self-hostable → meta-llama/llama-4-scout:free
• Multilingual → qwen/qwen-3-235b-a22b:free

FALLBACK CHAINS:
• Chat: gemini-2.5-flash → llama-4-maverick → mistral-small → openrouter/free
• Code: gemini-2.5-flash → deepseek-chat → llama-4-scout → openrouter/free
• Reasoning: gemini-2.5-flash → nvidia-nemotron → llama-4-maverick → openrouter/free

UPGRADE SIGNALS:
• Hitting 50 RPD consistently
• Need paid models (GPT-4, Claude, Gemini Pro)
• Building production app
• Need higher reliability / SLA
```

---

## 12. Summary: The Free Tier Winner

**For free tier users, OpenRouter's value is unmatched variety.**

You get:
- Access to 10+ high-quality free models
- Automatic fallback (reliability)
- 1M context via Gemini Flash free
- Open models (Llama, Mistral) for self-hosting path
- Single API for all models
- Zero cost to start

**Best Strategy:**
- **Start with `google/gemini-2.5-flash:free`** — it's the most capable and reliable free model
- **Use fallback chains** for production reliability
- **Batch requests** to stretch 50 RPD
- **Upgrade to $10 credits** when you need 1000 RPD or paid models
- **Use `openrouter/free`** only for exploration, not production

**The OpenRouter Advantage:** Unlike single-provider free tiers, OpenRouter lets you **compare models for free** — test Gemini vs Llama vs DeepSeek on your actual tasks before committing to any paid plan.
