🤖 AI Agent Portfolio — Recor Multas Automation Stack
> **Pedro Bragança** | Python Automation Engineer | AI Agents | RPA | WhatsApp Bots  
> Belo Horizonte, Brazil 🇧🇷 | Available for freelance projects
---
Overview
I'm the founder of Recor Multas, a Brazilian legal-tech company specialized in traffic fine defense and fleet infraction management. Over the past year, I built a full internal ecosystem of autonomous AI agents that run in production daily — handling lead generation, data extraction, content publishing, monitoring, and WhatsApp outreach.
Every agent described below is live, battle-tested, and deployed on a Ubuntu 24.04 VPS.
---
🔴 Agent: Flash — RPA Data Extraction Bot
Status: ✅ Live in Production  
Priority: Core business agent
What it does
Flash is a fully autonomous RPA agent that monitors 30+ Brazilian government traffic portals (DETRAN, municipal MG portals) daily. It extracts vehicle license plates from official infraction bulletins, then queries a parallel web platform to retrieve the vehicle owner's personal data (Name, CPF, Phone, Email) using cookie-based session persistence.
Key Features
Scrapes 30+ government portals on a scheduled basis
Session persistence with cookie management (no re-login overhead)
Human-like behavior: randomized delays (30–90s between requests, 5-min pause every 10 queries)
Filters results using an 84-code CNH suspension rule list
Outputs structured data to Google Sheets and Excel
Sends real-time WhatsApp notifications via Evolution API when new leads are found
Stores all records in Notion database
Stack
`Python` · `Selenium / Playwright` · `Google Sheets API` · `Evolution API (WhatsApp)` · `Notion API` · `Ubuntu VPS (cron)`
---
🟠 Agent: Daredevil — B2B Lead Capture Agent
Status: ✅ Deployed  
Priority: Revenue generation
What it does
Daredevil is a B2B lead generation agent that targets fleet and transportation companies in the Greater Belo Horizonte area. It scrapes Google Maps for relevant businesses, enriches each lead with full company data via the CNPJ.ws API (Brazil's public business registry), and triggers automated outreach via Gmail SMTP and WhatsApp.
Key Features
Google Maps scraping by niche + city keyword
Automatic company data enrichment (CNPJ, legal name, phone, email, address, activity code)
Multi-channel outreach: Email (Gmail SMTP) + WhatsApp (Evolution API)
Deduplication to avoid contacting the same company twice
Outputs leads to structured spreadsheets
Stack
`Python` · `Google Maps API` · `CNPJ.ws API` · `Gmail SMTP` · `Evolution API (WhatsApp)` · `Google Cloud`
---
🟡 Agent: Loki — Content Publishing & SEO Automation
Status: ✅ Live in Production
What it does
Loki automates the entire blog content pipeline for recormultas.com. It generates SEO-optimized articles using Claude Sonnet, publishes them via the Django CMS, and immediately submits each URL to the Google Indexing API to accelerate search engine crawling.
Key Features
AI article generation with Claude Sonnet (high writing quality)
Automatic publishing to Django-based CMS
Google Indexing API integration — submits each article immediately after publishing
Successfully indexed 25+ articles in production
Google Cloud service account with proper IAM permissions
Stack
`Python` · `Django` · `Claude API (Sonnet)` · `Google Indexing API` · `Google Cloud (Service Account)`
---
🔵 Agent: Wanda — UX Monitoring Agent
Status: ✅ Live in Production
What it does
Wanda monitors the recormultas.com website daily for UX issues, broken pages, and user experience anomalies. It uses Gemini Flash for cost-efficient analysis and sends a WhatsApp report every morning at 9am.
Key Features
Daily automated UX audit via cron job (9am)
AI-powered analysis with Gemini 1.5 Flash (free tier — zero cost)
WhatsApp report delivery via Evolution API
Flags broken links, slow pages, and layout issues
Stack
`Python` · `Gemini 1.5 Flash API` · `Evolution API (WhatsApp)` · `Cron (Ubuntu)`
---
🟣 Agent: Friday — WhatsApp Communication Hub
Status: ✅ Live in Production
What it does
Friday is the central WhatsApp instance powering all agent notifications and outreach across the entire ecosystem. All agents (Flash, Daredevil, Wanda) route their WhatsApp messages through Friday.
Key Features
Central Evolution API WhatsApp instance
Used by multiple agents simultaneously
Handles both automated outreach and internal alert notifications
Migrated to Gemini 1.5 Flash for AI responses (cost optimization)
Stack
`Evolution API` · `WhatsApp Business` · `Gemini 1.5 Flash`
---
🟢 Agent: Fury — Instagram Content Automation
Status: ✅ Live in Production
What it does
Fury automates Instagram carousel creation for social media marketing. It works in tandem with Loki, taking blog articles and transforming them into 1080x1080px carousel images ready for Instagram.
Key Features
Automated carousel generation from blog content
Output: 1080x1080px images saved to media pipeline
Integrated with Loki's content workflow
Migrated to Gemini 1.5 Flash (free tier)
Stack
`Python` · `Gemini 1.5 Flash` · `Image generation pipeline`
---
Infrastructure Overview
```
VPS: Ubuntu 24.04 LTS (Hostinger)
Framework: Python / Django
Deployment: Cron jobs + standalone scripts
AI Models: Claude Sonnet, Gemini 1.5 Flash
APIs: Google Maps, Google Sheets, Google Indexing,
      Gmail SMTP, Evolution API (WhatsApp), Notion,
      CNPJ.ws, Claude API, Gemini API
Version Control: GitHub (private)
```
---
What I Can Build For You
Based on this production stack, I'm available to build:
Service	Delivery	Starting at
Lead scraping agent (Google Maps + enrichment)	5–7 days	$800
WhatsApp outreach automation	3–5 days	$600
RPA bot for portal/website data extraction	7–10 days	$1,200
Full pipeline (scrape → enrich → notify)	10–14 days	$1,800
Content automation + SEO indexing pipeline	7 days	$900
---
Let's Talk
I build systems that run autonomously in production — not just prototypes.  
If you have a repetitive data or outreach problem, I can automate it.
> 📩 Available on Upwork | Fixed-price projects preferred
