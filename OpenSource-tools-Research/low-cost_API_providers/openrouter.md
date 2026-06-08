# OpenRouter

## 1.  what OpenRouter is

OpenRouter is a unified API layer for LLMs that gives access to many models and providers through one OpenAI-compatible interface.

At a high level, OpenRouter is useful for:
- Accessing many AI models with one API.
- Switching models without rewriting your app.
- Using fallback models when one provider fails.
- Comparing cost, quality, and speed across models.
- Starting with free models and moving to paid models later.

---

## 2. Core idea

The main idea is:

> One API key, one API format, many models.

OpenRouter acts as a routing and compatibility layer between your app and the actual model providers.

This is helpful when:
- You want to avoid vendor lock-in.
- You want to benchmark multiple models.
- You want simpler billing and model management.
- You want reliable production fallbacks.

---

## 3. Core features

### 3.1 Large model catalog
OpenRouter gives access to many model types:
- Chat models
- Reasoning models
- Coding models
- Vision-capable models
- Long-context models
- Free model variants

### 3.2 OpenAI-compatible API
Many existing tools and codebases can use OpenRouter by changing:
- base URL
- API key
- model name

### 3.3 Credits and billing
You can add credits and use them across many models and providers from one account.

### 3.4 Free models
OpenRouter supports free models through:
- model IDs ending in `:free`
- the `openrouter/free` router

### 3.5 Routing and fallback
You can define a primary model and fallback models so your app keeps working if the main one fails.

---

## 4. Routing and fallbacks

This is one of OpenRouter’s strongest features.

Why it matters:
- Providers can fail.
- Models can be rate-limited.
- Some requests may be rejected.
- Context errors can happen.

With OpenRouter, you can provide a list of models in priority order.
If the first model fails, OpenRouter tries the next one automatically.

Best for:
- customer support bots
- internal AI tools
- automation systems
- agents that must stay available

---

## 5. Free tier and limits

OpenRouter supports free model usage, but with limits.

For `:free` model variants:
- Up to 20 requests per minute
- 50 free-model requests per day if you purchased less than 10 credits
- 1000 free-model requests per day if you purchased at least 10 credits

Important:
- Free does not mean unlimited
- Negative balance can cause errors even on free models

Best use of free tier:
- learning
- prototypes
- demos
- small internal tools

---

## 6. Pricing

OpenRouter pricing depends on the model and usage.

You generally pay based on:
- the selected model
- input/output tokens
- the model actually used if routing is enabled

This makes OpenRouter flexible, but you should still monitor token usage and fallback costs in production.

---

## 7. Best use cases

### General chat
Good for assistants, support bots, and productivity tools.

### Coding
Good for benchmarking coding models for debugging, refactoring, tests, and code explanation.

### Agents
Very strong for agent workflows because you can combine routing, fallbacks, and different models for different steps.

### RAG
Useful as the answer-generation layer in document chat and knowledge assistants.

### Budget-aware development
Very useful for students, solo builders, hackathons, and prototypes.

---

## 8. When not to use OpenRouter

OpenRouter is less ideal when:
- you need the lowest-latency inference possible
- you want a full open-source ML ecosystem
- you need direct first-party provider control only
- you want one-provider-specific features with no abstraction layer

---

## 9. Model strategy

A strong practical setup is:
- cheap/free model for routing or classification
- better model for user-facing answers
- premium model for difficult tasks
- fallback model for reliability

This often gives a better cost-quality balance than using one expensive model for everything.

---

## 10. Best fit summary

Use OpenRouter when your top priority is:
- flexibility
- model choice
- easy experimentation
- routing
- fallback reliability

Mental model:
- Groq = speed
- Hugging Face = ecosystem
- OpenRouter = access + routing