# Deep Dive: Google AI / Gemini API Models — Free Tier Complete Guide (2026)

> **Last Updated:** June 2026 | **Status:** Active — Pro models removed from free tier April 2026

---

## 1. Free Tier Overview: What Changed in 2026

Google's free tier underwent a **major restriction in April 2026**. Key changes:
- **Pro models (2.5 Pro, 3.1 Pro) are now PAID-ONLY** — no free API quota
- Flash models retain free tier but with **reduced daily quotas**
- **2.0 Flash/Flash-Lite deprecated** (shutdown June 1, 2026) — migrate immediately
- New projects start on **Standard Free Tier** (no Cloud Billing required)

### Current Free Tier Status by Model (June 2026)

| Model | Free Tier? | Rate Limit | TPM Limit | Best For |
|---|---|---|---|---|
| **Gemini 2.5 Flash** | ✅ **FREE** | 1,500 RPD | 1,000,000 TPM | General chat, agents, coding |
| **Gemini 2.5 Flash-Lite** | ✅ **FREE** | 1,500 RPD | 1,000,000 TPM | High-volume, cost-sensitive |
| **Gemini 3 Flash** | ✅ **FREE** | Reduced (varies by region) | Varies | Advanced assistants, multimodal |
| **Gemini 3.1 Flash-Lite** | ✅ **FREE** | Reduced (varies by region) | Varies | Fastest, cheapest frontier |
| **Gemini 3.1 Flash Live** | ✅ **FREE** (Preview) | AI Studio only | N/A | Real-time voice agents |
| **Gemini 2.5 Pro** | ⚠️ **RESTRICTED** | 50 RPD only | Very limited | Complex reasoning (barely usable free) |
| **Gemini 3.1 Pro** | ❌ **PAID ONLY** | N/A | N/A | No free API quota |
| **gemini-embedding-001** | ✅ **FREE** | Light usage | Included | RAG, semantic search |
| **Gemini 2.5 Flash Image** | ✅ **FREE** (AI Studio) | Dynamic limits | N/A | Image generation/editing |

> **RPD** = Requests Per Day | **TPM** = Tokens Per Minute | **RPM** = Requests Per Minute

---

## 2. Model-by-Model Free Tier Deep Dive

### 2.1 Gemini 2.5 Flash — The Free Tier King

**Free Tier Limits:**
- **1,500 requests per day (RPD)**
- **1,000,000 tokens per minute (TPM)**
- **No credit card required**

**What You Get:**
- Full multimodal (text, image, audio, video input)
- 1M token context window
- Reasoning capabilities with controllable thinking budgets
- Tool use / function calling
- JSON mode

**Best Free Tasks:**
| Task | Why 2.5 Flash Free? | Practical Limit |
|---|---|---|
| **Chatbots & Assistants** | Fast, cheap, good reasoning | ~1,500 user interactions/day |
| **RAG Answer Generation** | 1M context fits large docs | 1,500 queries/day for doc Q&A |
| **Code Completion** | Strong coding benchmarks | Good for IDE autocomplete |
| **Classification/Routing** | Excellent price-performance | Route 1,500 requests/day |
| **Summarization** | Long context + fast | Summarize 1,500 articles/day |
| **Translation** | Multilingual support | 1,500 translation requests/day |
| **Light Agents** | Tool use + reasoning | Simple multi-step workflows |

**When You Hit Limits:**
- 1,500 RPD = ~62 requests/hour average
- For production: upgrade to paid ($0.30/$2.50 per 1M tokens)
- Batch API gives 50% discount for async workloads

---

### 2.2 Gemini 2.5 Flash-Lite — The Volume Beast

**Free Tier Limits:**
- **1,500 RPD** (shared quota with 2.5 Flash in same project)
- **1,000,000 TPM**

**What You Get:**
- Most cost-efficient model in Gemini family
- Optimized for massive scale
- Slightly lower quality than 2.5 Flash but 3x cheaper when paid

**Best Free Tasks:**
| Task | Why Flash-Lite? | Volume Potential |
|---|---|---|
| **High-Volume Classification** | Dirt cheap, fast | Tag 1,500 items/day |
| **Notification Generation** | Simple text output | Generate 1,500 alerts/day |
| **Data Extraction** | Structured output | Parse 1,500 documents/day |
| **Simple Q&A** | Direct answers | 1,500 basic queries/day |
| **Content Moderation** | Fast filtering | Moderate 1,500 posts/day |
| **Translation (Bulk)** | Massive throughput | Batch translate 1,500 texts/day |

