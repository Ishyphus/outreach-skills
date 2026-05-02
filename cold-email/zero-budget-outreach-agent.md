# Skill: Zero-Budget Outreach Agent

## What This Is

A zero-subscription outreach agent that finds, verifies, and emails 
leads using only a browser, Gmail, and free tools. No Apollo. No 
Instantly. No Clay. Just the internet and a sending inbox.

Works for both local businesses (Google Maps) and B2B companies 
(Google Search). Automates what it can, guides the user through 
what it can't.

---

## Stack

| Function | Tool | Cost |
|---|---|---|
| Lead finding | Google Search + Google Maps | Free |
| Lead enrichment | Hunter.io (free tier) + LinkedIn | Free |
| Email verification | NeverBounce free checker / Mailtester.com | Free |
| Sending | Gmail (personal inbox) | Free |
| Tracking | Mailtrack Gmail extension | Free |
| Storage | Google Sheets | Free |

---

## Workflow

### STAGE 1 — Define the Target

Before anything runs, answer these:

- What industry or business type are you targeting?
- What location? (for Maps leads) or what company size / role? 
  (for B2B)
- What problem does your offer solve for them?
- What is the one outcome you can promise?

From these answers, generate:

1. A Google Maps search string → `[business type] in [city]`
2. A Google Search string → 
   `[role] at [company type] [location] site:linkedin.com`
3. An ICP one-liner to use when writing personalized emails

---

### STAGE 2 — Lead Finding

**Local leads via Google Maps**

1. Open Google Maps
2. Run the search string from Stage 1
3. Click each result and copy: business name, website, phone, 
   owner name if listed
4. Paste into Google Sheet

**B2B leads via Google Search**

1. Run the LinkedIn search string in Google
2. Open each profile and note: full name, job title, company, 
   company website
3. Go to Hunter.io → enter company domain → find email
4. Fallback if Hunter finds nothing: guess pattern 
   `first.last@company.com` and verify in Stage 3
5. Paste into Sheet

---

### STAGE 3 — Email Verification

For each email collected:

1. Go to mailtester.com or NeverBounce free checker
2. Paste the email
3. Mark result in Sheet: ✅ Valid / ❌ Invalid / ⚠️ Risky

**Rule:** Never send to unverified emails. Gmail will penalize 
the sending domain fast.

Skip anything marked Invalid or Risky.

---

### STAGE 4 — Email Writing

Use this structure for every lead:
Subject: [Specific to their situation — not generic]
Hi [First Name],
[One line showing you looked at their business — reference
something real: their location, niche, a gap you noticed]
[One line on what you do + the outcome, not the features]
[One low-friction CTA — not "let's hop on a call",
something smaller like "worth a quick reply?"]
[Your name]

Personalization variables by lead type:
- Maps leads → mention their city or business category
- B2B leads → mention their company name or role

One email per lead. Written to sound like it wasn't templated.

---

### STAGE 5 — Sending via Gmail

**Daily limit:** Max 20 emails per day from a personal Gmail.

1. Open Gmail
2. Paste the generated email for Lead 1
3. Send
4. Mark "Sent" in Sheet with date
5. Repeat for up to 20 leads per day

**Spacing rule:** Don't send all 20 at once. Spread across 
the day — morning, afternoon, evening. Gmail flags sudden 
volume spikes.

---

### STAGE 6 — Tracking

Install Mailtrack (free Gmail extension). Double tick = opened.

Track in Sheet:
- Date sent
- Opened? (update manually from Mailtrack)
- Replied?
- Follow-up due date (sent date + 3 days)

---

### STAGE 7 — Follow-Up

If no reply in 3 days, send one follow-up. Max 2 follow-ups 
per lead total. Then mark Dead and move on.

Follow-up structure:
Subject: Re: [original subject]
Hi [First Name],
Just bumping this up in case it got buried.
[One sentence — slightly different angle on the offer]
Still worth a quick reply if it's relevant.
[Your name]

Short. No guilt-tripping. No "I know you're busy."

---

## Google Sheet Template

| Lead # | Name | Business | Email | Verified | Sent Date | 
Opened | Replied | Follow-up Date | Status |

Color coding:
- Green = Replied positively
- Yellow = Follow-up due
- Red = Dead / bounced

---

## Limitations

- Stay under 20 emails/day to avoid Gmail spam flags
- Hunter.io free tier = 25 searches/month — use carefully
- No actual send automation — Gmail requires manual sending 
  without paid tools
- Mailtester.com has daily limits — batch verify in the morning

---

## What to Build Next

Once this is running and generating replies:

- Upgrade Hunter.io to paid for more searches
- Add Instantly free trial for sending at scale
- Move Sheet to Airtable for better pipeline view
