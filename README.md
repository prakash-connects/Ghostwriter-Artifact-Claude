# 🧠 Content Humanizer — Claude Artifact v1.0

> Transform AI-generated text into natural, human-like writing inside Claude — from a 5-word WhatsApp reply to a 10,000-word blog post. Built on the actual science of how AI detectors work.

**👉 Perplexity Skill version:** [content-humanizer-skill](https://github.com/prakash-connects/content-humanizer-skill)

---

## What This Is

A Claude-native content humanization artifact powered by NLP detection science:

- **Perplexity elevation** — raises text unpredictability above human baseline (>85 PPL)
- **Burstiness injection** — forces dramatic sentence rhythm variation (>0.4 B score)
- **AI-ism removal** — eliminates 30+ BERT-flagged phrases and RLHF-induced patterns

**Works for every format:**
📱 WhatsApp · 💼 LinkedIn · 🌐 Quora · 📝 Blog/Article (up to 10k words) · 📧 Email · 💬 Comment replies

---

## How to Install

### ⭐ Option 1 — Claude Project (Best experience)
1. Open [Claude.ai](https://claude.ai) → Create New Project
2. Go to **Project Instructions**
3. Copy the full contents of [`ARTIFACT.md`](./ARTIFACT.md)
4. Paste as the project system instruction
5. Every chat in that project is now a Content Humanizer

### Option 2 — Paste Directly in Chat
1. Copy [`ARTIFACT.md`](./ARTIFACT.md)
2. Paste it at the start of any Claude conversation
3. Say: "Use these instructions for everything I send next"
4. Start pasting your content to humanize

### Option 3 — Claude API
```python
import anthropic

with open("ARTIFACT.md", "r") as f:
    system_prompt = f.read()

client = anthropic.Anthropic(api_key="YOUR_API_KEY")

response = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=4096,
    system=system_prompt,
    messages=[
        {
            "role": "user",
            "content": "Platform: LinkedIn\n\nHumanize this:\n\nIt is important to note that AI has significantly transformed marketing. Moreover, businesses must adapt to remain competitive."
        }
    ]
)
print(response.content[0].text)
```

### Option 4 — XML Artifact (Claude Projects Advanced)
1. Download [`ARTIFACT.xml`](./ARTIFACT.xml)
2. Upload directly to Claude Projects as a knowledge file
3. Claude will reference it automatically in every conversation

---

## How to Use

Once installed, paste your content and optionally specify:

```
Platform: LinkedIn / WhatsApp / Blog / Quora / Email / Comment / General
Tone: Casual / Professional-Conversational / Formal
Length: Preserve / Tighten / Expand

[Your content here]
```

**Minimal use:** Just paste your text — Claude will auto-detect the platform and apply Professional-Conversational tone.

---

## What It Does

| Technique | What It Targets |
|---|---|
| **Perplexity Elevation** | Raises PPL score using surprising-but-accurate word choices |
| **Burstiness Injection** | Short punchy sentences + long complex ones in every paragraph |
| **AI-ism Removal** | Strips 30+ banned phrases: "Moreover", "delve into", "tapestry" and more |
| **Structural Humanization** | Irregular paragraph lengths, organic transitions |
| **Voice Injection** | First-person hooks, contractions, emotional investment |
| **Platform Optimization** | WhatsApp to 10,000-word articles — tone-matched per platform |
| **Self-Validation Loop** | 8-point checklist before every output |

---

## Example

**Before (High AI Risk):**
> "It is important to note that artificial intelligence has significantly transformed the marketing landscape. Moreover, businesses must adapt to these changes to remain competitive."

**After — LinkedIn (Low AI Risk):**
> "Here's what I've noticed — AI has completely shaken up how we do marketing. The companies rolling with it are pulling ahead fast. The ones dragging their feet? They're going to feel it. Not someday. Now."

---

## Files

```
content-humanizer-artifact/
├── ARTIFACT.md     ← Main file — paste into Claude Projects or chat
├── ARTIFACT.xml    ← XML version for Claude Projects knowledge upload
└── README.md       ← This file
```

---

## Ethical Use

✅ Your own AI-assisted drafts · Professional content · Marketing copy · Educational materials

❌ Academic fraud · Impersonation · Misinformation · Harassment

---

## Related

- **Perplexity Skill version:** [prakash-connects/content-humanizer-skill](https://github.com/prakash-connects/content-humanizer-skill)

---

## License

MIT — free to use, modify, and share with attribution.

---

## Author

**Prakash Behera** — [@prakash-connects](https://github.com/prakash-connects)

*Built on the actual science of how AI detectors work — not guesswork.*
