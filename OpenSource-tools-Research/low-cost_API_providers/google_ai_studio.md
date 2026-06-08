# Deep Dive: Google AI / Gemini API Models (with Free‑Tier )

## 1. Big picture: what “Google AI models” means

Google exposes its models mainly via the **Gemini API (Google AI for Developers)** and **Vertex AI on Google Cloud**.
The current lineup is built around the **Gemini 2.x / 3.x families**, plus a dedicated **embedding model** and specialized image/audio models.

At a high level you get:

- **General + reasoning + coding models** (Pro / Flash families).
- **Fast, cheap “Flash / Flash‑Lite” models** for high‑volume tasks.
- **Realtime + audio + TTS models** for interactive agents.
- **Image generation / editing models**.
- **Embedding models** for search / RAG.

Pricing and free usage depend on the model and whether you use the **Free Tier** or link a **paid billing account**.

---

## 2. Core Gemini text / multimodal model families

### 2.1 Gemini 3.x: latest frontier family

From the official models docs:

- **Gemini 3.1 Pro**
  - “Advanced intelligence, complex problem‑solving, powerful agentic and coding capabilities.”
  - 1M‑token context, reasoning‑first design, optimized for complex multimodal tasks and sophisticated agents.
  - Great for: heavy agentic workflows, complex codebases, long‑context RAG, high‑stakes reasoning.

- **Gemini 3.5 Flash**
  - “Most intelligent model for agentic workflows” with performance rivaling large flagship models, but at Flash‑style speed.
  - Benchmarks from DeepMind show strong performance on **agentic coding benchmarks** while staying fast.
  - Great for: production‑grade agents, coding assistants, tool‑using systems where latency also matters.

- **Gemini 3 Flash**
  - “Frontier‑class performance rivaling larger models at a fraction of the cost.”
  - Designed for complex multimodal understanding and challenging agentic problems, with strong coding and reasoning.
  - Great for: advanced assistants, multimodal agents, complex planning where Flash‑series cost/latency is important.

- **Gemini 3.1 Flash Live (preview)**
  - High‑quality, low‑latency **audio‑to‑audio** model for real‑time dialogue and voice‑first applications.
  - Great for: live voice agents, call‑center assistants, real‑time conversational UIs.

- **Gemini 3.1 Flash Image / 3 Pro Image (preview)**
  - For high‑fidelity image generation and editing with reasoning‑aware composition and multi‑turn editing.
  - Great for: production‑quality image workflows, complex prompts, multi‑image fusion, character consistency.

**Free vs paid:**
- Gemini 3.x models are available via Gemini API and Vertex AI; Pro and 3.5 Flash are considered **frontier** and pricing is on the higher end.
- For Gemini 3 Pro, external analyses note **no standing free API quota**; you can experiment in AI Studio’s UI, but API calls are billed from first token.

---

### 2.2 Gemini 2.5: current “workhorse” family

Per the models docs and blog:

- **Gemini 2.5 Pro**
  - “Most advanced model for complex tasks,” with deep reasoning, coding capabilities, and 1M‑token context.
  - Designed for complex agentic workflows, multimodal reasoning, and enterprise‑scale use cases.
  - Great for: complex enterprise agents, multi‑step tools, long‑context RAG, sophisticated workflows.

- **Gemini 2.5 Flash**
  - “Best price‑performance” model for low‑latency, high‑volume tasks that still require reasoning.
  - Balanced intelligence and latency, with **controllable thinking budgets**.
  - Great for: general chat, summarization, classification, routing, RAG, lighter agents at scale.

- **Gemini 2.5 Flash‑Lite**
  - Optimized for **massive scale** and cost‑sensitive workloads; “our most cost‑efficient model yet.”
  - Ideal for classification, translation, intelligent routing, and other high‑volume tasks where cost trumps peak IQ.

- **Gemini 2.5 Flash Live / Flash TTS (preview)**
  - Live: real‑time audio streaming, designed for low‑latency conversational agents with natural speech.
  - TTS: controllable text‑to‑speech with control over style, pacing, and quality for podcasts/audiobooks.

- **Gemini 2.5 Flash Image**
  - State‑of‑the‑art image generation and editing with conversational editing and multi‑image fusion.

**Free vs paid (2.5 family):**