**Limitation:** Less capable for complex reasoning or creative writing. Use 2.5 Flash for those.

---

### 2.3 Gemini 3 Flash / 3.1 Flash-Lite — Frontier Free Access

**Free Tier Limits:**
- **Reduced quotas** (varies by region, typically ~500-1,000 RPD)
- **Dynamic allocation** based on demand

**What You Get:**
- Frontier-class performance rivaling larger models
- Better reasoning than 2.5 series
- Faster response times
- Multimodal understanding

**Best Free Tasks:**
| Task | Why 3.x Flash? | Note |
|---|---|---|
| **Advanced Coding** | Better than 2.5 on coding benchmarks | Limited daily quota |
| **Complex Agents** | Stronger tool use | Plan for paid upgrade |
| **Multimodal Analysis** | Better image/video understanding | Preview status |
| **Math/Science** | Improved reasoning | Use sparingly due to limits |

**Warning:** Quotas are lower and more variable than 2.5 series. Monitor AI Studio dashboard.

---

### 2.4 Gemini 2.5 Pro — Barely Free (50 RPD)

**Free Tier Limits:**
- **50 requests per day ONLY**
- **Heavily restricted**

**Practical Use:**
- This is essentially a **trial tier**, not a usable free tier
- 50 requests = ~2 per hour
- **Best for:** Testing complex reasoning before paying, comparing against Flash

**When to Use the 50 RPD:**
| Task | Strategy | Why |
|---|---|---|
| **Complex Reasoning Test** | Run 1-2 hard problems | Verify if Pro is worth paying |
| **Code Architecture** | 1-2 big design questions | Evaluate before subscription |
| **Long-Context RAG Test** | Test 1M context | See if context helps your use case |
| **Agent Prototype** | Build proof-of-concept | Then migrate to 2.5 Flash for scale |

**Paid Upgrade:** $1.25-$2.50 input / $10-$15 output per 1M tokens

---

### 2.5 Gemini 3.1 Pro — NO FREE TIER

**Status:** ❌ **Paid from first token**

**Pricing:** $2-$4 per 1M input / $12-$18 per 1M output (context-tiered)

**Access:**
- AI Studio UI: Free to try with **dynamic daily limits** (~10 requests/day when demand is high)
- API: **Must link billing account**

**Strategy for Free Users:**
- Use AI Studio for **occasional testing**
- For API: Budget $20-50/month for light usage
- Alternative: Use 2.5 Flash free tier + upgrade only for critical tasks

---

### 2.6 Embedding Models — Free for Light RAG

**Free Tier:**
- `gemini-embedding-001`: Included in free tier for light usage
- `gemini-embedding-2`: $0.20 per 1M tokens (paid only)

**Best Free Tasks:**
| Task | Volume | Limitation |
|---|---|---|
| **Small RAG (1-100 docs)** | Embed 1,000 chunks/day | Free tier covers light usage |
| **Semantic Search** | 1,500 queries/day | Use with 2.5 Flash for answers |
| **Classification** | Cluster 1,500 items/day | Good for prototyping |
| **Recommendation** | Light user base | Scale to paid for production |

---

## 3. Free Tier Rate Limits: Complete Reference

### Hard Limits (Enforced)

| Limit Type | 2.5 Flash/Flash-Lite | 2.5 Pro | 3.x Flash | Embedding |
|---|---|---|---|---|
| **Requests Per Day (RPD)** | 1,500 | 50 | 500-1,000 | Shared with project |
| **Tokens Per Minute (TPM)** | 1,000,000 | 100,000 | 500,000 | 100,000 |
| **Requests Per Minute (RPM)** | ~60 | ~2 | ~20-40 | ~60 |
| **Context Window** | 1M tokens | 1M tokens | 1M+ tokens | 8,192 tokens |
| **Max Output Tokens** | 8,192 | 8,192 | 8,192 | N/A |

### Soft Limits (Dynamic)

