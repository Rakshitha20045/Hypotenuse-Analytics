# Ollama: The Complete A-Z Guide

> Everything you need to know about Ollama, from beginner concepts to production deployments.

---

# Table of Contents

1. Introduction
2. What is Ollama?
3. Why Ollama Was Created
4. The Docker Analogy
5. How Ollama Works
6. Local AI vs Cloud AI
7. Ollama Architecture
8. Installation
9. First Model Execution
10. Important CLI Commands
11. Ollama Model Library
12. Types of Models Available
13. General Chat Models
14. Coding Models
15. Embedding Models
16. Vision & OCR Models
17. Model Sizes Explained
18. Hardware Requirements
19. Ollama Cloud
20. Rate Limits
21. Modelfiles
22. Creating Custom Models
23. Ollama REST API
24. OpenAI Compatibility
25. Python SDK
26. JavaScript SDK
27. Embeddings
28. Retrieval Augmented Generation (RAG)
29. Vector Databases
30. Ollama + n8n
31. Ollama + Agents
32. Ollama + WhatsApp Bots
33. Ollama + Computer Vision
34. Ollama + Automation
35. Ollama + Research Systems
36. Ollama GUIs
37. Open WebUI
38. AnythingLLM
39. Performance Optimization
40. Security Considerations
41. Production Deployment
42. Ollama vs OpenAI
43. Ollama vs LM Studio
44. Ollama vs Oobabooga
45. Real-World Use Cases
46. Advantages
47. Limitations
48. Best Models for Beginners
49. Recommended Models by Hardware
50. Final Summary

---

# Introduction

Ollama is an open-source runtime designed to run Large Language Models (LLMs) locally on your own computer or server.

It allows developers, students, researchers, and companies to use powerful AI models without relying entirely on cloud providers such as OpenAI, Anthropic, or Google.

---

# What is Ollama?

Ollama is:

- A model manager
- A local AI runtime
- A REST API server
- A model packaging system
- A deployment platform

Think of Ollama as:

> Docker for AI Models

Just as Docker lets you run containers using a simple command, Ollama lets you run LLMs using a simple command.

Example:

```bash
ollama run llama3.2
```

---

# Why Ollama Was Created

Before Ollama:

| Problem | Traditional AI |
|----------|----------|
| API Costs | High |
| Internet Required | Yes |
| Data Privacy | Sent to Cloud |
| API Keys | Required |
| Setup Complexity | High |

After Ollama:

| Feature | Ollama |
|----------|----------|
| Free Local Inference | Yes |
| Offline Usage | Yes |
| Privacy Friendly | Yes |
| API Key Required | No |
| Easy Setup | Yes |

---

# The Docker Analogy

Docker:

```bash
docker pull nginx
docker run nginx
```

Ollama:

```bash
ollama pull llama3.2
ollama run llama3.2
```

Docker manages containers.

Ollama manages AI models.

---

# How Ollama Works

Traditional Workflow:

```text
User
 ↓
OpenAI API
 ↓
Cloud Server
 ↓
Response
```

Ollama Workflow:

```text
User
 ↓
Ollama
 ↓
Local Model
 ↓
Response
```

Everything runs locally.

---

# Core Concept

Ollama is NOT an AI model.

Ollama is a platform that runs AI models.

Examples:

- Llama
- Gemma
- Qwen
- Mistral
- DeepSeek
- Phi

These are models.

Ollama runs them.

---

# Installation

## Linux

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## Windows

Download installer from:

https://ollama.com

## macOS

Download official application.

---

# First Model Execution

Start server:

```bash
ollama serve
```

Run model:

```bash
ollama run llama3.2
```

First run:

1. Downloads model
2. Stores locally
3. Loads model
4. Starts chat

Future runs use cached weights.

---

# Important CLI Commands

## Download Model

```bash
ollama pull llama3.2
```

## Run Model

```bash
ollama run llama3.2
```

## Installed Models

```bash
ollama list
```

## Running Models

```bash
ollama ps
```

## Stop Model

```bash
ollama stop llama3.2
```

## Delete Model

```bash
ollama rm llama3.2
```

---

# Types of Models Available

## General Chat

- Llama
- Gemma
- Mistral
- Dolphin

## Coding

- Qwen-Coder
- DeepSeek-Coder
- StarCoder2
- Stable-Code

## Reasoning

- DeepSeek-R1
- Qwen Reasoning
- Gemma Reasoning