- **Gemini API Free Tier**:
  - New projects start on a **Free** usage tier that allows access to **selected 2.5 and 2.0 models** with free tokens until you hit model‑specific free‑tier rate limits.
  - External breakdowns note that 2.5 Flash and 2.5 Flash‑Lite are explicitly included among the models with free input/output tokens under the Standard Free Tier (no Cloud Billing) for low‑volume dev/testing.
- Once you link a **paid API key** (billing account), usage for these models becomes billable per token, based on the official pricing table.

---

### 2.3 Gemini 2.0 Flash & Flash‑Lite

Google’s blog describes the Gemini 2.0 family:

- **Gemini 2.0 Flash**
  - Production‑ready Flash model with higher rate limits, stronger performance, and simplified pricing, compared to 1.5 Flash.
  - Cost can be lower than 1.5 Flash for mixed context workloads while delivering better performance.

- **Gemini 2.0 Flash‑Lite**
  - “Most cost‑efficient model yet,” optimized for large‑scale text output.
  - Great when you need very cheap, fast responses at huge volume (notifications, routing, simple Q&A).

These are essentially **older but still supported Flash models**; for new work, 2.5 Flash / Flash‑Lite and 3.x Flash family are usually preferable.

---

## 3. Embedding models

Google provides **Gemini Embedding** models via the Gemini API.

- **`gemini-embedding-001`**
  - First Gemini embedding text model, now generally available in the API and Vertex AI.
  - Designed for semantic search, classification, clustering, and typical RAG use cases with multilingual support.
  - Official pricing: around **0.15 USD per 1M input tokens** in early releases.

Legacy embedding models (`text-embedding-004`, `text-embedding-005`) have been or are being deprecated, and integrations are migrating to `gemini-embedding-001`.

**Free vs paid:**
- `gemini-embedding-001` is included in Free Tier access for light usage, with paid pricing for higher volume via standard Gemini API pricing.

---

## 4. What model to use for which task (and free‑tier status)

> Note: exact free‑tier quotas and per‑day limits can change and may be “dynamic”; always double‑check billing docs for up‑to‑date numbers.

### 4.1 General chat / summarization / Q&A

- **Best default (paid / serious use):**
  - **Gemini 2.5 Flash** – great balance of cost, speed, and reasoning.
- **Cheapest at scale:**
  - **Gemini 2.5 Flash‑Lite** or **2.0 Flash‑Lite** – optimized for very high‑volume, cost‑sensitive workloads like routing, tagging, simple responses.

**Free:**
- 2.5 Flash / Flash‑Lite are available in the **Free Tier** for low‑volume API usage before billing kicks in.

---

### 4.2 Reasoning‑heavy tasks / complex agents

- **High‑end reasoning:**
  - **Gemini 3.1 Pro** – “reasoning‑first” model with 1M context and advanced agentic capabilities.
  - Great for multi‑step agents, complex multimodal reasoning, system‑oriented code assistants.
- **Fast but strong agents:**
  - **Gemini 3.5 Flash** – described as “most impressive model yet for agentic workflows” with frontier‑level performance.
  - Good trade‑off when you need both IQ and speed.

**Free:**

- **3.1 Pro / 3.5 Flash**:
  - Exposed in Gemini API/Vertex AI; external sources note that 3 Pro‑class models generally **do not have a standing free API quota** (only UI trials in AI Studio).
  - Expect to pay from token 1 for API usage.
- For **free experimentation** with agents, 2.5 Flash is often the better starting point.

---

### 4.3 Coding assistants / code agents

- **Top choices:**
  - **Gemini 3.5 Flash** – strong on agentic coding benchmarks (Terminal‑bench 2.1, etc.).
  - **Gemini 3.1 Pro** and **Gemini 2.5 Pro** – both marketed as having deep coding capabilities and agentic workflows.

**Typical usage:**

- Code completion + refactor + tests in IDEs.
- Agentic coding with tools (e.g., Gemini Code Assist CLI & GitHub app).

**Free and quotas:**

- Gemini Code Assist (consumer/individual):
  - Free edition: up to **1000 requests per user per day** across CLI/agent mode.
  - Higher tiers (AI Pro, Ultra, Standard, Enterprise) raise that quota to 1500–2000 requests per user per day.
- API‑level: 2.5 Flash/Pro have Free Tier tokens; 3.x Pro/Flash are billed according to pricing table.

---

### 4.4 Realtime voice / interactive agents

