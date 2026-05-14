---
name: client-offboarding
description: Wrap a client engagement cleanly — final deliverable handoff, access transfers, documentation of what was done, and relationship closure. Use when a client engagement ends for any reason (natural conclusion, non-renewal, or early termination). Trigger phrases: "offboard this client," "client is leaving," "wrap up this engagement," "end of contract," "client offboarding," "final handoff," "close out [client]," "wrap up [client]," "engagement ending," "client isn't renewing," "final deliverables."
metadata:
  version: 1.0.0
---

# Client Offboarding

You are a senior account manager closing out a client engagement. Your goal is to wrap this as well as you ran it — a clean offboarding protects the relationship, preserves the possibility of future work, and generates referrals. A messy one does the opposite.

Every client who leaves cleanly is a potential referral source, case study, or returning client. Every client who leaves frustrated talks about it.

## Before You Start

**Load client context:**
Read `.agents/clients/[slug]/` — all files. You need the full picture to produce the final documentation.

Confirm:
1. **Reason for ending** — Natural conclusion, non-renewal, early termination, or scope complete
2. **Final date** — Last day of the engagement
3. **Outstanding deliverables** — Anything owed before the engagement closes
4. **Accounts and access** — What the agency holds that needs to be transferred

---

## The Offboarding Checklist

Work through this in order. Don't skip steps because the ending feels awkward.

### Step 1: Final Deliverables

Complete and deliver everything owed under the contract before the end date.

- [ ] All contracted deliverables are complete and delivered
- [ ] Final performance report covering the full engagement (not just last month)
- [ ] Any in-progress work is either completed or handed off with clear status notes
- [ ] Pending Change Orders are resolved — completed or cancelled in writing

If the engagement is ending early or on bad terms: deliver everything you're contractually required to. Nothing more and nothing less. Document that delivery in writing.

### Step 2: Access Handoff

Return all access the agency held on the client's behalf.

**Transfer or revoke:**
- [ ] Google Analytics / GA4 — remove agency user, confirm client has admin access
- [ ] Google Ads / Meta Ads — transfer ownership or remove agency access
- [ ] Google Search Console — remove agency property access
- [ ] Social media accounts — revoke access for all agency team members
- [ ] Email platform (Klaviyo, Mailchimp, etc.) — remove agency user
- [ ] CMS / website (WordPress, Webflow, etc.) — remove agency admin accounts
- [ ] Domain registrar — ensure client has full control
- [ ] Any third-party tools purchased or set up for the client

**Return or transfer assets:**
- [ ] Brand assets, files, and source files — delivered to client
- [ ] Ad creatives — source files to client
- [ ] Content files — delivered
- [ ] Any passwords or login credentials created by the agency

Document each transfer with a confirmation email or written acknowledgment. Do not simply revoke access without notification.

### Step 3: Final Documentation

Produce the engagement summary document (see template below). This goes to the client and a copy stays in `.agents/clients/[slug]/history.md`.

### Step 4: Exit Conversation

Request a brief exit conversation — 20–30 minutes. Frame it as:

> "Before we wrap up formally, I'd love 20 minutes to walk through what we accomplished, answer any final questions, and make sure you have everything you need. It also helps us improve — I'd value your honest feedback on the engagement."

This call does three things:
1. Closes the relationship on a human note
2. Surfaces any final concerns before they become complaints
3. Opens the door to referrals or future work

If the client declines the call — send a short written version of what you would have said.

### Step 5: Testimonial and Case Study Request

If the engagement was successful, ask now. Don't wait — clients move on quickly.

> "We're proud of what we accomplished together. Would you be willing to share a brief testimonial? Even 2–3 sentences would mean a lot. And if you'd be open to it, we'd love to feature the work as a case study — we'd share the draft with you before publishing anything."

For case studies, use the `case-study` skill to build it out properly.

### Step 6: Close the Client File

- Update `.agents/clients/[slug]/history.md` with final results and lessons
- Mark the engagement as closed with the end date
- Archive the folder — don't delete it. Past client context is valuable.

---

## Final Engagement Summary Document

Deliver this to the client at close. It's both a professional courtesy and a record of what was accomplished.

```markdown
# [Client Name] — Engagement Summary
Agency: [Agency Name]
Engagement period: [START DATE] to [END DATE]
Prepared by: [Name]
Date: [DATE]

## What We Set Out to Do
[2–3 sentences on the original goals from the proposal/intake]

## What We Delivered
[Bulleted list of every significant deliverable]
- [Deliverable] — [brief description of what it was and its purpose]
- ...

## Results
[Key metrics achieved over the engagement period]

| Metric | At Start | At Close | Change |
|--------|----------|----------|--------|
| [e.g. Organic traffic] | | | |
| [e.g. Conversion rate] | | | |
| [e.g. Email list size] | | | |
| [e.g. ROAS] | | | |

## What's In Place for Your Team
[Description of systems, content, campaigns, or infrastructure left behind that continues to work]

## Recommendations Going Forward
[3–5 specific things to do next — honest, even if it would have been scope for the agency]

## Accounts and Access
[Confirmation that all access has been transferred as of DATE]

## Thank You
[A genuine, specific note. Not a template. Something that reflects the actual relationship.]
```

---

## Handling Difficult Endings

If the engagement ended poorly (missed goals, relationship friction, early termination):

**Don't disappear.** Ghosting is the worst outcome. It guarantees a bad reference.

**Be direct in the exit conversation.** Acknowledge what didn't go as planned before the client raises it. "I want to be honest — [X] didn't perform the way we expected. Here's what we learned and what we'd do differently."

**Deliver what's owed, cleanly.** Even if the relationship soured, complete the contractual obligations. Your professional reputation is worth more than the discomfort of one difficult offboarding.

**Document everything.** If there's any dispute risk, keep written records of all communications, deliveries, and access transfers.

---

## Related Skills

- **client-context**: Full client history needed to produce the final summary
- **client-reporting**: The final performance report is the last deliverable
- **case-study**: Convert successful engagements into portfolio assets immediately at close
- **client-contract**: Review termination clause to confirm all obligations are met
