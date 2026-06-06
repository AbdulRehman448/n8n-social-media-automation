# 📱 Social Media Content Automation Pipeline — n8n

An AI-powered content automation system that fetches trending articles daily, generates viral LinkedIn posts using Gemini AI, delivers them to your inbox, and tracks everything in a Google Sheets content calendar — fully hands-off.

## 🚀 What It Does

- 📡 Reads RSS feed sources from Google Sheets (TechCrunch, MIT AI, HackerNews, VentureBeat)
- 🔍 Filters only articles published in the last 24 hours
- 🔄 Checks for duplicates — never generates the same post twice
- 🧠 Generates engaging LinkedIn posts using **Gemini AI** with hooks, insights, and hashtags
- 📧 Delivers ready-to-post content to your email daily
- 📊 Saves all posts to a Google Sheets content calendar with status tracking
- ⏰ Runs automatically every 24 hours — zero manual effort

## 🏗️ Workflow Architecture
Daily Schedule → Read RSS Sources → Fetch RSS Feed → Filter Recent Articles →
Check Skip → Fetch Existing Posts → Duplicate Check → Check Duplicate Skip →
Generate LinkedIn Post (Gemini) → Prepare Post Data →
Save to Content Calendar → Email Post to Self

## ✨ Advanced Features

- **Multi-source RSS** — reads from multiple feeds simultaneously
- **Recency filter** — only articles from last 24 hours qualify
- **Duplicate prevention** — cross-checks Content Calendar before generating
- **AI-powered hooks** — Gemini writes human-sounding posts with viral openers
- **Content calendar** — full history of generated posts in Google Sheets
- **Email delivery** — one-click copy-paste to LinkedIn

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| n8n Cloud | Workflow orchestration |
| Google Gemini AI | LinkedIn post generation |
| RSS Feed Reader | Article fetching from multiple sources |
| Google Sheets | RSS source management + content calendar |
| Gmail OAuth2 | Daily email delivery of generated posts |

## 📋 Google Sheets Structure

**RSS Sources tab:**
| url | category |
|-----|----------|
| https://feeds.feedburner.com/TechCrunch | Technology |
| https://news.mit.edu/rss/topic/artificial-intelligence2 | AI |
| https://hnrss.org/frontpage | Startup |
| https://feeds.feedburner.com/venturebeat/SZYF | AI Business |

**Content Calendar tab:**
`title | source_url | category | generated_post | status | created_at`

## ⚙️ Setup

1. Import `workflow.json` into n8n Cloud
2. Connect Google Sheets OAuth2 credentials
3. Connect Gmail OAuth2 credentials
4. Connect Google Gemini API key
5. Create Google Sheet with RSS Sources and Content Calendar tabs
6. Update Spreadsheet ID in all Google Sheets nodes
7. Activate workflow — runs daily automatically

## 📬 Contact

**Abdul Rehman Ali**
[LinkedIn](https://www.linkedin.com/in/abdul-rehman-ali/) | 
[Portfolio](https://abdulrehmanali.netlify.app/) | 
abdulrehman.tp.786@gmail.com
