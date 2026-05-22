# Paid Media Digest — New Client Briefing Guide
How to set up the weekly digest for a new client
*Template version based on DealRoom digest · Last updated April 2026*

---

## Overview

This document tells Claude everything it needs to know to build and maintain a weekly paid media digest for a new client. Drop this file into a new Claude Project along with the client's ICP and account files and Claude will generate a digest in the same format used for DealRoom, adapted to the client's channels, KPIs, and targeting.

The digest is an interactive HTML file with tabbed sections. It is generated fresh each week from CSV exports and is designed to be shared directly with clients or discussed on a weekly call. It covers wasted spend, cross-channel correlation, target account engagement, ad copy performance, and one prioritized recommendation per week.

---

## Step 1 — Create a New Claude Project

Go to Claude.ai and create a new Project for the client. One project per client. This keeps their data, memory, and context completely isolated from other clients.

Name the project clearly, e.g. "[Client Name] — Paid Media". This becomes the persistent workspace for all weekly digest conversations.

---

## Step 2 — Upload Foundational Files

These files only need to be uploaded once at the start. They give Claude the context it needs to interpret data correctly every week without re-explaining.

### Required Files

**1. Website URL**
A plain text file containing the client's website URL. Claude uses this to understand their product, messaging, and landing page structure.
Example: `https://clientwebsite.com`

**2. ICP Definition**
The client's Ideal Customer Profile, including:
- Tier definitions (e.g. S01, S02, S03 or equivalent)
- Qualifying criteria per tier (e.g. number of acquisitions, revenue, employee count)
- Target geographies
- Target industries (included and excluded)

This can be a PDF, image, or plain text document.

**3. Target Job Title Criteria**
Two lists: High Fit and Medium Fit job titles.
Format: 'Job title contains any of X, Y, Z. Job title does not contain any of A, B, C.'
These are used to categorize demo requests by ICP fit in Google Ads and to assess LinkedIn lead quality. Matches the conversion column 'HS - Demo High/Med Fit' in Google Ads exports.

**4. Target Accounts List**
A CSV of named target accounts (company names). Used to cross-reference LinkedIn company engagement data and flag which ICP accounts are warming up. Can be a single file or multiple files — Claude will deduplicate on company name. This list can be updated whenever the client refreshes their ABM list.

**5. Paid Ad Strategy Doc** *(optional but recommended)*
Any brief, one-pager, or slide deck describing active campaigns, creative direction, and messaging strategy. Helps Claude assess whether ad copy is on-brand and aligned with current campaign goals. PDF or image format works.

---

## Step 3 — Have the Briefing Conversation

After uploading the foundational files, start a conversation in the new Project with a message like:

> *"I'm setting up a new client digest. I've uploaded their ICP, target job titles, target accounts, and website. Their channel mix is Google Ads + LinkedIn. Their primary conversion goal is [demo request / free trial / form fill]. Their CRM is [HubSpot / Salesforce / other]. Please review the files and tell me exactly what weekly exports you'll need from me."*

Claude will respond with the exact file list and column requirements based on their specific setup.

---

## Step 4 — Weekly Export Checklist

This is the standard file set based on the DealRoom model. Adjust based on the client's active channels and any differences Claude flags during the briefing conversation.

### Google Ads Exports

Pull all four from Google Ads UI. Before downloading: **Segment → Time → Week**. Confirm the HS Demo Request and HS - Demo High/Med Fit conversion columns are visible.

| File | Source | Date Range | Notes |
|------|--------|------------|-------|
| Campaign report | Google Ads | Last 7 days | Segmented by week. Include HS Demo Request + HS High/Med Fit columns. |
| Ad group report | Google Ads | Last 7 days | Segmented by week. Same conversion columns. |
| Search terms report | Google Ads | Last 7 days | Used for wasted spend and keyword add opportunities. |
| Ad report | Google Ads | YTD | Not date-segmented. Used for copy analysis. Pull once monthly or when ads change. |
| Keyword report | Google Ads | Last 7 days | Optional but useful for keyword-level fit demo analysis. |

### LinkedIn Ads Exports

Pull from LinkedIn Campaign Manager. LinkedIn doesn't support weekly segmentation — use daily breakdowns and Claude will roll them up to weekly.

| File | Source | Date Range | Notes |
|------|--------|------------|-------|
| Ad Set Performance Report | LinkedIn CM | YTD (daily) | Campaign-level daily data. Gives spend, clicks, leads, CTR by campaign and ad set. |
| Company Engagement Report | LinkedIn CM | Last 90 days | Powers the Target Accounts section. Shows which ICP companies are engaging with ads. |