- **Realtime conversation (audio in/out):**
  - **Gemini 3.1 Flash Live** – audio‑to‑audio for real‑time dialogue.
  - **Gemini 2.5 Flash Live** – bidirectional streaming audio with low latency for natural conversations.

- **Text‑to‑speech:**
  - **Gemini 2.5 Flash TTS** – controllable TTS optimized for high‑quality speech (podcasts, audiobooks, etc.).

**Free:**
- These are exposed via Gemini API; some Live/TTS variants are accessible in AI Studio for free experimentation, with usage limits; API usage is billed per token/second under the pricing docs.

---

### 4.5 Image generation and editing

- **Gemini 2.5 Flash Image** – image generation + editing, with conversational editing, multi‑image fusion, character consistency.
- **Gemini 3.1 Flash Image / 3 Pro Image (preview)** – higher‑end image reasoning, text rendering, multi‑turn editing for advanced workflows.

**Use cases:** marketing creatives, UIs, diagrams, character art, multi‑turn editing sessions.

**Free:**
- Image models can be tried in Google AI Studio without billing until you link a paid key; API use is billed per image/token according to pricing.

---

### 4.6 Embeddings / RAG

- **Recommended:** `gemini-embedding-001`.
- Use for: semantic search, RAG over documents, classification, clustering, recommendation, etc.

**Free:**
- Included in Free Tier for low‑volume usage; large‑scale RAG will incur embedding charges (per embedding token) as per pricing.

---

## 5. Free vs paid: how the tiers actually work

Key facts from billing docs and independent breakdowns:

- **AI Studio UI**
  - Chat/playground UI is **free to try** many models, including high‑end ones like Gemini 3 Pro, subject to **hidden, dynamic daily rate limits**.
  - Recent reports mention some users seeing **very low daily limits (≈10 requests/day) in AI Studio** for certain models when demand is high.

- **Gemini API Free Tier**
  - When you create an API key *without* attaching a Cloud Billing account, you start on the **Free tier**.
  - Free Tier gives **zero‑cost tokens** for selected models (primarily Gemini 2.5/2.0/3.x Flash‑class models and embedding) until you hit per‑model free quotas per project.
  - Exact per‑day request limits and free tokens vary by model and may change; they are not all explicitly documented.

- **Paid tiers**
  - Once you link a billing account or exceed free quota, usage is billed per million tokens by **model + input/output** mode (Standard vs higher quality modes where applicable).
  - Some top frontier models (e.g., Gemini 3 Pro) are billed from the first token for API usage and have **no standing free API quota**, though you can play with them in AI Studio UI.

---

## 6. Code examples (Python, very minimal)

### 6.1 Text / chat with Gemini 2.5 Flash (Python)

```python
import google.generativeai as genai

genai.configure(api_key="YOUR_API_KEY")

model = genai.GenerativeModel("gemini-2.5-flash")

response = model.generate_content("Explain retrieval-augmented generation in simple terms.")
print(response.text)
```

- Uses `gemini-2.5-flash` as a fast, cheap general model.

---

### 6.2 Embeddings with `gemini-embedding-001`

```python
import google.generativeai as genai

genai.configure(api_key="YOUR_API_KEY")

embed_model = "gemini-embedding-001"

texts = [
    "First chunk of a document",
    "Second chunk of a document",
]

result = genai.embed_content(
    model=embed_model,
    content=texts,
)

vectors = result['embedding']  # or result['embeddings'] depending on SDK version
print(len(vectors), "embeddings")
```

- These vectors are what you’d store in a vector DB for RAG.

---

## 7. How to choose models in practice (for you)

Given your interests (agents, deepfake detection, CV, automation):

- **Prototype / low‑cost agents & RAG** →
  - Use **Gemini 2.5 Flash** + `gemini-embedding-001` on the **Free Tier** until you outgrow the quotas.

- **Serious coding assistant / CoS agent** →
  - Move to **Gemini 3.5 Flash** or **Gemini 3.1 Pro** when you need frontier‑level coding + reasoning; expect to pay via API.

- **Voice / real‑time assistants** →
  - Use **Gemini 3.1 Flash Live / 2.5 Flash Live** for audio streaming; TTS models for speech output.

- **Image workflows (reports, SHM diagrams, visuals)** →
  - Use **Gemini 2.5 Flash Image** (and later 3.x image models) for generation + editing.

Start with free‑tier **2.5 Flash + embedding** for most experimentation, then upgrade to **3.x Pro/Flash** once you need more power or higher limits.