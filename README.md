# faceless-video-script-to-telegram-n8n
Automatically generates a cinematic faceless video script every day and sends each scene directly to Telegram using n8n and OpenRouter AI.
# 🎬 Daily Faceless Video Script to Telegram (n8n)

This automation workflow generates a **cinematic faceless video script** with 6 visually rich scenes every day at 9 AM and sends each scene as a message to a Telegram bot.  
Perfect for AI creators, short-form video makers, and automation lovers.

---

## 🔁 Workflow Summary

| Feature | Description |
|--------|-------------|
| ⏰ Trigger | Daily at 9:00 AM |
| 🧠 Script Generator | OpenRouter (Mistral 7B) |
| 🎥 Output | 6 visual scenes |
| 📤 Sends to | Telegram Chat |

---

## 🎯 Use Case

This workflow helps:
- AI video creators looking for faceless script ideas
- Creators using Sora, Kaiber, Pika, etc.
- Short-form video teams needing daily content
- Anyone automating visual storytelling

---

## 🧩 Node Breakdown

1. **Schedule Trigger**
   - Runs daily at 9 AM.

2. **SCRIPT (HTTP Request)**
   - Sends a cinematic script prompt to OpenRouter using the Mistral 7B model.

3. **SENDING SCRIPT (Set)**
   - Extracts the AI response.

4. **CLEAN SCRIPT (Code)**
   - Breaks the full script into individual scene blocks.

5. **Send a Text Message (Telegram)**
   - Sends each scene to your Telegram chat.

---

## 📂 Files in This Repo

| File | Description |
|------|-------------|
| `faceless-video-script-to-telegram-n8n.json` | Full n8n workflow export |
| `README.md` | This documentation |

---

## 🛠️ Setup Instructions

1. **Import the `.json` file** into your n8n editor.
2. Configure:
   - `Bearer sk-...` → Your **OpenRouter API Key**
   - `Telegram Credentials` → Your own Telegram bot setup
3. (Optional) Customize the prompt in the **SCRIPT** node.
4. Activate the workflow.

---

## 🔐 API Keys Required

| Tool | Key Needed | Where to Use |
|------|------------|--------------|
| OpenRouter.ai | ✅ | In HTTP Request headers |
| Telegram Bot | ✅ | In Telegram node credentials |

---

## 📸 Workflow Screenshot

_Add a screenshot of your n8n workflow for presentation_

---

## 🧠 Prompt Used in AI

```text
You are a professional AI video scriptwriter. You create realistic, cinematic, faceless video scripts with high-definition visuals for 60-second reels...
