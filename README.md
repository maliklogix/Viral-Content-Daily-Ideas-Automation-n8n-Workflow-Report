# Viral Content Daily Ideas Automation – n8n Workflow Report

## 1. Workflow Title

**Viral Content Daily Ideas for YouTube, TikTok & Instagram with Discord Notifications**

---

## 2. Purpose & Objective

This n8n workflow is designed to **automatically generate viral short‑form content ideas** based on current social media trends and distribute them across **Discord and Google Sheets** for content planning and execution.

The main goals are:

* Identify trending topics from the web
* Use AI to generate **high‑impact video ideas**
* Structure ideas for **short‑form platforms** (TikTok, Reels, Shorts)
* Deliver ideas to a Discord community
* Store ideas in Google Sheets for tracking and reuse

---

## 3. Target Platforms

* **TikTok**
* **Instagram Reels**
* **YouTube Shorts**
* **Discord** (distribution & notifications)
* **Google Sheets** (content planning database)

---

## 4. Workflow Triggering Methods

The workflow can be triggered in multiple ways:

1. **Schedule Trigger** – Runs automatically at a defined daily time
2. **Webhook Trigger** – Allows Discord commands like `!update`
3. **Execute Workflow Trigger** – Can be started by another n8n workflow

This makes the automation flexible for both **manual and scheduled execution**.

---

## 5. Data Source (Trend Collection)

### HTTP Request Node

* Fetches live trend data from **social-searcher.com**
* Example focus keyword: `AI`

### Markdown Node

* Converts raw HTML into readable text
* Prepares data for AI processing

---

## 6. AI Content Generation Engine

### AI Agent (TrendSage)

The AI agent is configured with a detailed system prompt to:

* Analyze social media trends
* Generate **viral video ideas**
* Optimize ideas for short‑form content
* Keep responses within Discord limits

### Output Structure (per idea)

Each idea includes:

* 🔥 Trend Title
* 🌐 Platform (TikTok / IG / YouTube Shorts)
* 📊 Trend Type (Sound, POV, Challenge, Niche)
* 📈 Trend Stats
* 🧠 Hook Idea (first 3 seconds)
* 💡 Key Points (why it works)
* 🎯 Call to Action (CTA)

The output is split into **3 parts** to ensure Discord message compatibility.

---

## 7. Structured Output Parsing

### Structured Output Parser

Ensures AI output follows a consistent JSON format:

* `part_1` – First set of ideas
* `part_2` – Continuation
* `part_3` – Final ideas & CTA

This makes the workflow reliable and automation‑safe.

---

## 8. Discord Integration

### Discord Nodes

* Each AI output part is sent as a **separate Discord message**
* Messages are posted to a dedicated channel: `#viral-content-ideas`

This enables:

* Daily inspiration for creators
* Community discussion
* Easy idea sharing

---

## 9. Google Sheets Integration

The workflow stores generated ideas across multiple sheets:

### Sheets Used

* **YouTube Sheet**
* **TikTok Sheet**
* **Instagram Sheet**

### Stored Fields

* Creation Date
* Content Summary
* Title
* Description
* Tags
* Trend Type
* Hook Idea
* CTA
* Thumbnail Link
* Video Link

This turns Google Sheets into a **content idea database**.

---

## 10. Title & Description Generator

A secondary AI agent:

* Converts raw content summaries into:

  * Clean titles
  * Platform‑ready descriptions

This helps creators move faster from **idea → publishing**.

---

## 11. Automation Flow Summary

1. Trigger activated (Schedule / Webhook / Manual)
2. Trend data fetched from web
3. AI analyzes trends
4. Viral video ideas generated
5. Output structured into parts
6. Ideas posted to Discord
7. Ideas saved to Google Sheets
8. Titles & descriptions refined by AI

---

## 12. Required Accounts & APIs

To run this workflow successfully, you need:

* n8n (self‑hosted or cloud)
* OpenAI API key
* Discord Bot Token
* Google Service Account
* Google Sheets access

---

## 13. Use Cases

* Content creators
* Social media agencies
* YouTube automation channels
* Discord creator communities
* Trend research teams

---

## 14. Key Benefits

* Fully automated content ideation
* Platform‑optimized ideas
* Community distribution via Discord
* Centralized content planning
* Scalable & reusable workflow

---

## 15. Future Improvement Ideas

* Add hashtag generation
* Add thumbnail prompt generation
* Add posting automation
* Add analytics feedback loop
* Multi‑language support

---

## 16. Author / Contact

**Malik Logix**
Email: [maliklogix@gmail.com](mailto:maliklogix@gmail.com)
YouTube: youtube/@maliklogix

---

