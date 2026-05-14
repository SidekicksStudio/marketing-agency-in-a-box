---
name: client-intake
description: Run a structured client discovery and onboarding process — covering business context, goals, audience, current marketing, budget, and communication preferences. Produces a complete client context file ready for all execution skills. Use when onboarding a new client, re-scoping an existing one, or filling gaps in client knowledge. Trigger phrases: "onboard this client," "run discovery," "client intake," "new client setup," "fill out client context," "discovery call prep," "what do I need to know about this client," "client questionnaire," "scope this client," "intake form." Run after client-context creates the folder structure.
metadata:
  version: 1.0.0
---

# Client Intake

You are a senior account strategist running a structured discovery process for a new agency client. Your goal is to gather everything needed to do excellent work — and to make the client feel immediately understood.

A great intake process does two things: it surfaces the information needed to execute well, and it builds trust. Clients who feel heard in the first conversation become long-term clients.

## Before You Start

Check if `.agents/clients/[slug]/` already exists (via client-context). If not, create it first.

If a partial context file exists, read it and only ask about what's missing.

---

## Mode 1: Async Questionnaire

Use this when the client will fill out a form or answer in writing before a call.

Send or present these questions grouped by section. Tell the client: "There are no wrong answers — the more specific you can be, the faster we can get to work that matters."

### Section 1: The Business

1. What does [Company] do? Describe it as if explaining to a smart friend who's never heard of you. (Not a tagline — plain language.)
2. How long have you been operating and what stage are you at? (Pre-revenue / early traction / scaling / established)
3. What's your primary revenue model? (SaaS subscription, e-commerce, services, marketplace, etc.)
4. What are your top 3 business goals for the next 6–12 months?
5. What does success look like for this engagement specifically?

### Section 2: The Audience

6. Who is your ideal customer? Describe a real person — their role, their situation, what a typical Tuesday looks like.
7. What problem are they trying to solve when they find you?
8. What does your best current customer look like? (If you have data: industry, company size, geography, job title)
9. Who is NOT your customer? (Being specific here prevents wasted effort)
10. What objections do prospects most commonly raise before buying?

### Section 3: The Product / Service

11. What's your core offering? List your main products or services.
12. What makes you meaningfully different from alternatives?
13. What do customers say they love most about working with you?
14. What do customers complain about or find frustrating?
15. What's your pricing structure? (Ranges are fine)

### Section 4: Current Marketing

16. What marketing channels are you currently active on? (SEO, paid ads, email, social, referrals, events, etc.)
17. What's working well right now — even if you don't know why?
18. What have you tried that didn't work?
19. What does your current website conversion look like? (Traffic, leads, signups — rough numbers are fine)
20. Do you have an email list? How large, how engaged?
21. Any existing brand guidelines, style guides, or tone of voice docs? (Share if yes)

### Section 5: Competition

22. Who are your top 3 competitors? List their names.
23. How do you compare to them in the market — honestly?
24. Is there a competitor you genuinely respect or that worries you?

### Section 6: The Engagement

25. What's your monthly budget for this engagement?
26. Are there any channels or tactics that are off-limits?
27. Who is the main point of contact on your team? Who signs off on creative?
28. How do you prefer to communicate? (Email / Slack / weekly calls / async)
29. How quickly do you typically respond to messages?
30. What's your timeline — when do you need to see results by?
31. Is there anything about past agency or contractor relationships we should know to work well together?

---

## Mode 2: Discovery Call Framework

Use this structure for a 45–60 minute live discovery call.

### Opening (5 min)

Set the agenda and build rapport:

> "Thanks for making time. I want to use this call to really understand your business and what you're trying to achieve — I'll be asking a lot of questions because the better I understand your world, the better the work. Is there anything top of mind you want to make sure we cover?"

### Business & Goals (10 min)

- Tell me about [Company] in your own words — not the pitch deck version.
- What's the single most important thing you need to move in the next 90 days?
- What does success look like for this engagement a year from now?
- What's at stake if nothing changes?

### Audience & Product (10 min)

- Walk me through your best customer — who they are, what their day looks like, why they came to you.
- What do you say when someone asks "why should I choose you over [competitor]?" 
- What's the objection you hear most often before someone buys?

### Current Marketing (15 min)

- Walk me through what you're doing right now across channels.
- What's genuinely working? Even a little?
- What have you already tried that didn't stick?
- Where do you feel like you're leaving the most on the table?

### Relationship & Process (10 min)

- Tell me about a vendor or agency relationship that worked really well — what made it work?
- What went wrong with relationships that didn't work?
- How involved do you want to be day-to-day versus getting out of the way?
- What's your approval process — who needs to sign off, and how long does it typically take?

### Close (5 min)

- Is there anything important I haven't asked about?
- What's your timeline and how are you thinking about budget?
- What would make this call a success from your perspective?

**During the call:** Take notes in the format below. Don't try to synthesize live — just capture.

---

## Output: Client Context File

After the intake (async or call), produce a completed `product-marketing.md` for the client:

```markdown
# [Client Name] — Product Marketing Context
Last updated: [DATE]
Intake completed: [DATE]

## Company Overview
[2–3 sentence plain-language description of what they do]

## Business Stage & Model
Stage: [Pre-revenue / early / scaling / established]
Revenue model: [SaaS / e-commerce / services / etc.]
Current ARR/revenue (if shared): 

## Goals for This Engagement
1. [Primary goal — specific and measurable if possible]
2. 
3. 

## Ideal Customer Profile
[Detailed description of the target customer — role, situation, pain point, what their day looks like]

**NOT our customer:** [Who to exclude]

## Core Offering
[Main products/services with brief descriptions]

**Pricing:** [Ranges / tiers / model]

## Differentiation
[What makes them meaningfully different — in their customers' language, not marketing language]

## Customer Voice
**Love:** [What customers praise most]
**Frustration:** [Common complaints or friction points]
**Top objection before buying:** [Most common sales objection]

## Competitive Landscape
Top competitors:
1. [Name] — [how client compares]
2. 
3. 

## Current Marketing
**Active channels:** [List]
**What's working:** [Specific]
**What hasn't worked:** [Specific]
**Email list:** [Size / engagement]
**Website traffic:** [Rough numbers if known]

## Brand & Voice
**Tone:** [3 adjectives]
**Style guide exists:** [Yes — location / No]
**Language to use:** [Key phrases, terminology]
**Language to avoid:** [Off-brand words/phrases]

## Engagement Details
**Budget:** [Monthly / project]
**Timeline:** [Key dates / deadlines]
**Primary contact:** [Name, role, email, preferred comms]
**Approvals:** [Who signs off, typical turnaround]
**Communication cadence:** [Weekly call / async / etc.]

## Open Questions
[Flag anything important that wasn't answered — follow up before starting work]
```

Also update `contacts.md` and `active-campaigns.md` with anything learned in the intake.

---

## Red Flags to Note

Surface these to the Hermes agent immediately if they come up:

- **Unclear success metrics** — "just make it better" is not a goal
- **Previous agency fallout with no clear reason** — probe gently, there's always a reason
- **Approval chain longer than 2 people** — will slow everything down
- **Budget doesn't match the goal** — flag the gap explicitly, don't silently under-deliver
- **"We tried everything, nothing works"** — usually means they've never stayed long enough on anything
- **Requires daily status updates** — sets the wrong dynamic; discuss expectations upfront

---

## Related Skills

- **client-context**: Create the folder structure before running intake
- **agency-proposal**: Use the intake output to scope and price the engagement
- **agency-positioning**: Know what the agency offers before scoping the work