- **Burst pressure:** Short spikes may trigger 429 errors even under RPD
- **Model availability:** Free tier deprioritized during high demand
- **Regional variation:** Limits vary by Google Cloud region
- **Project-level:** All keys in one project share the same quota

### Error Codes & What They Mean

| Error | Code | Meaning | Fix |
|---|---|---|---|
| **429 Too Many Requests** | Rate limit hit | Exceeded RPD/RPM/TPM | Wait for reset, upgrade to paid |
| **429 Resource Exhausted** | Burst limit | Too many requests in short window | Implement exponential backoff |
| **403 Billing Disabled** | Model not free | Trying to use Pro without billing | Switch to Flash model or add billing |
| **400 Invalid Argument** | Context too long | Exceeded token limit | Truncate input, use chunking |

---

## 4. Task-by-Task: Which Free Model to Use

### 4.1 General Chat / Q&A / Summarization

| Use Case | Best Free Model | Why | Daily Capacity |
|---|---|---|---|
| Casual chatbot | **2.5 Flash** | Fast, good quality | 1,500 conversations |
| High-volume FAQ | **2.5 Flash-Lite** | Cheapest, sufficient | 1,500 answers |
| Long document summary | **2.5 Flash** | 1M context | 1,500 docs |
| News digest | **2.5 Flash** | Real-time capable | 1,500 digests |

### 4.2 Coding & Development

| Use Case | Best Free Model | Why | Strategy |
|---|---|---|---|
| Code completion | **2.5 Flash** | Good benchmarks, fast | Use in IDE |
| Debug small snippets | **2.5 Flash** | Accurate, fast | 1,500 debugs/day |
| Complex architecture | **2.5 Pro (50 RPD)** | Better reasoning | Use sparingly, test only |
| Code review | **2.5 Flash** | Sufficient for most | Batch reviews |
| Generate tests | **2.5 Flash** | Good coverage | 1,500 test files/day |
| **Advanced coding** | **3 Flash** | Better than 2.5 | Limited quota, plan upgrade |

### 4.3 Agents & Automation

| Use Case | Best Free Model | Why | Architecture |
|---|---|---|---|
| Simple tool-using agent | **2.5 Flash** | Function calling, fast | 1,500 agent runs/day |
| Multi-step workflow | **2.5 Flash** | Reliable reasoning | Chain 3-5 steps |
| Router/classifier agent | **2.5 Flash-Lite** | Ultra-fast, cheap | Route to other services |
| Complex agent prototype | **2.5 Pro (50 RPD)** | Test sophisticated logic | Then rebuild with 2.5 Flash |
| Voice agent | **3.1 Flash Live** | Real-time audio | AI Studio preview only |

### 4.4 RAG & Document Processing

| Use Case | Best Free Model | Why | Limit |
|---|---|---|---|
| Small RAG (1-100 docs) | **2.5 Flash + embedding** | 1M context, free embed | 1,500 queries/day |
| Large RAG (1000+ docs) | **2.5 Flash** | Long context reduces need for chunks | Plan paid for embed volume |
| Document Q&A | **2.5 Flash** | Direct long-context | 1,500 docs/day |
| Multi-document synthesis | **2.5 Flash** | Fits many docs in context | 1,500 syntheses/day |

### 4.5 Multimodal (Image/Audio/Video)

| Use Case | Best Free Model | Why | Limit |
|---|---|---|---|
| Image description | **2.5 Flash** | Native multimodal | 1,500 images/day |
| Video analysis | **2.5 Flash** | 1M context fits video | 1,500 videos/day |
| Image generation | **2.5 Flash Image** | AI Studio free | Dynamic limits |
| Audio transcription | **2.5 Flash** | Audio input support | 1,500 files/day |
| Real-time voice | **3.1 Flash Live** | Audio-to-audio | AI Studio preview |

### 4.6 Reasoning & Complex Tasks

| Use Case | Best Free Model | Why | Warning |
|---|---|---|---|
| Math problems | **2.5 Flash** | Good enough for most | Hard problems → 2.5 Pro (paid) |
| Logic puzzles | **2.5 Flash** | Controllable thinking | Enable thinking budget |
| Scientific analysis | **2.5 Pro (50 RPD)** | Better accuracy | Only 50/day |
| Multi-hop reasoning | **2.5 Flash** | Sufficient for 80% | Complex cases need Pro |
| Planning/scheduling | **2.5 Flash** | Structured output | 1,500 plans/day |

