# AI-Powered Meeting Automation:

This project demonstrates how to build an **end-to-end no-code AI automation** that:
- Transcribes virtual meetings automatically (Fireflies AI)
- Summarizes transcripts using Google Gemini via Zapier
- Stores the summary in Notion along with the key insights and date of the meeting
- Sends it instantly to Email, Slack, and Microsoft Teams


---

## Why this project?
✅ Eliminates manual meeting notes  
✅ Uses AI to create concise summaries  
✅ Distributes insights across tools automatically  
✅ Demonstrates practical integration of AI + no-code automation

---

## Tech Stack / Tools
| Tool | Purpose |
|-----|---------|
| Fireflies AI | Automatic meeting transcription |
| Zapier | Automation platform to connect apps |
| Google Gemini (AI by Zapier) | Summarizes transcripts |
| Notion | Stores summaries in a database |
| Email by Zapier | Sends email alerts |
| Slack & Microsoft Teams | Deliver summaries to chat |

---

##  Workflow Overview
1.  Meeting is held → Fireflies transcribes
2.  Zapier detects new transcript
3.  Sends transcript to Gemini → AI summary
4.  Saves summary to Notion
5.  Sends email
6.  Posts to Slack & Teams


---

##  Step-by-Step Setup

###  1. Setup Fireflies
- Sign up at [Fireflies.ai](https://fireflies.ai)
- Connect your calendar & Zoom / Google Meet
- Fireflies will auto-join and transcribe meetings

---

###  2. Setup Notion
- Create a **new database** (e.g., “Meeting Summaries”)
- Share database with the Zapier integration  
  - Go to *Settings → Connections → Integrations → Zapier*  
  - Give “Can edit” permission

---

###  3. Create Zap in Zapier

####  Trigger: Fireflies
- App: **Fireflies AI**
- Event: *New Meeting Transcript*

####  Action #1: Summarize
- App: **AI by Zapier** (Google Gemini)
- Prompt:  
  > “You are an AI assistant. Summarize the following meeting transcript in a clear, concise paragraph, highlighting key topics and decisions. Do not include filler or irrelevant parts.”

####  Action #2: Save to Notion
- App: **Notion**
- Event: *Create Database Item*
- Map fields:  
  - Title → Meeting name
  - Content → AI summary

####  Action #3: Send Email
- App: **Email by Zapier**
- To: your email (or team)
- Subject: e.g., “Meeting Summary: {{Meeting name}}”
- Body: AI summary

####  Action #4: Send Slack message
- App: **Slack**
- Event: *Send channel message* or *Send DM*
- Message: AI summary + meeting link

####  Action #5: Send Microsoft Teams message
- App: **Microsoft Teams**
- Event: *Send chat message to self*
- Message: AI summary

---

##  Testing & Validation
- Tested on 2 real meetings (Meeting A & Meeting B)
- Verified:
  - Fireflies transcript → Zapier trigger works
  - AI summary created correctly
  - Summary appears in Notion
  - Email, Teams & Slack messages received

---

## Screenshots

| Step | Screenshot |
|-----|-----------|
| Zapier workflow | <img width="322" height="498" alt="zapier workflow" src="https://github.com/user-attachments/assets/865e5f6a-9c87-412f-8ab7-c324909d68a9" />
 |
| Notion database | <img width="1079" height="525" alt="notion" src="https://github.com/user-attachments/assets/d9df9c2c-dc1d-4d72-8cd1-c0c91a69cb64" />
 |
| Email summary | <img width="1011" height="491" alt="mail" src="https://github.com/user-attachments/assets/67d63959-ea8e-4398-ba9b-3c9bd3d7b746" />
 |
| Slack / Teams message | <img width="965" height="413" alt="slack" src="https://github.com/user-attachments/assets/9523ddef-044d-42e7-ae6b-cce041dc0add" />
 |

---

##  Future Improvements
- Extract & save **action items** separately
- Add **topic tags** automatically
- Compare summaries from Gemini vs GPT vs Claude
- Auto-generate **weekly summary reports**

---

##  Author
Built by Amlan (https://github.com/Amlan125)

Email: abgohain77@gmail.com

---

