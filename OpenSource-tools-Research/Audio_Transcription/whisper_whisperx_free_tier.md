# Whisper & WhisperX — Free Tier Guide (2026)

> **Last Updated:** June 2026 | **Status:** Active — Fully open source, run locally for $0

---

## 1. Overview: Two Different Tools

| Tool | What It Is | Cost | Best For |
|---|---|---|---|
| **Whisper (OpenAI)** | Open-source speech recognition model | **$0** (self-run) | Transcription, translation |
| **WhisperX** | Community fork with speaker diarization | **$0** (self-run) | Multi-speaker transcription |
| **WhisperAI.com** | Commercial service using Whisper | **Freemium** ($0-9.49/wk) | Cloud transcription |
| **OpenWhispr** | Desktop app using Whisper | **$0** (local) / $6.67/mo (Pro) | Real-time dictation |

> **This guide focuses on the FREE open-source options:** Whisper and WhisperX.

---

## 2. Whisper (OpenAI) — Free Tier

### What You Get (Free)

Whisper is **completely free** when run locally or via open-source tools. No API calls, no subscriptions.

| Feature | Free? | Details |
|---|---|---|
| **Transcription** | ✅ $0 | 100+ languages |
| **Translation** | ✅ $0 | Non-English → English |
| **Model sizes** | ✅ $0 | Tiny, Base, Small, Medium, Large, Turbo |
| **Timestamps** | ✅ $0 | Word-level and segment-level |
| **Local processing** | ✅ $0 | No internet needed after download |
| **Commercial use** | ✅ $0 | MIT license |

### Model Sizes & Hardware Needs

| Model | Size | Speed | Accuracy | VRAM Needed | Best For |
|---|---|---|---|---|---|
| **Tiny** | 39 MB | Fastest | Basic | ~1 GB | Real-time, low resource |
| **Base** | 74 MB | Fast | Good | ~1 GB | Quick drafts |
| **Small** | 244 MB | Moderate | Better | ~2 GB | Balanced |
| **Medium** | 769 MB | Slower | Very Good | ~5 GB | Quality matters |
| **Large-v3** | 1.5 GB | Slowest | Best | ~10 GB | Maximum accuracy |
| **Turbo** | 1.6 GB | Fast | Near-Large | ~6 GB | Best speed/quality |

### Rate Limits (Self-Hosted)

| Resource | Limit | Control |
|---|---|---|
| **Audio length** | Unlimited | Your hardware |
| **Files/day** | Unlimited | Your time |
| **Languages** | 100+ | Auto-detect |
| **Concurrent** | Batch size | Your GPU |
| **Speed** | Real-time factor | Model size + GPU |

**Real-Time Factor (RTF):**
- Tiny on CPU: ~0.5x (2x faster than real-time)
- Large on GPU: ~0.1x (10x faster than real-time)
- Turbo on GPU: ~0.05x (20x faster than real-time)

---

## 3. WhisperX — Free Tier

### What WhisperX Adds

WhisperX is a **community-enhanced version** of Whisper with:
- **Speaker diarization** — "Who spoke when"
- **Better word-level timestamps**
- **Batch processing optimization**
- **Voice Activity Detection (VAD)**

| Feature | Whisper | WhisperX | Cost |
|---|---|---|---|
| Transcription | ✅ | ✅ | $0 |
| Translation | ✅ | ✅ | $0 |
| Speaker labels | ❌ | ✅ | $0 |
| Word timestamps | ✅ | ✅ (better) | $0 |
| Batch processing | Basic | Optimized | $0 |
| VAD | ❌ | ✅ | $0 |

### Hardware Needs (WhisperX)

| Task | Minimum | Recommended | Speed |
|---|---|---|---|
| **Transcription only** | 4GB RAM, CPU | 8GB RAM, GPU | 2-10x real-time |
| **+ Speaker diarization** | 8GB RAM, GPU | 16GB RAM, GPU | 1-5x real-time |
| **Batch (10 files)** | 16GB RAM, GPU | 24GB RAM, GPU | Processes in parallel |

---

## 4. Task-by-Task: What Can You Transcribe for Free?

### ✅ Excellent (Free, Fast, Accurate)

| Use Case | Model | Time for 1hr Audio | Why It Works |
|---|---|---|---|
| **Meeting transcription** | Medium/Large | 6-10 min | Clear audio, few speakers |
| **Podcast transcription** | Large/Turbo | 5-8 min | Single speaker, clean audio |
| **Lecture notes** | Medium | 6-10 min | Structured speech |
| **YouTube captions** | Small/Medium | 3-6 min | Pre-recorded, can batch |
| **Interview transcription** | Large + WhisperX | 10-15 min | Speaker diarization needed |
| **Voice memos** | Base/Small | 2-4 min | Short, clear audio |
| **Call recordings** | Medium + WhisperX | 6-10 min | Speaker separation |
| **Sermon/sermon transcription** | Large | 8-12 min | Single speaker, long form |
| **Subtitles (SRT)** | Small/Medium | 3-6 min | Timestamped output |

### ⚠️ Challenging (Still Free, But Lower Accuracy)

| Use Case | Challenge | Model | Tip |
|---|---|---|---|
| **Noisy recordings** | Background noise | Large | Pre-process with noise reduction |
| **Heavy accents** | Unfamiliar speech patterns | Large-v3 | Use fine-tuned model if available |
| **Multiple overlapping speakers** | Crosstalk | WhisperX | May miss some overlaps |
| **Technical jargon** | Domain-specific terms | Large | Add custom vocabulary |
| **Music + speech** | Background music | Medium+ | Use VAD to isolate speech |
| **Very long files** | Memory issues | Any | Split into 30-min chunks |