---

## 5. Free Tier Strategy: Maximizing Your 1,500 RPD

### The "1,500 RPD Budget" Framework

You have 1,500 requests/day on Flash/Flash-Lite. Here's how to allocate:

```
Tier 1 - Critical (60% = 900 RPD): User-facing chat, core agent logic
Tier 2 - Important (30% = 450 RPD): Background tasks, summaries, notifications  
Tier 3 - Nice-to-have (10% = 150 RPD): Analytics, experiments, testing
```

### Optimization Techniques

1. **Batch Requests:** Combine multiple tasks into one prompt
   - Instead of: 10 separate classification calls (10 RPD)
   - Do: 1 call with 10 items in a list (1 RPD)

2. **Use Flash-Lite for Simple Tasks:** Save 2.5 Flash quota for complex work
   - Flash-Lite: classification, extraction, simple Q&A
   - 2.5 Flash: reasoning, coding, creative tasks

3. **Cache Repeated Context:** Use context caching (paid feature) or keep conversation history minimal

4. **Implement Request Deduplication:** Don't re-process identical inputs

5. **Time-shift Non-Urgent Work:** Use Batch API (50% off) for async tasks when you upgrade

### When to Upgrade to Paid

| Signal | Action |
|---|---|
| Hitting 1,500 RPD by noon | Upgrade immediately |
| Need 2.5 Pro for quality | Budget $50-200/month |
| Need 3.1 Pro capabilities | Budget $200-500/month |
| Embedding volume > 1M tokens/day | Pay $0.15-0.20 per 1M |
| Building production app | Mandatory paid for reliability |

---

## 6. Free vs Paid: Complete Comparison

| Feature | Free Tier | Paid Tier |
|---|---|---|
| **Cost** | $0 | Per-token billing |
| **Models** | Flash/Flash-Lite only | All models including Pro |
| **Rate Limits** | 1,500 RPD (Flash) | Custom / much higher |
| **TPM** | 1M | 10M+ |
| **Reliability** | Best effort | SLA guaranteed |
| **Support** | Community | Enterprise support |
| **Data handling** | May be used for improvement | Explicit data protection |
| **Batch API** | ❌ | ✅ (50% discount) |
| **Context Caching** | ❌ | ✅ |
| **Grounding (Search)** | 500 RPD free | 1,500 RPD + paid overage |

---

## 7. Code Examples: Free Tier Usage

### 7.1 Check Your Rate Limit Status (Python)

```python
import google.generativeai as genai
import time

genai.configure(api_key="YOUR_FREE_API_KEY")

# Check which models are available on free tier
for model in genai.list_models():
    if 'generateContent' in model.supported_generation_methods:
        print(f"Model: {model.name}")
        print(f"  Limits: {model.input_token_limit} input / {model.output_token_limit} output")

# Implement rate limit tracking
class FreeTierTracker:
    def __init__(self, rpd_limit=1500):
        self.rpd_limit = rpd_limit
        self.request_count = 0
        self.reset_time = time.time() + 86400  # 24 hours

    def can_request(self):
        if time.time() > self.reset_time:
            self.request_count = 0
            self.reset_time = time.time() + 86400
        return self.request_count < self.rpd_limit

    def track_request(self):
        self.request_count += 1
        remaining = self.rpd_limit - self.request_count
        print(f"Requests used: {self.request_count}/1500 | Remaining: {remaining}")
        return remaining

# Usage
tracker = FreeTierTracker()
model = genai.GenerativeModel("gemini-2.5-flash")

if tracker.can_request():
    response = model.generate_content("Explain RAG")
    tracker.track_request()
    print(response.text)
else:
    print("Rate limit exceeded. Wait for reset or upgrade to paid.")
```

### 7.2 Smart Model Selection Based on Task Complexity

```python
def select_free_model(task_complexity: str, remaining_rpd: int) -> str:
    if remaining_rpd < 100:
        return "gemini-2.5-flash-lite"

    if task_complexity == 'simple':
        return "gemini-2.5-flash-lite"
    elif task_complexity == 'medium':
        return "gemini-2.5-flash"
    elif task_complexity == 'complex':
        if remaining_rpd > 500:
            return "gemini-2.5-flash"
        else:
            return "gemini-2.5-flash-lite"

    return "gemini-2.5-flash"

# Example usage
remaining = 800
model_name = select_free_model('medium', remaining)
print(f"Using {model_name} for medium complexity task")
```