## Embeddings

- EmbeddingGemma
- Qwen3-Embedding
- All-MiniLM

## OCR

- GLM-OCR

## Vision

- LLaVA
- NVIDIA Nano Omni

---

# Model Sizes Explained

| Size | Use Case |
|--------|--------|
| 1B-4B | Basic Chat |
| 7B-9B | Assistant |
| 13B-22B | Coding + Agents |
| 30B-70B | Advanced Reasoning |
| 100B+ | Enterprise |

Larger model:

- Better reasoning
- Better coding
- More memory required

---

# Hardware Requirements

## Tier 1

### 8GB RAM

Models:

- Gemma 4B
- Phi Mini

Tasks:

- Chat
- Notes
- Q&A

---

## Tier 2

### 16GB RAM

Models:

- Llama 8B
- Qwen 7B

Tasks:

- Coding
- Small RAG
- Personal Agent

---

## Tier 3

### 32GB RAM + GPU

Models:

- 13B
- 22B

Tasks:

- Agents
- Coding Assistants
- Large RAG

---

## Tier 4

### 64GB+ RAM + 24GB VRAM

Models:

- 30B
- 70B

Tasks:

- Enterprise AI
- Multi-Agent Systems
- Advanced Reasoning

---

# What People Actually Use Ollama For

## Local ChatGPT

Chat with models locally.

---

## Coding Assistant

Generate code.

Explain code.

Debug code.

---

## RAG Systems

Chat with PDFs.

Internal company search.

Knowledge bases.

---

## AI Agents

Chief of Staff Agent.

Research Agent.

Automation Agent.

---

## WhatsApp Bots

Use Ollama API to generate replies.

---

## Computer Vision Pipelines

YOLO
↓
Detection
↓
Structured Data
↓
Ollama
↓
Natural Language Report

---

# Modelfiles

Modelfiles are similar to Dockerfiles.

Example:

```text
FROM llama3.2:3b

SYSTEM """
You are a Chief of Staff AI Assistant.
"""

PARAMETER temperature 0.3

PARAMETER num_ctx 8192
```

Create:

```bash
ollama create cos-agent -f Modelfile
```

---

# Ollama REST API

Default:

```text
http://localhost:11434
```

Endpoints:

| Endpoint | Purpose |
|----------|----------|
| /api/chat | Chat |
| /api/generate | Completion |
| /api/embed | Embeddings |
| /api/create | Create Model |
| /api/show | Model Details |
| /api/pull | Download |
| /api/delete | Delete |

---

# OpenAI Compatibility

Ollama supports:

```text
/v1/chat/completions
```

Many OpenAI SDKs work with minimal modifications.

---

# Embeddings

Embeddings convert text into vectors.

Used for:

- Search
- RAG
- Similarity
- Recommendations

Recommended Models:

- EmbeddingGemma
- Qwen3-Embedding
- All-MiniLM

---

# RAG Workflow

```text
Documents
 ↓
Chunking
 ↓
Embeddings
 ↓
Vector Database
 ↓
Retrieval
 ↓
LLM
 ↓
Answer
```

Vector Databases:

- Chroma
- Qdrant
- Weaviate
- Pinecone
- pgvector

---

# GUI Ecosystem

## Open WebUI

ChatGPT-like interface.

## AnythingLLM

Document chat.

RAG.

Knowledge bases.

---

# Performance Tips

- Use quantized models
- Use GPU
- Reduce context size
- Monitor with `ollama ps`
- Use 4-bit or 5-bit GGUF models

---

# Security

Default:

```text
localhost:11434
```

For production:

- HTTPS
- Nginx
- Caddy
- Authentication
- VPN

---

# Ollama vs OpenAI

| Feature | Ollama | OpenAI |
|----------|----------|----------|
| Free | Yes | No |
| Offline | Yes | No |
| Privacy | High | Lower |
| Setup | Required | Easy |
| Rate Limits | No | Yes |

---

# Final Summary

Ollama is an open-source local AI platform that lets you run powerful language models on your own hardware.

Think of it as:

> Docker + Local ChatGPT + AI API Server

Best Uses:

- AI Assistants
- Coding Assistants
- RAG Systems
- AI Agents
- Automation
- Privacy-Sensitive Applications

If you want to learn local AI, build agents, create RAG systems, or reduce API costs, Ollama is one of the best tools available today.