# Ollama: Complete A-Z Guide

> A comprehensive guide to understanding, installing, running, and deploying Ollama for local AI applications.

---

# Table of Contents

1. What is Ollama?
2. Why Ollama Exists
3. How Ollama Works
4. Ollama Architecture
5. Installation
6. Basic Commands
7. Model Library
8. Popular Models
9. Understanding Model Sizes
10. Modelfiles
11. Ollama API
12. Python Integration
13. JavaScript Integration
14. Embeddings
15. RAG with Ollama
16. Hardware Requirements
17. Performance Optimization
18. Local vs Cloud
19. Security Considerations
20. Ollama vs OpenAI
21. Ollama vs LM Studio
22. Ollama vs Oobabooga
23. Real-World Use Cases
24. Best Models by Task
25. Deployment Patterns
26. Advantages
27. Limitations
28. Frequently Asked Questions
29. Learning Roadmap
30. Final Summary

---

# 1. What is Ollama?

Ollama is an open-source runtime that allows you to download, manage, and run Large Language Models (LLMs) locally on your machine.

Think of Ollama as:

> Docker for LLMs

Just as Docker makes it easy to run containers, Ollama makes it easy to run AI models.

## Key Features

- Run AI models locally
- No API key required
- Works offline
- Free local inference
- Simple CLI
- REST API support
- Python & JavaScript SDKs
- Supports hundreds of open-source models

---

# 2. Why Ollama Exists

Before Ollama:

| Problem | Solution Provided by Ollama |
|----------|----------|
| Need API keys | Run locally |
| Pay-per-token costs | Free local inference |
| Internet dependency | Offline capability |
| Privacy concerns | Data stays on device |
| Complex setup | One-command installation |

---

# 3. How Ollama Works

## Traditional AI Workflow

```text
User
 ↓
OpenAI API
 ↓
Cloud Model
 ↓
Response
```

## Ollama Workflow

```text
User
 ↓
Ollama
 ↓
Local Model
 ↓
Response
```

Everything happens on your machine.

---

# 4. Ollama Architecture

```text
Application
     │
     ▼
 Ollama API
     │
     ▼
 Ollama Runtime
     │
     ▼
 LLM Model
     │
     ▼
 CPU / GPU
```

---

# 5. Installation

## Linux

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## macOS

Download from:

https://ollama.com

## Windows

Download installer from:

https://ollama.com

---

# 6. Basic Commands

## Run Model

```bash
ollama run llama3.2
```

## Download Model

```bash
ollama pull llama3.2
```

## List Models

```bash
ollama list
```

## Running Models

```bash
ollama ps
```

## Remove Model

```bash
ollama rm llama3.2
```

## Start Server

```bash
ollama serve
```

---

# 7. Model Library

Official Library:

https://ollama.com/library

## Categories

| Category | Examples |
|-----------|-----------|
| Chat | Llama, Gemma |
| Coding | Qwen-Coder |
| Reasoning | DeepSeek-R1 |
| Embeddings | EmbeddingGemma |
| Vision | LLaVA |
| OCR | GLM-OCR |

---

# 8. Popular Models

## General Chat

| Model | Strength |
|---------|---------|
| Llama 3.3 | Balanced |
| Gemma 3 | Fast |
| Qwen 3 | Strong Reasoning |
| Mistral | Lightweight |
| Phi-4 | Small but Powerful |

## Coding

| Model | Strength |
|---------|---------|
| Qwen-Coder | Excellent |
| DeepSeek-Coder | Strong |
| StarCoder2 | Popular |
| Stable-Code | Lightweight |

## Embeddings

| Model |
|---------|
| EmbeddingGemma |
| Qwen-Embedding |
| All-MiniLM |

---

# 9. Understanding Model Sizes

| Size | Typical Usage |
|---------|---------|
| 1B–4B | Lightweight Chat |
| 7B–9B | Personal Assistant |
| 13B–22B | Coding & Agents |
| 30B–70B | Advanced Reasoning |
| 100B+ | Enterprise AI |

---

# 10. Modelfiles

A Modelfile is similar to a Dockerfile.

Example:

```text
FROM llama3.2

SYSTEM """
You are a helpful AI assistant.
"""

PARAMETER temperature 0.3
PARAMETER num_ctx 8192
```

Create:

```bash
ollama create assistant -f Modelfile
```

Run:

```bash
ollama run assistant
```

---

# 11. Ollama API

Default endpoint:

```text
http://localhost:11434
```

## Common Endpoints

| Endpoint | Purpose |
|-----------|-----------|
| /api/chat | Chat Completion |
| /api/generate | Text Generation |
| /api/embed | Embeddings |
| /api/create | Create Model |
| /api/show | Model Details |
| /api/pull | Download Model |
| /api/delete | Delete Model |

---

# 12. Python Integration

Install:

```bash
pip install ollama
```

Example:

```python
import ollama

response = ollama.chat(
    model="llama3.2",
    messages=[
        {
            "role": "user",
            "content": "Hello"
        }
    ]
)

print(response["message"]["content"])
```

---

# 13. JavaScript Integration

Install:

```bash
npm install ollama
```

Example:

```javascript
import ollama from "ollama"

const response = await ollama.chat({
  model: "llama3.2",
  messages: [
    {
      role: "user",
      content: "Hello"
    }
  ]
})

console.log(response.message.content)
```

---

# 14. Embeddings

Embeddings convert text into vectors.

Uses:

- Semantic Search
- Similarity Search
- RAG
- Recommendations
- Vector Databases

Example:

```python
import ollama

response = ollama.embed(
    model="embeddinggemma",
    input="Artificial Intelligence"
)
```

---

# 15. RAG with Ollama

RAG = Retrieval Augmented Generation

```text
Documents
    ↓
Embeddings
    ↓
Vector Database
    ↓
Retrieve Context
    ↓
LLM Response
```

Popular Databases:

- Chroma
- Qdrant
- Pinecone
- Weaviate
- pgvector

---