### ❌ Not Recommended (Even on Free)

| Use Case | Why | Alternative |
|---|---|---|
| **Real-time live transcription** | Latency too high for conversation | Use commercial API (Deepgram, AssemblyAI) |
| **Medical/legal (critical)** | Hallucination risk | Human review + specialized model |
| **Low-resource language** | May hallucinate | Use larger model + verify |
| **Phone call with bad connection** | Too distorted | Clean audio first |

---

## 5. Free Tools to Run Whisper/WhisperX

| Tool | Platform | Ease | Features | Best For |
|---|---|---|---|---|
| **whisper-cli** (official) | All | Medium | Basic transcription | Scripting, automation |
| **WhisperX** | All | Medium | +Diarization | Multi-speaker |
| **faster-whisper** | All | Medium | Optimized speed | Production |
| **insanely-fast-whisper** | All | Easy | 4x speedup | Large batches |
| **Buzz** | Desktop (Win/Mac/Linux) | Easy | GUI, live transcription | Non-technical users |
| **MacWhisper** | Mac | Very Easy | GUI, editing | Mac users |
| **OpenWhispr** | Desktop | Easy | Dictation, AI cleanup | Real-time dictation |
| **Whisper Web UI** | Browser | Easy | Web interface | Any device |
| **Google Colab** | Cloud | Easy | Free GPU | No local GPU |

---

## 6. Quick Start (Free)

### Option A: Command Line (Most Flexible)

```bash
# Install
pip install openai-whisper

# Transcribe (free, local)
whisper audio.mp3 --model medium --language en --output_format txt

# With timestamps
whisper audio.mp3 --model large-v3 --output_format srt

# Translate to English
whisper audio.mp3 --model large-v3 --task translate
```

### Option B: WhisperX (With Speaker Diarization)

```bash
# Install
pip install whisperx

# Transcribe + identify speakers
whisperx audio.mp3 --model large-v3 --diarize --hf_token YOUR_HF_TOKEN
```

### Option C: Google Colab (Free GPU, No Setup)

```python
# Run in Google Colab (free T4 GPU)
!pip install openai-whisper
import whisper

model = whisper.load_model("medium")
result = model.transcribe("audio.mp3")
print(result["text"])
```

---

## 7. Free vs Paid Comparison

| Feature | Whisper (Self-Hosted) | WhisperAI.com | OpenWhispr Pro |
|---|---|---|---|
| **Cost** | **$0** | $0-9.49/wk | $6.67/mo |
| **Setup** | Install required | Web UI | Install required |
| **Privacy** | Complete | Cloud-processed | Local (free tier) |
| **Speed** | Hardware-dependent | Fast (cloud GPU) | Fast (local) |
| **Speaker diarization** | WhisperX only | ✅ | ✅ |
| **Batch processing** | ✅ | ✅ | ✅ |
| **Real-time** | ⚠️ Laggy | ✅ | ✅ |
| **Editing UI** | ❌ | ✅ | ✅ |
| **API access** | ❌ | ✅ | ✅ |
| **Support** | Community | Email | Email |

---

## 8. Quick Cheat Sheet

```
WHISPER / WHISPERX FREE TIER CHEAT SHEET

COST: $0 (self-hosted, open source)
LICENSE: MIT (commercial use allowed)

MODEL SIZES (pick based on your hardware):
• Tiny (39MB)  → Low resource, real-time, basic accuracy
• Base (74MB)  → Fast, good for drafts
• Small (244MB) → Balanced speed/quality
• Medium (769MB) → Good quality, most common choice
• Large-v3 (1.5GB) → Best accuracy, slower
• Turbo (1.6GB) → Near-Large quality, faster

HARDWARE NEEDS:
• CPU only: Tiny, Base, Small (slow but works)
• 4GB GPU: Small, Medium
• 8GB GPU: Medium, Large
• 16GB GPU: Large, Turbo, WhisperX diarization

BEST FREE USES:
• Meeting transcription (Medium/Large)
• Podcast captions (Small/Medium)
• Lecture notes (Medium)
• Interview with speaker IDs (Large + WhisperX)
• YouTube subtitles (Small/Medium)
• Voice memos (Base/Small)
• Call recordings (Medium + WhisperX)

FREE TOOLS:
• whisper-cli: Official, scripting
• WhisperX: +Speaker diarization
• faster-whisper: Speed optimized
• Buzz: Desktop GUI (easy)
• MacWhisper: Mac GUI (very easy)
• Google Colab: Free GPU, no setup

CHALLENGING (lower accuracy):
• Noisy audio
• Heavy accents
• Overlapping speakers
• Technical jargon
• Music background

NOT RECOMMENDED:
• Real-time conversation (too slow)
• Critical medical/legal (hallucination risk)
• Very low-resource languages
```

---

## 9. Summary

**Whisper and WhisperX are completely free** when self-hosted. Your only cost is your hardware.

**Best Strategy:**
- **Start with `medium` model** — best balance for most tasks
- **Use WhisperX** when you need speaker diarization
- **Use Google Colab** if you don't have a GPU
- **Use Buzz/MacWhisper** if you want a GUI without coding
- **Upgrade to commercial** (WhisperAI, Deepgram) only if you need real-time or editing features
