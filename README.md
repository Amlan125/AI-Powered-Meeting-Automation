# 🤖 AI-Powered Meeting Automation: Fireflies + Zapier + Gemini + Notion, Email, Slack & Teams

This project demonstrates how to build an **end-to-end no-code AI automation** that:
- Transcribes meetings automatically (Fireflies AI)
- Summarizes transcripts using Google Gemini via Zapier
- Stores the summary in Notion
- Sends it instantly to Email, Slack, and Microsoft Teams

A perfect real-world project to showcase on your CV or GitHub.

---

## 📌 Why this project?
✅ Eliminates manual meeting notes  
✅ Uses AI to create concise summaries  
✅ Distributes insights across tools automatically  
✅ Demonstrates practical integration of AI + no-code automation

---

## ⚙️ Tech Stack / Tools
| Tool | Purpose |
|-----|---------|
| Fireflies AI | Automatic meeting transcription |
| Zapier | Automation platform to connect apps |
| Google Gemini (AI by Zapier) | Summarizes transcripts |
| Notion | Stores summaries in a database |
| Email by Zapier | Sends email alerts |
| Slack & Microsoft Teams | Deliver summaries to chat |

---

## 🧩 Workflow Overview
1. 📝 Meeting is held → Fireflies transcribes
2. 🔄 Zapier detects new transcript
3. ✏️ Sends transcript to Gemini → AI summary
4. 🗂️ Saves summary to Notion
5. 📧 Sends email
6. 💬 Posts to Slack & Teams

![Workflow Diagram](images/zap-setup.png)

---

## 🚀 Step-by-Step Setup

### ✅ 1. Setup Fireflies
- Sign up at [Fireflies.ai](https://fireflies.ai)
- Connect your calendar & Zoom / Google Meet
- Fireflies will auto-join and transcribe meetings

---

### ✅ 2. Setup Notion
- Create a **new database** (e.g., “Meeting Summaries”)
- Share database with the Zapier integration  
  - Go to *Settings → Connections → Integrations → Zapier*  
  - Give “Can edit” permission

---

### ✅ 3. Create Zap in Zapier

#### ⚡ Trigger: Fireflies
- App: **Fireflies AI**
- Event: *New Meeting Transcript*

#### 🤖 Action #1: Summarize
- App: **AI by Zapier** (Google Gemini)
- Prompt:  
  > “You are an AI assistant. Summarize the following meeting transcript in a clear, concise paragraph, highlighting key topics and decisions. Do not include filler or irrelevant parts.”

#### 📒 Action #2: Save to Notion
- App: **Notion**
- Event: *Create Database Item*
- Map fields:  
  - Title → Meeting name
  - Content → AI summary

#### 📧 Action #3: Send Email
- App: **Email by Zapier**
- To: your email (or team)
- Subject: e.g., “Meeting Summary: {{Meeting name}}”
- Body: AI summary

#### 💬 Action #4: Send Slack message
- App: **Slack**
- Event: *Send channel message* or *Send DM*
- Message: AI summary + meeting link

#### 🗨️ Action #5: Send Microsoft Teams message
- App: **Microsoft Teams**
- Event: *Send chat message to self*
- Message: AI summary

---

## 🧪 Testing & Validation
- Tested on 2 real meetings (Meeting A & Meeting B)
- Verified:
  - Fireflies transcript → Zapier trigger works
  - AI summary created correctly
  - Summary appears in Notion
  - Email, Slack & Teams messages received

---

## 📸 Screenshots

| Step | Screenshot |
|-----|-----------|
| Zapier workflow | ![](images/zap-setup.png) |
| Notion database | ![](images/notion-db.png) |
| Email summary | ![](images/email-example.png) |
| Slack / Teams message | ![](images/slack-teams.png) |

*(Add real screenshots here in the /images folder)*

---

## 📚 Future Improvements
- Extract & save **action items** separately
- Add **topic tags** automatically
- Compare summaries from Gemini vs GPT vs Claude
- Auto-generate **weekly summary reports**

---

## 🧑‍💻 Author
Built by [Your Name](https://github.com/yourusername) — July 2025

---

## 📄 License
MIT (or your chosen license)

---

## 🎥 Demo Script (Optional)
> Hi! Here’s a quick demo of my AI meeting automation project.  
> After every meeting, Fireflies AI automatically creates a transcript.  
> Zapier detects the new transcript, sends it to Google Gemini, and produces a summary.  
> Then, Zapier saves it to Notion, sends me an email, and posts it to Slack & Teams.  
> It keeps my notes organized, shares them instantly with the team, and saves time every week!

---

## ⭐ Feel free to fork, use, or ask questions!
