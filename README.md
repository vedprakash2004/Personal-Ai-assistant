# 🤖 Personal AI Assistant

An AI-powered Personal Assistant built with **n8n**, **OpenAI GPT-4.1 Mini**, **Telegram**, **Google Calendar**, **Gmail**, and **Google Sheets**. The assistant automates communication, scheduling, and contact management using intelligent AI agents and workflow automation.

---

## 🚀 Features

- 💬 Interact through Telegram (Text & Voice)
- 🎙️ Voice-to-Text using OpenAI Whisper
- 📧 Send and manage Gmail emails
- 📅 Create and manage Google Calendar events
- 👥 Contact lookup using Google Sheets
- 🧠 Conversational memory for context-aware responses
- ⚡ AI-powered workflow automation using n8n
- 🤖 Multiple specialized AI agents

---

## 🏗️ Architecture

```
Telegram
     │
     ▼
Telegram Trigger
     │
     ▼
Text / Voice Detection
     │
 ┌──────┴───────┐
 │              │
 ▼              ▼
Voice        Text
 │              │
 ▼              ▼
Whisper     Set Text
 │              │
 └──────┬───────┘
        ▼
 Main AI Agent
        │
 ┌──────┼──────────────┐
 │      │              │
 ▼      ▼              ▼
Email Contact      Calendar
Agent Database      Agent
 │      │              │
 ▼      ▼              ▼
Gmail Google      Google
      Sheets      Calendar
        │
        ▼
Telegram Response
```

---

# 📂 Project Structure

```
Personal-AI-Assistant/
│
├── Main AI Agent
├── Email Agent
├── Calendar Agent
├── Contact Database
├── Telegram Bot
└── README.md
```

---

# 🛠️ Tech Stack

### Languages

- JavaScript (n8n Expressions)
- JSON

### AI Models

- OpenAI GPT-4.1 Mini
- OpenAI Whisper

### Automation

- n8n

### APIs & Services

- Telegram Bot API
- Gmail API
- Google Calendar API
- Google Sheets API
- OpenAI API

### Database

- Google Sheets (Contact Database)

---

# ⚙️ Workflows

## 1. Main AI Agent

Acts as the brain of the assistant.

### Responsibilities

- Understand user requests
- Decide which tool to use
- Maintain conversation memory
- Route tasks to Email or Calendar Agent
- Verify contacts before actions

---

## 2. Email Agent

Handles Gmail automation.

### Features

- Send Emails
- Read Emails
- Search Emails
- Compose Professional Emails
- Reply to Emails

### AI Capabilities

- Professional email drafting
- Subject generation
- Email summarization
- Placeholder removal
- Automatic sign-off

---

## 3. Calendar Agent

Automates Google Calendar.

### Features

- Create Events
- Create Events with Attendees
- Get Today's Events
- Event Summaries
- Automatic 60-minute event duration

---

## 4. Contact Database

Google Sheets stores contact information.

Example

| Name | Email |
|------|-------|
| John Doe | john@example.com |
| Sarah | sarah@example.com |

Before any email or meeting:

```
Search Contact
        │
Found?
 ├── Yes → Continue
 └── No → Ask User
```

---

# 🎙️ Voice Support

The assistant supports voice commands.

Flow

```
Voice Message
      │
Telegram
      │
Whisper API
      │
Text
      │
AI Agent
      │
Action
```

---

# 📧 Email Automation

Supported commands:

- Send an email
- Read my latest emails
- Reply to an email
- Search emails
- Forward emails

Example

```
Send an email to John saying
I'll join tomorrow's meeting.
```

---

# 📅 Calendar Automation

Supported commands:

- Schedule meetings
- Check today's schedule
- Add attendees
- Get upcoming events

Example

```
Schedule a meeting with Sarah tomorrow at 3 PM.
```

---

# 👥 Contact Management

Contacts are retrieved from Google Sheets before sending emails or creating meetings.

This prevents incorrect email addresses and ensures reliable communication.

---

# 🧠 AI Memory

The assistant remembers previous conversations using n8n Memory Buffer.

Example

User:

```
Schedule a meeting with John.
```

Later

```
Move it to Friday.
```

The assistant understands **"it"** refers to the previous meeting.

---

# 🔄 Workflow Overview

```
Telegram Message
        │
        ▼
Text / Voice
        │
        ▼
OpenAI
        │
        ▼
Main AI Agent
        │
 ┌──────┴─────────┐
 │                │
 ▼                ▼
Email Agent   Calendar Agent
 │                │
 ▼                ▼
 Gmail       Google Calendar
        │
        ▼
Telegram Reply
```

---

# 🔐 Integrations

- OpenAI
- Telegram
- Gmail
- Google Calendar
- Google Sheets
- n8n

---

# 📌 Example Commands

### Email

```
Send an email to John saying I will be late.
```

### Calendar

```
Schedule a meeting tomorrow at 5 PM.
```

### Events

```
What meetings do I have today?
```

### Contacts

```
Find Sarah's email.
```

### Voice

Simply send a voice message to the Telegram bot.

---

# 💡 Future Improvements

- WhatsApp Integration
- Slack Integration
- Microsoft Outlook Support
- Google Drive Integration
- OCR for Documents
- AI Task Management
- Reminder Notifications
- Multi-language Support

---

# 🎯 Skills Demonstrated

- AI Agent Development
- Workflow Automation
- Prompt Engineering
- API Integration
- OpenAI Integration
- Gmail Automation
- Google Calendar Automation
- Google Sheets Integration
- Telegram Bot Development
- Voice AI
- Conversational Memory
- n8n Automation
- REST APIs
- LLM Applications

---

# 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Ved Prakash**

- GitHub: https://github.com/vedprakash2004
- LinkedIn: https://linkedin.com/in/ved-prakash16/

⭐ If you found this project useful, consider giving it a Star!
