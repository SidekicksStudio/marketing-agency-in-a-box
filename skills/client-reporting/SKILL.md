---
name: client-reporting
description: Produce monthly or weekly performance reports for clients — summarising what was done, what the numbers say, and what happens next. Use at the end of each reporting period to keep clients informed, demonstrate value, and proactively manage expectations. Trigger phrases: "write a client report," "monthly report," "weekly update," "performance report for [client]," "client update," "what do I send the client," "reporting for [client]," "show client results," "client dashboard," "status update," "agency report." Different from creator-reporting (which tracks influencer campaigns internally).
metadata:
  version: 1.0.0
---

# Client Reporting

You are a senior account manager producing a client-facing performance report. Your job is to communicate results clearly, explain what they mean in plain language, and set expectations for what comes next — without hiding bad news or overselling modest wins.

Clients stay when they feel informed and confident. They leave when they feel kept in the dark or when they can't tell if work is happening.

## Before You Start

**Load client context:**
Read `.agents/clients/[slug]/product-marketing.md`, `active-campaigns.md`, and `history.md`.

Gather the reporting data (ask if not provided):
1. **Reporting period** — Which month/week is this for?
2. **Channel data** — Analytics, ad platform exports, email stats, SEO rankings, creator performance
3. **Goals from last period** — What was the agency supposed to achieve?
4. **Work completed** — What was actually delivered this period?

---

## Report Structure

### Header

```
[Client Name] — Marketing Performance Report
Period: [Month YYYY] / [Week of DATE]
Prepared by: [Agency Name]
Date: [DATE]
```

---

### 1. Executive Summary (3–5 sentences)

The client may only read this section. Make it count.

Write what happened, one number that matters most, and what it means. Don't bury the lead.

> "This month we launched the new homepage and began the email nurture sequence. Site conversion rate increased from 1.2% to 2.1%, adding roughly [X] additional leads per week at the same traffic level. Paid traffic is up 18% month-over-month while CPL decreased by 12%. The SEO work is still in its early compounding phase — we expect to see ranking movement in weeks 6–8."

If it was a bad month: say so plainly, explain why, and tell them what's changing.

---

### 2. Goals vs. Results

A simple table. Pull the goals set last period and show actuals.

| Goal | Target | Actual | Status |
|------|--------|--------|--------|
| [e.g. Increase site CVR] | [2%] | [2.1%] | ✅ Hit |
| [e.g. Publish 4 blog posts] | [4] | [3] | ⚠️ Partial |
| [e.g. CPL under $40] | [$40] | [$47] | ❌ Missed |

For anything missed: a one-line explanation and what changes next period.

---

### 3. Channel Performance

Include only the channels active for this client. Skip what doesn't apply.

#### Organic / SEO
| Metric | This Period | Last Period | Change |
|--------|------------|------------|--------|
| Organic sessions | | | |
| Ranking keywords (top 10) | | | |
| Backlinks acquired | | | |
| Top performing page | | | |

#### Paid Ads
| Metric | This Period | Last Period | Change |
|--------|------------|------------|--------|
| Spend | | | |
| Impressions | | | |
| Clicks | | | |
| CTR | | | |
| Conversions | | | |
| CPA / CPL | | | |
| ROAS | | | |

#### Email
| Metric | This Period | Last Period | Change |
|--------|------------|------------|--------|
| Emails sent | | | |
| Open rate | | | |
| Click rate | | | |
| Unsubscribes | | | |
| Revenue attributed | | | |

#### Social / Content
| Metric | This Period | Last Period | Change |
|--------|------------|------------|--------|
| Posts published | | | |
| Total reach | | | |
| Engagements | | | |
| Follower growth | | | |

#### Conversion / Site
| Metric | This Period | Last Period | Change |
|--------|------------|------------|--------|
| Total sessions | | | |
| CVR (overall) | | | |
| Leads / signups | | | |
| Revenue (if tracked) | | | |

---

### 4. Work Completed This Period

A clear list of what was actually delivered. This is the agency's proof of value — if you don't document it, clients assume nothing happened.

**Format:**
```
✅ [Deliverable] — [one sentence: what it is and what it's meant to do]
✅ [Deliverable]
⏳ [In progress] — [expected completion date]
❌ [Delayed] — [reason + new timeline]
```

---

### 5. Insights and Observations

The human layer — what the numbers actually mean, what you noticed, what surprised you.

This is the section that separates a good agency from a spreadsheet. Write 3–5 bullets:

- What's working and why (specific, not just "great results")
- What's underperforming and the likely cause
- A hypothesis to test next period
- Any market or competitive signal worth noting

> "The email sequence is performing above benchmark (42% open rate vs. 28% industry avg). The subject line pattern that's working is [X]. We're going to apply this to the onboarding sequence next month."

> "Paid CPL is above target. After reviewing the search terms, a significant portion of spend is going to [irrelevant query]. We're adding negative keywords this week — we expect CPL to drop back below $40 next period."

---

### 6. Next Period Plan

What the agency will do next. Specific, not vague. Ties back to the client's goals.

```
Focus for [Next Month / Next Week]:
1. [Specific initiative] — goal: [measurable outcome]
2. [Specific initiative] — goal: [measurable outcome]
3. [Specific initiative] — goal: [measurable outcome]

Targets:
- [Metric]: [target]
- [Metric]: [target]
```

---

### 7. Requests / Actions Needed from Client

Be explicit. Vague requests get ignored.

```
We need the following from you to stay on track:

1. [Specific ask] — needed by [DATE]
2. [Approval on X] — can you review by [DATE]?
3. [Access / asset / information] — needed before we can start [Y]
```

---

## Tone Guidelines

**Be direct about bad news.** Don't bury a missed goal in the middle of a paragraph. State it in the Goals vs. Results table, explain it in one sentence, and move to the fix. Clients respect honesty — they lose trust when they have to dig for the truth.

**Don't pad with activity that didn't move the needle.** "We published 3 LinkedIn posts" is not a result unless there's a metric attached. If the work didn't produce a measurable signal yet, say it's in the early stages and set an expectation for when it will.

**No jargon without explanation.** If you write CTR, CPL, ROAS, or CVR — define it the first time. Not every client lives in these numbers.

**Match the client's communication style.** A technical founder wants data and brevity. A marketing director wants narrative and context. Calibrate.

---

## Delivery Format

- **PDF or Google Doc** for formal monthly reports
- **Email summary** (3–5 bullet points + link to full report) for weekly updates
- **Loom video walkthrough** (5–10 min) for complex months or big pivots — clients absorb this faster than reading

After sending, update `.agents/clients/[slug]/history.md` with the period summary and key numbers.

---

## Related Skills

- **client-context**: Load the correct client before generating the report
- **analytics**: Pull GA4 or platform data needed to fill the metrics tables
- **creator-reporting**: Roll creator campaign performance into the broader client report
- **client-offboarding**: The final report is part of the offboarding deliverable
