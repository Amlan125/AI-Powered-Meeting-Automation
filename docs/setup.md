# ⚙️ Setup Guide

Step-by-step to set up the AI meeting note automation.

## 1️⃣ Fireflies.ai
- Sign up & connect your Zoom account.
- Ensure Fireflies joins your meetings & creates transcripts automatically.

## 2️⃣ Zapier
- Create a new Zap.
- Trigger: **New Meeting** in Fireflies.
- Action 1: **Google Gemini** (summarize transcript).
- Action 2: **Notion** – stores meeting summary in a database.
- Action 3: **Gmail** – send summary email.
- Action 4: **Slack** – post summary to a channel/DM.
  
## 3️⃣ Google Gemini / OpenAI
- Create credentials / API key.
- Connect in Zapier when adding the Gemini step.

## 4️⃣ Test & Publish
- Run test meeting.
- Verify transcript, summary, and email/Slack delivery.