### 7.3 Free Tier RAG Pipeline

```python
import google.generativeai as genai
from typing import List

genai.configure(api_key="YOUR_FREE_API_KEY")

class FreeTierRAG:
    def __init__(self):
        self.embed_model = "gemini-embedding-001"
        self.chat_model = "gemini-2.5-flash"
        self.rpd_used = 0
        self.RPD_LIMIT = 1500

    def embed_documents(self, chunks: List[str]) -> List[List[float]]:
        result = genai.embed_content(
            model=self.embed_model,
            content=chunks,
            task_type="retrieval_document"
        )
        return result['embedding']

    def answer_question(self, question: str, context: str) -> str:
        if self.rpd_used >= self.RPD_LIMIT:
            return "Error: Daily free quota exceeded. Upgrade to paid tier."

        model = genai.GenerativeModel(self.chat_model)
        prompt = f"Context: {context}

Question: {question}

Answer based on context only."

        response = model.generate_content(prompt)
        self.rpd_used += 1
        return response.text

    def get_status(self):
        return {
            'rpd_used': self.rpd_used,
            'rpd_remaining': self.RPD_LIMIT - self.rpd_used,
            'percentage_used': (self.rpd_used / self.RPD_LIMIT) * 100
        }

# Usage
rag = FreeTierRAG()
docs = ["Doc 1 content...", "Doc 2 content...", "Doc 3 content..."]
embeddings = rag.embed_documents(docs)
answer = rag.answer_question("What is RAG?", "Retrieval Augmented Generation is...")
print(rag.get_status())
```

---

## 8. Migration Path: Free → Paid

**Phase 1: Flash Power User ($0-30/month)**
- Still use 2.5 Flash/Flash-Lite free tier
- Add billing for 2.5 Pro when needed (50 RPD isn't enough)
- Cost: ~$30/month for mixed usage

**Phase 2: Pro User ($50-200/month)**
- Regular 2.5 Pro usage for complex tasks
- Flash for high-volume tasks
- Embedding paid tier for RAG

**Phase 3: Enterprise ($500+/month)**
- 3.1 Pro for frontier tasks
- Batch API for 50% savings
- Context caching for repeated queries
- Custom rate limits

---

## 9. Quick Reference: Free Tier Cheat Sheet

```
GEMINI FREE TIER CHEAT SHEET (June 2026)

✅ FREE: 2.5 Flash, 2.5 Flash-Lite, 3 Flash,
         3.1 Flash-Lite, Embedding-001, Flash Image
⚠️  RESTRICTED: 2.5 Pro (50 RPD only)
❌ PAID ONLY: 3.1 Pro, 3.5 Flash, Embedding-2

DAILY BUDGET: 1,500 RPD (Flash/Flash-Lite)
ALLOCATE: 60% critical / 30% important / 10% experimental

BEST FREE MODELS BY TASK:
• Chat/Summarize/RAG → 2.5 Flash
• High-volume/Classification → 2.5 Flash-Lite
• Advanced coding → 3 Flash (limited quota)
• Complex reasoning test → 2.5 Pro (50/day only)
• Image generation → 2.5 Flash Image (AI Studio)
• Voice real-time → 3.1 Flash Live (preview)

UPGRADE SIGNALS:
• Hitting 1,500 RPD before end of day
• Need Pro model quality
• Building production app
• Need SLA/reliability guarantees
```

---

## 10. Summary: The Free Tier Winner

**For 95% of free tier users, Gemini 2.5 Flash is the single best choice.**

It offers:
- ✅ 1,500 RPD (usable daily volume)
- ✅ 1M context window
- ✅ Strong reasoning and coding
- ✅ Multimodal input
- ✅ Tool use / function calling
- ✅ Zero cost

**Use 2.5 Flash-Lite** when you need maximum volume and task complexity is low.

**Use 2.5 Pro (50 RPD)** only for testing complex tasks before paying.

**Avoid 3.1 Pro** unless you have a paid budget — it has zero free API quota.