---

## Step 5 — Send the First Data Drop

The first upload should be YTD data to establish a baseline. This is the equivalent of the January–April export used to build the DealRoom baseline digest.

Send the message:

> *"Here are the first exports — this is YTD data. Please review and build the first digest using the same format as DealRoom. I've also attached the DealRoom digest HTML as a template reference."*

Attach: all 7 CSV files + the DealRoom digest HTML file from this project's outputs folder.

Claude will read the files, flag any data questions (missing columns, unexpected formats), and generate the first digest as an interactive HTML file.

---

## Digest Structure Reference

The digest has 7 tabs:

| Tab | What It Shows | Adapts When... |
|-----|---------------|----------------|
| 📊 Pulse | Top-line metrics: total spend, demo requests, fit demos, CPD, CPFit. Monthly trend tables for Google and LinkedIn side by side. | KPI labels change based on the client's conversion goal. Monthly tables expand as more weeks accumulate. |
| 🔗 Correlation | Cross-channel view: LinkedIn spend/clicks vs. Google Brand demo requests. The core thesis — LinkedIn warms, Google Brand captures. | If the client doesn't run LinkedIn, this tab becomes a channel mix or funnel view instead. If they have a longer sales cycle, the lag window adjusts. |
| 🔍 Keyword Ops | Wasted spend (high cost, zero conversions), match type leaks, VDR-intent or wrong-category bleed, and keyword add opportunities in three tiers. | The negative keyword patterns change by client category. Keyword add candidates are always pulled from search term data specific to their account. |
| 🎯 Target Accounts | LinkedIn company engagement cross-referenced against the target accounts list. Shows reach, clicks, leads, and engagement tier per ICP account. | Requires the company engagement export and a target accounts list. If the client has no ABM list, this tab shows top engaging companies by industry or segment instead. |
| 📣 Ad Mix | LinkedIn campaign structure and CPL by ad set. Google campaign health flags (what's working, what's underperforming, what to pause). | Adapts to whatever campaigns are active. Meta, Reddit, or other channels can be added as additional cards within this tab. |
| ✍️ Copy Insights | Top and bottom Google RSA assets by CTR/leads. LinkedIn ad set CTR as creative proxy. Draft new headlines, descriptions, and LinkedIn intro themes. Landing page alignment notes. | The draft asset suggestions are always grounded in what's converting in that specific account — not generic copy. |
| ⚡ Recommendation | One primary action and one quick win per week. Sales handoff: top 3-5 ICP accounts to flag. Watch list for the following week. | The recommendation logic stays consistent. The sales handoff section only appears when there are target accounts with lead + engagement signal. |

---

## What to Tell Claude in the New Project

The more context you provide upfront, the less you'll need to re-explain week to week.

### Client Context
- What does the client sell and who buys it?
- What is their primary conversion event? (demo, trial, form fill, call)
- What do they call their ICP segments internally?
- What CRM do they use? (affects conversion column names)
- Are there any campaigns or channels NOT to analyze? (e.g. brand campaigns managed separately)
- Any known seasonality? (e.g. fiscal year timing, industry events)

### Data Context
- What channels are active? (Google, LinkedIn, Meta, Reddit, etc.)
- What are the exact conversion column names in their Google Ads exports?
- Is the LinkedIn company export available or do they not use ABM?
- Are there any paused campaigns still in the data that should be excluded?
- Is the account in USD or another currency?
- Any known data quality issues or tracking gaps to be aware of?

---

## Tips for Ongoing Use

### Keeping the digest consistent week to week
- Always upload files in the same Project conversation thread (or a new thread within the same Project).
- If the digest format drifts, paste the previous week's HTML and say 'keep this structure, update the data.'
- The digest filenames include the date range — save them locally by client for easy reference.

### When the client changes something
- **New campaign launched:** mention it when uploading the next week's files — Claude will incorporate it automatically.
- **ICP tiers updated:** re-upload the ICP definition file and note what changed.
- **Target accounts list refreshed:** re-upload the CSV and note 'this replaces the previous list.'
- **New conversion event added in Google Ads:** let Claude know the exact column name it will appear under in exports.

### Adding channels (Meta, Reddit, etc.)
- Tell Claude the channel and what exports are available (most platforms export CSV performance data).
- The digest will gain a new card in the Ad Mix tab and the Pulse tab will expand to include the new channel's top-line metrics.
- The Correlation tab logic may also shift depending on how the new channel fits into the funnel.

---

*Paid Media Digest Briefing Guide · Template based on DealRoom v2 (April 2026) · Adapt freely for each client.*
