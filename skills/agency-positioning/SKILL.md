---
name: agency-positioning
description: Define and articulate the agency's own positioning — what it does, who it's for, what it doesn't do, and how it talks about itself. The foundation for proposals, outreach, and anything the agent says when a prospect asks "what do you do?" Trigger phrases: "what does the agency do," "how do we pitch ourselves," "agency positioning," "who is our ideal client," "agency ICP," "what should I say about Sidekicks Studio," "agency elevator pitch," "our services," "what do we offer," "agency bio," "how do we introduce ourselves," "pitch the agency."
metadata:
  version: 1.0.0
---

# Agency Positioning

You are the agency's positioning strategist. This skill defines how the agency presents itself — to prospects, in proposals, in cold outreach, and in any context where someone asks "what do you do?"

This skill is meta: it's about the agency, not the clients. Every other skill serves clients. This one serves the agency itself.

## The Agency Context File

The agency's own positioning lives at `.agents/agency.md`. This file is the equivalent of a client's `product-marketing.md` — but for the agency itself.

If `.agents/agency.md` doesn't exist, create it by running through the questions below with the user.

Read `.agents/agency.md` before writing any agency-facing content (proposals, outreach, bios, pitches).

---

## Building the Agency Positioning

Work through each section. Answer these questions in the user's voice — not generic agency-speak.

### 1. What We Do

One sentence. Not a list of services. The problem you solve.

**Weak:** "We're a full-service digital marketing agency offering SEO, paid media, content, and social."

**Strong:** "We help early-stage SaaS companies build the marketing foundation — positioning, website, and acquisition channels — so they can grow without burning budget on things that don't compound."

The one-sentence test: could you say this at a party without sounding like a brochure? If not, simplify.

---

### 2. Who We're For (ICP)

Be specific. Narrow is better than broad. "We work with any business that needs marketing" is how agencies compete on price.

Define the ideal client by:

- **Company type:** SaaS / e-commerce / service business / consumer app / B2B / B2C
- **Stage:** Pre-seed / seed / Series A / bootstrapped / growth-stage / established
- **Size:** Revenue range, employee count, or team size
- **Situation:** What has to be true for them to need you? ("Just raised" / "product-market fit but no marketing infrastructure" / "tried doing it in-house and it didn't work")
- **Geography:** Where are they based?

Example:
> "Our sweet spot is B2B SaaS companies between $1M–$10M ARR that have product-market fit but haven't built a repeatable acquisition engine. They usually have 1–2 people doing marketing who are too stretched to do it properly. They've tried paid ads, maybe hired a freelancer, but nothing has compounded."

---

### 3. What We Don't Do

Being explicit about this saves everyone time and builds trust.

List 3–5 things the agency genuinely turns down or isn't good at:

- "We don't do brand identity or logo design"
- "We don't manage ad budgets under $5k/month — the math doesn't work"
- "We don't take on e-commerce brands — our expertise is B2B SaaS"
- "We don't do PR or earned media"

This also helps the agent qualify inbound — don't waste time pitching clients who aren't a fit.

---

### 4. What Makes Us Different

Not "we're results-driven" or "we treat you like a partner." Every agency says that.

This should be one of:

- A specific methodology or process that others don't have
- A specific type of client or stage you're unusually good at
- A structural advantage (you use AI agents, you're ex-[company], you have a specific tool or system)
- A philosophical stance that attracts the right clients and repels the wrong ones

Example:
> "We're built differently — we use AI agents to run execution at a fraction of the cost of a traditional agency team. That means a client paying $5k/month gets work that would cost $20k at a traditional shop. We're not for everyone, but for the right client it's an unfair advantage."

---

### 5. Services

List the services the agency actually delivers. Be honest about what's core vs. what's available.

Format:
```
Core services (every engagement):
- [Service] — [one sentence on what it includes and what it does]
- [Service]

Available services (by request / scope):
- [Service]
- [Service]

We don't offer:
- [Explicit exclusions]
```

---

### 6. Proof

What results have been achieved for clients? This feeds into proposals and outreach.

Capture:
- 3–5 specific results (with or without client names depending on permission)
- The type of client each result was for
- The timeframe

Example:
```
- 3x organic traffic in 6 months for a Series A HR tech SaaS
- Reduced CPL from $180 to $62 over 90 days for a B2B fintech
- Built and launched an email acquisition funnel that generates 400+ leads/month on autopilot
```

---

### 7. Pricing Model

How the agency charges. This should be clear enough that the agent can answer "how much do you charge?" without hedging.

Options:
- Monthly retainer from $[X] to $[X] depending on scope
- Project-based from $[X]
- Starter / Growth / Full-service tiers at $[X] / $[X] / $[X]

Also note: minimum engagement term, what's included in the base, what costs extra.

---

### 8. The Pitch (by context)

Pre-built versions of how the agency introduces itself in different situations.

**30-second elevator pitch:**
> "[Agency name] helps [ICP] [achieve outcome]. We do that by [brief methodology]. Most of our clients come to us when [triggering situation], and within [timeframe] we typically [specific result]."

**Cold outreach intro (1–2 sentences):**
> "[Agency name] works with [ICP] to [outcome]. We recently helped [anonymous client type] [specific result] in [timeframe]."

**Proposal intro:**
> "[Agency name] is a [descriptor] marketing agency specialising in [ICP]. We've [proof point]. We work with [X–Y] clients at a time, which means [implication for this client — attention, accountability, etc.]."

**When asked "what makes you different?":**
> "[Specific differentiator stated plainly and confidently.]"

---

## Agency Context File Template

Create `.agents/agency.md` with this structure:

```markdown
# Agency — Sidekicks Studio
Last updated: [DATE]

## What We Do
[One sentence]

## Ideal Client
[Detailed ICP]

## What We Don't Do
- 
- 
- 

## Differentiator
[Specific, honest, not generic]

## Services
Core:
- 

Available:
- 

## Proof Points
- 
- 
- 

## Pricing
[Model and ranges]

## Pitches
30-sec: 
Cold outreach: 
Proposal intro: 
What makes you different: 
```

---

## Related Skills

- **client-intake**: Know what the agency offers before scoping a client engagement
- **agency-proposal**: Agency positioning is the "Why us" section of every proposal
- **case-study**: Proof points here are built from case studies
- **cold-email**: The agency's cold outreach uses the positioning language defined here
