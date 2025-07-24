# ⚙️ Setup Guide

Step-by-step to set up the AI meeting note automation.

## 1️⃣ Fireflies.ai
- Sign up & connect your Zoom account.
- Ensure Fireflies joins your meetings & creates transcripts automatically.

## 2️⃣ Zapier
- Create a new Zap.
- Trigger: **New Meeting** in Fireflies.
- Action 1: **Google Gemini** (summarize transcript).
- Action 2: **Gmail** – send summary email.
- Action 3: **Slack** – post summary to a channel.

📦 Or import the provided Zap:
[`fireflies-zoom-ai-summarizer.zap`](../zap-export/fireflies-zoom-ai-summarizer.zap)

## 3️⃣ Google Gemini / OpenAI
- Create credentials / API key.
- Connect in Zapier when adding the Gemini step.

## 4️⃣ Test & Publish
- Run test meeting.
- Verify transcript, summary, and email/Slack delivery.
