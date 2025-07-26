# ⚙️ Setup Guide

Step-by-step to set up the AI meeting note automation.


## ✅ Prerequisites

Make sure you have accounts and access to:
- Zapier
- Fireflies.ai (connected to Zoom)
- Google Gemini (via Google AI Studio, integrated with Zapier)
- Notion
- Slack
- Microsoft Teams

> **Tip:** Use the free tiers to start, but some features may need paid plans.


---

## 🛠️ Step-by-Step Setup

### Step 1: Connect Accounts in Zapier

1. Go to Zapier → *My Apps*.
2. Connect these apps:
   - Fireflies.ai
   - Google AI Studio (Gemini)
   - Notion
   - Slack
   - Microsoft Teams
   - (Optional) Email by Zapier
3. Authorize each integration when prompted.


---

### Step 2: Configure Fireflies to Auto-Record Zoom Meetings

1. Log into Fireflies.ai.
2. Go to **Settings → Integrations → Zoom**.
3. Enable *Auto-join meetings* so Fireflies automatically records your Zoom meetings.
4. Start a short Zoom meeting to check that Fireflies joins and adds the meeting to your Fireflies dashboard.


---

### Step 3: Build the Zap in Zapier

1. Create a **new Zap**.
2. **Trigger:**
   - App: Fireflies.ai
   - Event: *New Meeting Transcript* (or similar)
3. **First Action: Summarize**
   - App: Google AI Studio (Gemini)
   - Event: *Send Prompt*
   - Prompt example:
     ```
     You are an AI assistant. Summarize the following meeting transcript in a clear, concise paragraph highlighting key topics and decisions.
     Transcript: {{Transcript URL}}
     ```
4. *(Optional)* **Second Action: Refine summary**
   - Add another Gemini action to clean up or reformat the summary.
5. **Save summary to Notion:**
   - App: Notion
   - Event: *Create Database Item*
   - Map fields:
     - `Name`: Meeting title or date
     - `Content`: Summary text
6. **Send summary to Slack:**
   - App: Slack
   - Event: *Send Channel Message* or *Send Direct Message*
7. **Send summary to Microsoft Teams:**
   - App: Microsoft Teams
   - Event: *Send Chat Message* or *Send Bot Message*
8. **Send summary via Email (optional):**
   - App: Email by Zapier
   - Event: *Send Outbound Email*
   - Body: Include the summary

> ⚙️ **Tip:** Use Zapier's test button for each step to confirm data is flowing correctly.


---

### Step 4: Create Notion Database

1. In Notion:
   - Create → *Empty database* in your workspace (usually in *Private* space).
   - Add properties/columns:
     - `Name` (Title)
     - `Content` (Text)
2. Share the database with Zapier:
   - Click *Share* → *Invite* → Search for **Zapier** → Grant *Edit* access.
3. Back in Zapier:
   - Refresh the database list to select it.


---

### Step 5: Publish & Test

1. Turn on the Zap (*Publish*).
2. Start a Zoom meeting and speak.
3. Confirm:
   - Fireflies records & generates a transcript.
   - Zap triggers automatically.
   - Summary is saved to Notion.
   - Summary is sent to Slack, Teams, and Email.


---


