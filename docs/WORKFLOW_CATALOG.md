# Workflow Catalog

This catalog provides a quick overview of the workflows included in this repository. After importing, open each workflow to review required credentials, nodes, and configuration details.

## AI & Knowledge Workflows

| Workflow | Location | What it does | Notes |
| --- | --- | --- | --- |
| n8n AI Agent | `n8n-ai-agent.json` | AI agent starter workflow for task execution | Review LLM/tool credentials after import |
| RAG Chatbot (Google Drive + Gemini) | `RAG_Chatbot_for_Company_Documents_using_Google_Drive_and_Gemini.json` | Retrieval‑augmented chatbot from Drive docs | Requires Drive + LLM credentials |

## Marketing & Social

| Workflow | Location | What it does | Notes |
| --- | --- | --- | --- |
| Social Media Manager | `Social media manager.json` | Automates social media content tasks | Configure platform credentials |
| LinkedIn Auto‑post | `linkedin_autopost_n8n.json` | Publishes posts to LinkedIn | Ensure LinkedIn API access |
| Cold Email | `Cold email.json` | Outreach automation for cold email | Configure email service + lists |

## Research & Recruiting

| Workflow | Location | What it does | Notes |
| --- | --- | --- | --- |
| LinkedIn Jobs + Decision MakerResearch | `Linkedin Jobs Scraping and Decision MakerResearch.json` | Scrapes jobs and researches decision makers | Validate source limits and terms |

## Sales & Lead Generation

| Workflow | Location | What it does | Notes |
| --- | --- | --- | --- |
| Lead Scraper (Parent) | `Sales agent/Lead Scraper/Parent.json` | Orchestrates lead scraping flow | Parent/Child structure |
| Lead Scraper (Child) | `Sales agent/Lead Scraper/Child.json` | Child workflow used by Parent | Run via parent call |
| SDR Workflow | `Sales agent/Lead Scraper/SDR.json` | Sales development rep sequence | Customize outreach |
| Email Verifier | `Sales agent/Lead Scraper/Email_verifier__N8N_.json` | Verifies email validity | Configure verifier API |

## Avatar Agent (DM Automation)

| Workflow | Location | What it does | Notes |
| --- | --- | --- | --- |
| Main Workflow | `Avatar agent/DM AGENT - INSTA , FB/Main_workflow.json` | Core DM agent workflow | Configure socials + credentials |
| CRM Workflow | `Avatar agent/DM AGENT - INSTA , FB/CRM_workflow.json` | CRM‑related DM automation | Connect CRM tools |
| Calendar Workflow | `Avatar agent/DM AGENT - INSTA , FB/Calendar_workflow.json` | Calendar scheduling from DMs | Connect calendar provider |

## Utilities

| Workflow | Location | What it does | Notes |
| --- | --- | --- | --- |
| Subscription Tracker | `Subscription Tracker.json` | Tracks subscriptions | Configure data source |
| Subscription Tracker (legacy) | `My1st_workflow_of_n8n(Subscription Tracker)` | Early version of subscription tracking | Consider using the newer version |

---

Want a new workflow? Open a request in GitHub Issues and share:
- Use case
- Target apps/services
- Trigger + desired outputs
