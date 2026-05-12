# 👻 Ghostwriter Artifact — AI Text Humanizer for Claude

> **The #1 AI text humanizer artifact for Claude AI.** Transform AI-generated content into natural, human-like writing that bypasses GPTZero, Turnitin, Originality.ai, and Copyleaks — from a 5-word WhatsApp reply to a 10,000-word blog post.

<!-- SEO keywords: ai text humanizer claude, humanize ai text claude, ai content humanizer, bypass ai detection claude, claude artifact humanizer, ghostwriter claude, ai to human text converter, remove ai detection, ai text rewriter claude, chatgpt text humanizer, make ai text sound human, claude project instructions humanizer -->

**👉 Perplexity version:** [ghostwriter-skill](https://github.com/prakash-connects/content-humanizer-skill) | **Also known as:** `ai-text-humanizer-claude` `ai-content-humanizer` `humanize-ai-writing-claude`

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Platform](https://img.shields.io/badge/platform-Claude%20AI-orange.svg)](https://claude.ai)
[![Version](https://img.shields.io/badge/version-1.0-blue.svg)](./ARTIFACT.md)
[![Works With](https://img.shields.io/badge/also%20works%20with-Perplexity%20%7C%20GPT%20%7C%20Gemini-purple.svg)](./ARTIFACT.md)

---

## What Is This?

**Ghostwriter Artifact** is a Claude-native AI text humanizer built on the actual science behind how AI detectors work. It doesn’t just swap words — it targets the three detection layers every major AI detector uses:

| Detection Layer | What AI Detectors Check | What Ghostwriter Does |
|---|---|---|
| **Perplexity (PPL)** | Is the text too statistically predictable? AI = <60 PPL | Raises your text above 85 PPL |
| **Burstiness (B)** | Are all sentences the same length? AI = <0.2 B | Injects rhythm variation above 0.4 B |
| **Classifier Patterns** | BERT-flagged transition phrases + RLHF verbosity | Removes 30+ AI-isms completely |

### Supported Formats
📱 WhatsApp / casual chat · 💼 LinkedIn posts · 🌐 Quora / forum answers · 📝 Blog posts (up to 10,000 words) · 📧 Email · 💬 Comments & replies

---

## ⭐ Quick Install — Claude Projects (Recommended)

1. Open [Claude.ai](https://claude.ai) → **Create New Project**
2. Go to **Project Instructions**
3. Copy the full contents of [`ARTIFACT.md`](./ARTIFACT.md)
4. Paste as the project system instruction
5. Every chat in that project is now a Ghostwriter session — just paste your content

---

## Quick Install — Paste in Chat

1. Copy [`ARTIFACT.md`](./ARTIFACT.md)
2. Paste at the start of any Claude conversation
3. Say: *"Use these instructions for everything I send next"*
4. Start pasting content to humanize

---

## Quick Install — XML Artifact Upload

1. Download [`ARTIFACT.xml`](./ARTIFACT.xml)
2. Upload directly to Claude Projects as a **knowledge file**
3. Claude references it automatically in every conversation

---

## Quick Install — API

```python
import anthropic

with open("ARTIFACT.md", "r") as f:
    system_prompt = f.read()

client = anthropic.Anthropic(api_key="YOUR_API_KEY")

response = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=4096,
    system=system_prompt,
    messages=[{
        "role": "user",
        "content": "Platform: LinkedIn\n\nHumanize this:\n\nIt is important to note that AI has significantly transformed marketing. Moreover, businesses must adapt to remain competitive."
    }]
)
print(response.content[0].text)
```

---

## How to Use

```
Platform: [LinkedIn / WhatsApp / Blog / Quora / Email / Comment / General]
Tone: [Casual / Professional-Conversational / Formal]
Length: [Preserve / Tighten / Expand]

[Paste your AI-generated content here]
```

**Minimal use:** Just paste your text — Ghostwriter auto-detects platform and tone.

---

## What It Removes (AI-ism Ban List)

Ghostwriter hard-bans **30+ AI-isms** that trigger every major detector:

```
Moreover · Furthermore · Indeed · Consequently · In conclusion · To summarize
It's important to note · This underscores · This highlights · Needless to say
At the end of the day · In today’s fast-paced world · In the ever-evolving landscape
Leverage (metaphorical) · Utilize · Delve into · Deep dive · Navigate the landscape
Tapestry · Pivotal · Meticulous · Vibrant · Realm · Showcasing · Seamlessly
Game-changer · Revolutionary · Groundbreaking · Paradigm shift · In order to
```

---

## Transformation Example

**Before (High AI Risk — GPTZero flags this):**
> “It is important to note that artificial intelligence has significantly transformed the marketing landscape. Moreover, businesses must adapt to these changes to remain competitive. Furthermore, those who fail to embrace this technology may find themselves at a disadvantage.”

**After — LinkedIn (Low AI Risk):**
> “Here’s what I’ve noticed — AI has completely shaken up how we do marketing. The companies rolling with it are pulling ahead fast. And the ones dragging their feet? They’re going to feel it. Not someday. Now.”

**Changes:** Eliminated 3 Tier-1 banned phrases · Burstiness injection (4 varied sentences) · First-person framing · Fragment punch ending.

---

## Features at a Glance

| Feature | Description |
|---|---|
| 📊 **Perplexity Elevation** | Raises PPL above human baseline (>85) |
| 🔀 **Burstiness Injection** | Forces sentence length variation every paragraph |
| 🚫 **AI-ism Removal** | 30+ hard-banned phrases, 8 soft-limit phrases |
| 🎤 **Voice Injection** | Contractions, first-person, emotional investment |
| 🎯 **Platform Optimization** | WhatsApp to 10k-word articles — tone-matched |
| ✅ **Self-Validation Loop** | 8-point checklist before every output |
| 📀 **Long-form Ready** | Handles up to 10,000 words |
| 📎 **XML Artifact Support** | Upload directly to Claude Projects knowledge base |

---

## Files

```
content-humanizer-artifact/  (also: ghostwriter-artifact, ai-text-humanizer-claude)
├── ARTIFACT.md     ← Main file — paste into Claude Projects or chat
├── ARTIFACT.xml    ← XML version for Claude Projects knowledge upload
└── README.md       ← This file
```

---

## Ethical Use

✅ Rephrasing your own AI-assisted drafts · Professional content refinement · Marketing copy · Personal writing improvement

❌ Academic fraud · Impersonation · Misinformation · Harassment

---

## Related

- **Perplexity Skill version:** [prakash-connects/content-humanizer-skill](https://github.com/prakash-connects/content-humanizer-skill)

---

## Also Known As

`ghostwriter-artifact` · `ai-text-humanizer-claude` · `ai-content-humanizer` · `humanize-ai-text` · `claude-artifact-humanizer` · `bypass-ai-detection-claude` · `chatgpt-humanizer` · `ai-to-human-text` · `remove-ai-detection` · `claude-project-instructions-humanizer`

---

## License

MIT — free to use, modify, and share with attribution.

---

## Author

**Prakash Behera** — [@prakash-connects](https://github.com/prakash-connects)

*Built on the actual science of how AI detectors work — not guesswork.*
