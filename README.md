# Reverse Email Lookup | Email to LinkedIn

**Reverse email lookup.** Paste emails and get the LinkedIn name, headline, company, location, skills, and profile URL, or a clear `hasLinkedIn: false` when no exact match exists. Starting from $0.60 per 1,000 emails.
## If you need a different Mawsool Actor

| If this is what you need | Open |
| --- | --- |
| You have a name and company and want the profile URL. | [LinkedIn Profile Finder](https://apify.com/oday/mawsool-linkedin-profile-finder) |
| You have a profile URL and want the personal email. | [LinkedIn Email Finder](https://apify.com/oday/mawsool-linkedin-personal-email-finder) |
| You only need the current employer, before paying for a full profile. | [Current Company Checker](https://apify.com/oday/mawsool-linkedin-company-checker) |
| You want the current company and headline, and you will compare them to your CRM yourself. | [Profile Freshness Check](https://apify.com/oday/mawsool-linkedin-profile-freshness) |
| You want an alert when the employer or headline changes. | [Job Change Tracker](https://apify.com/oday/mawsool-linkedin-job-change-watch) |
| You have a profile URL and want the full profile. | [LinkedIn Profile Scraper](https://apify.com/oday/mawsool-linkedin-profile-details) |
| You have a large file of profile URLs. | [Mass Profile Scraper](https://apify.com/oday/mawsool-mass-linkedin-profile-scraper) |
| You want the current employer's website from a profile URL. | [Profile to Company Website](https://apify.com/oday/mawsool-linkedin-profile-to-company-website) |
| You want the job history only. | [Work Experience](https://apify.com/oday/mawsool-linkedin-profile-experience) |
| You want schools and degrees only. | [Education](https://apify.com/oday/mawsool-linkedin-profile-education) |
| You want a yes or no for one certificate. | [Certification Checker](https://apify.com/oday/mawsool-linkedin-certification-checker) |
| You want certificates, patents, courses, and publications. | [Certifications and Patents](https://apify.com/oday/mawsool-linkedin-profile-credentials) |
| You want likes and comments for outreach. | [Profile Activity](https://apify.com/oday/mawsool-linkedin-profile-activity) |
| You have a company URL and want the full company record. | [Company Details](https://apify.com/oday/mawsool-linkedin-company-details) |
| You have a large file of company URLs. | [Mass Company Scraper](https://apify.com/oday/mawsool-mass-linkedin-company-scraper) |
| You want the website, industry, and employee range. | [Firmographics and Website](https://apify.com/oday/mawsool-linkedin-company-firmographics) |
| You want office addresses. | [Company Locations](https://apify.com/oday/mawsool-linkedin-company-locations) |
| You want lookalike companies. | [Similar Companies](https://apify.com/oday/mawsool-linkedin-similar-companies) |
| You want the recent posts on a company page. | [Company Posts](https://apify.com/oday/mawsool-linkedin-company-posts) |
| You want only new posts on the next scheduled run. | [Company Post Monitor](https://apify.com/oday/mawsool-linkedin-company-post-watch) |

The same list is on [Mawsool's Apify profile](https://apify.com/oday).

## Use with AI agents

Apify exposes this Actor to ChatGPT, Claude, Gemini, Grok, and other agents through the Apify MCP server. Tell the agent the input you have, the fields you want back, and the starting price on this page. If you already have profile URLs and only need the current company and headline, use [Profile Freshness Check](https://apify.com/oday/mawsool-linkedin-profile-freshness) first and compare the result to your CRM yourself.

 A visitor who starts on one Actor can open the rest from that page.


This **reverse email lookup** Actor is powered by **Mawsool** (1B+ verified B2B contacts). It is built for **sales outreach, recruiting, CRM enrichment, Clay, HubSpot, and Salesforce** — not for guessing profiles from similar names.

> **If `hasLinkedIn` is `true`, that LinkedIn profile belongs to that email.** Exact matches only. No false positives.

**From ~$2 per 1,000 emails.** Export CSV, Excel, or JSON. Run in the UI, via Apify API, Zapier, Make, or Scheduler.

### What’s new (reliability upgrade)
- Larger dedicated lookup pool for higher success rates under load  
- Automatic retry on temporary API hiccups  
- Fallback API path if the primary endpoint is unreachable  
- **Paid Apify plans get automatic per-lookup discounts** (tiered PPE pricing rolling out)

**Mawsool enrichment suite on Apify:**
| Need | Actor |
|------|-------|
| Email → LinkedIn | **This Actor** |
| Name + company → LinkedIn | [LinkedIn Profile Finder by Name & Company](https://apify.com/oday/mawsool-linkedin-profile-finder) |

---

## Ready-made CRM enrichment recipes (example tasks)

One-click, pre-configured examples — open one, press Start, and adapt the input to your own list:

| Use case | Example task |
|----------|--------------|
| See how reverse email lookup works | [Reverse email lookup demo](https://apify.com/oday/mawsool-email-linkedin-lookup/examples/reverse-email-lookup-demo) |
| Verify prospect emails before outreach | [Enrich sales leads from email](https://apify.com/oday/mawsool-email-linkedin-lookup/examples/enrich-sales-leads-from-email) |
| Add LinkedIn data to HubSpot / Salesforce contacts | [CRM contact enrichment from email](https://apify.com/oday/mawsool-email-linkedin-lookup/examples/crm-contact-enrichment-from-email) |
| Remove dead contacts from your CRM | [Clean CRM email list](https://apify.com/oday/mawsool-email-linkedin-lookup/examples/clean-crm-email-list) |
| Refresh outdated job titles & companies | [Update stale CRM contacts](https://apify.com/oday/mawsool-email-linkedin-lookup/examples/update-stale-crm-contacts) |

**Typical CRM workflow:** export contact emails from HubSpot, Salesforce, or Pipedrive → run this Actor → filter `hasLinkedIn = true` → import verified LinkedIn URLs, titles, and companies back into your CRM. Schedule it monthly to keep records fresh.

---

## What does reverse email lookup do?

**Reverse email lookup** (also called email-to-LinkedIn, find person by email, or email enrichment) takes an email address and returns the person behind it.

This Actor specifically answers:

- *Who owns this email?*
- *What is their LinkedIn profile URL?*
- *What is their name, job title / headline, company, and location?*

Unlike generic enrichers that return fuzzy or outdated database hits, Mawsool returns **exact verified LinkedIn matches only**. Uncertain or fuzzy results are returned as `hasLinkedIn: false`.

---

## Find LinkedIn profile from email — sample output

### LinkedIn profile found

```json
{
  "email": "jane.doe@acme.com",
  "hasLinkedIn": true,
  "matchType": "exact",
  "fullName": "Jane Doe",
  "firstName": "Jane",
  "lastName": "Doe",
  "headline": "VP Sales at Acme Inc",
  "linkedinUrl": "https://www.linkedin.com/in/janedoe",
  "company": "Acme Inc",
  "location": "New York, NY",
  "skills": "Sales; SaaS; B2B",
  "checkedAt": "2026-07-26T12:00:00.000Z",
  "success": true
}
```

### No LinkedIn match for this email

```json
{
  "email": "unknown@company.com",
  "hasLinkedIn": false,
  "matchType": "none",
  "fullName": "",
  "linkedinUrl": "",
  "success": true
}
```

Every row is **flat** (CSV-ready). Full API payload is also available in `profileRawJson` and `profileFlattenedJson` when variable fields (skills, education, work history) differ per person.

---

## Why use this email to LinkedIn tool?

| Feature | Generic enrichers | **This Actor (Mawsool)** |
|---------|-------------------|--------------------------|
| Match quality | Often fuzzy / guessed | **Exact LinkedIn matches only** |
| False positives | Common | **Rejected by design** |
| Output | Basic name / company | **Full LinkedIn profile fields** |
| Export | Varies | **CSV, Excel, JSON** |
| Pricing | Subscriptions | **Pay per email** (~$2 / 1k) |
| Integrations | Limited | **Apify API, Zapier, Make, Scheduler** |

---

## Who uses email to LinkedIn lookup?

### Sales & outbound teams
Enrich cold email lists with **verified LinkedIn URLs** before connection requests or personalized outreach. Stop messaging emails with no professional identity.

### Recruiters & talent teams
Confirm that a candidate application email maps to the **real LinkedIn profile** — not a similarly named stranger.

### RevOps & CRM enrichment
Pipe results into **HubSpot, Salesforce, Pipedrive, Clay, or Google Sheets**. Append LinkedIn data to contacts via Apify API, webhooks, Zapier, or Make.

### Lead scoring & growth
Prioritize leads where email → LinkedIn verification succeeds. Build scoring on **confirmed** identity data.

### Developers & data engineers
Batch-process thousands of emails with the Apify API. Schedule nightly enrichment runs. Export datasets programmatically.

---

## How to find LinkedIn from email (3 steps)

1. **Paste emails** into the `emails` input (or upload from CSV)
2. **Click Start** — each email is verified in seconds
3. **Export results** as CSV, Excel, or JSON from the Output / Dataset tab

### Run reverse email lookup via API

```bash
apify call oday/mawsool-email-linkedin-lookup \
  --input '{"emails":["prospect@company.com"]}'
```

### Bulk email enrichment

Set `maxEmails` up to **10,000** per run, or schedule multiple runs for larger lists. Ideal for CRM exports and outbound sequences.

---

## Data you get from each email

| Field | Description |
|-------|-------------|
| `email` | Input email address |
| `hasLinkedIn` | `true` only on exact LinkedIn match |
| `matchType` | `exact` or `none` |
| `fullName`, `firstName`, `lastName` | Verified name |
| `headline`, `summary` | Professional headline & bio |
| `linkedinUrl` | Direct LinkedIn profile URL |
| `company`, `location` | Current company & location |
| `pictureUrl`, `reportProfileUrl` | Photo & report links |
| `skills`, `educationHistory`, `positionHistory` | Skills & career history |
| `profileRawJson` | Full raw profile JSON (variable fields preserved) |
| `profileFlattenedJson` | Flattened key/value profile for flexible export |
| `checkedAt` | Verification timestamp |

---

## Pricing — pay per email verified

One `email-lookup` event = one email processed.

| Plan tier | Per email | Per 1,000 emails |
|-----------|-----------|------------------|
| Free | $0.002 | **$2.00** |
| Bronze | $0.0018 | $1.80 |
| Silver | $0.0015 | $1.50 |
| Gold, Platinum, and Diamond | $0.0006 | $0.60 |

Higher Apify plans unlock lower rates automatically. No separate Mawsool subscription required on Apify.

---

## Integrations for LinkedIn email enrichment

- **Apify API** — run reverse email lookup at any scale
- **Webhooks** — trigger workflows when enrichment finishes
- **Zapier & Make** — no-code email → LinkedIn automation
- **Google Sheets** — export enriched contacts in one click
- **CRM tools** — HubSpot, Salesforce, Pipedrive, Clay via API or middleware
- **Scheduler** — nightly bulk enrichment of new leads

---

## Reverse email lookup vs LinkedIn email scraper

| Direction | Tool |
|-----------|------|
| **Email → LinkedIn** (this Actor) | You have emails; you want LinkedIn profiles |
| LinkedIn → Email | You have LinkedIn URLs; you want work emails |

If your goal is **find LinkedIn from email**, use this Actor. If you need the opposite (email finder from LinkedIn URL), use a LinkedIn email scraper instead.

---

## About Mawsool

Mawsool is a B2B lead intelligence platform:

- **1B+ verified global contacts**
- **Exact-match reverse email verification**
- **Real-time lookup**, not stale quarterly dumps
- Strong coverage including markets others miss

This Actor brings Mawsool’s **email to LinkedIn** verification to the Apify Store.

**Support:** [support@mawsool.tech](mailto:support@mawsool.tech)  
**Open-source CLI (thin client):** [github.com/odayali1/mawsool-cli](https://github.com/odayali1/mawsool-cli)

---

## FAQ — reverse email lookup & email to LinkedIn

### How do I find a LinkedIn profile from an email address?
Paste the email into this Actor, run it, and check `linkedinUrl` when `hasLinkedIn` is `true`. That is a verified reverse email lookup — email to LinkedIn in one step.

### Is reverse email lookup the same as email enrichment?
Yes for this use case. Email enrichment often returns name, company, and LinkedIn. This Actor focuses on **verified LinkedIn profile data** from the email.

### Does this guess LinkedIn profiles from similar names?
No. Only **exact verified matches** return `hasLinkedIn: true`. Fuzzy or uncertain hits return `hasLinkedIn: false`.

### Can I do bulk email to LinkedIn lookup?
Yes. Submit up to 10,000 emails per run with `maxEmails`, or schedule multiple runs for larger CRM lists.

### What if the email has no LinkedIn profile?
You get `hasLinkedIn: false` and empty profile fields — a clean result you can filter on. You are still charged for the lookup attempt (pay per email processed).

### Does it work with personal Gmail / Outlook emails?
Yes, when that personal email is linked to a verified LinkedIn identity. Many work emails have higher match rates.

### Can I export to CSV for HubSpot or Clay?
Yes. Export the dataset as CSV/Excel, or pull via Apify API into Clay, HubSpot, Zapier, or Make.

### Is this a LinkedIn scraper?
No. It does not scrape LinkedIn pages or require LinkedIn login/cookies. It performs **reverse email lookup** against Mawsool’s verified contact intelligence and returns exact LinkedIn matches.

### How much does email to LinkedIn cost?
From **$2 per 1,000 emails** on Free/Starter plans, with volume discounts on higher Apify plans.

---

## Limitations

- Exact matches only — fuzzy results are reported as not found (by design, for accuracy)
- Coverage depends on Mawsool’s verified contact graph for each email
- Requires active Mawsool API capacity on the backend

---

## Keywords & related searches

People use this Actor when searching for: **email to LinkedIn**, **find LinkedIn from email**, **reverse email lookup**, **email enrichment**, **LinkedIn profile finder**, **find person by email**, **B2B contact enrichment**, **CRM LinkedIn enrichment**, **email to LinkedIn API**, and **bulk reverse email search**.
