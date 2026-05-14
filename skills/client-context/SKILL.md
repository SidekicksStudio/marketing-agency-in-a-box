---
name: client-context
description: Load, switch, and manage context for a specific client. This is the foundational skill for multi-client agency operation — always run this first before any other skill when working on a client project. Trigger phrases: "load [client name]," "switch to [client]," "we're working on [client] now," "set up a new client," "create a client file," "which client are we on," "client context," "show me the clients," "list clients," "I need to work on [client name]." Every other skill depends on this one being loaded.
metadata:
  version: 1.0.0
---

# Client Context

You are the context manager for a multi-client marketing agency. Before any other work begins, the right client must be loaded. Every skill in this repo assumes a single product context — this skill makes that work across multiple clients by routing to the correct one.

## The Problem This Solves

Every execution skill (copywriting, SEO, ads, creator campaigns, etc.) reads from a product context file before doing anything. In a single-product setup that file lives at `.agents/product-marketing.md`. In an agency with 10 clients, running without this skill means the agent either uses the wrong client's context or asks repetitive questions it should already know.

This skill creates and manages per-client context files and tells the agent which client is currently active.

---

## Client File Structure

All client files live under `.agents/clients/`:

```
.agents/
  clients/
    [client-slug]/
      product-marketing.md     # Core context — read by all execution skills
      brand-guidelines.md      # Voice, tone, visual rules, do/don't language
      active-campaigns.md      # What's currently running, goals, budgets
      contacts.md              # Key stakeholders, decision makers, communication prefs
      history.md               # What's been done, results, decisions made
  product-marketing.md         # Legacy single-client path (still supported)
```

`[client-slug]` is lowercase, hyphenated. Examples: `nike`, `acme-co`, `johns-bakery`, `project-atlas`.

---

## Loading a Client

When the user says "load [client]" or "we're working on [client] now":

1. Check if `.agents/clients/[client-slug]/` exists
2. If yes — read `product-marketing.md` and `active-campaigns.md` from that directory. Confirm: "Loaded [Client Name]. Here's what I know: [brief summary of product, current campaigns, last activity]."
3. If no — offer to create a new client file (see below)

Once a client is loaded, treat their `product-marketing.md` as the active context for all subsequent skills. Do not switch clients mid-conversation unless explicitly told to.

---

## Creating a New Client

When the user says "set up a new client" or "create a client file for [name]":

Ask the following — or pre-fill from anything already provided:

```
Client name: 
Slug (for folder name, lowercase-hyphenated): 
Industry: 
Product/service (one sentence): 
Target audience: 
Primary goal for this engagement: 
Key contacts (name, role, email): 
Monthly retainer or project basis: 
Start date: 
```

Then create the directory and seed these files:

**`.agents/clients/[slug]/product-marketing.md`** — filled with what you know, flagged TODOs for missing info

**`.agents/clients/[slug]/active-campaigns.md`** — blank template:
```markdown
# Active Campaigns — [Client Name]
Last updated: [DATE]

## Currently Running
[None yet]

## Upcoming
[None yet]

## On Hold
[None yet]
```

**`.agents/clients/[slug]/contacts.md`** — blank template:
```markdown
# Contacts — [Client Name]

## Primary Contact
Name: 
Role: 
Email: 
Preferred communication: 
Response time expectation: 

## Decision Maker (if different)
Name: 
Role: 

## Notes
```

**`.agents/clients/[slug]/history.md`** — blank template:
```markdown
# Engagement History — [Client Name]
Started: [DATE]

## Decisions Made
[Log important decisions here with dates]

## Work Completed
[Log deliverables with dates]

## Results
[Log performance data as it comes in]
```

Confirm creation and offer to run `client-intake` to fill out the context properly.

---

## Listing All Clients

When the user says "list clients" or "show me the clients":

Read the contents of `.agents/clients/` and list each folder with:
- Client name (from their `product-marketing.md` header)
- Active campaigns count (from `active-campaigns.md`)
- Last modified date of any file in their folder

---

## Updating Client Context

When work is completed, significant decisions are made, or results come in — update the relevant client file immediately. Don't let the history go stale.

**After any deliverable:** Add an entry to `history.md`
**After a campaign launches:** Update `active-campaigns.md`
**After a client call:** Update `contacts.md` with anything new learned
**After results come in:** Log in both `history.md` and `active-campaigns.md`

---

## How Other Skills Use This

Every execution skill checks for product context in this order:
1. `.agents/clients/[active-client]/product-marketing.md` ← agency multi-client path
2. `.agents/product-marketing.md` ← legacy single-client path
3. `.claude/product-marketing.md` ← older fallback

When client-context is loaded correctly, skills pick up context automatically — no re-explaining the client on every task.

---

## Confidentiality Note

Each client's files contain proprietary business information. When working in a shared environment or handing off between agents, confirm that client files are not being exposed to the wrong session or user.

---

## Related Skills

- **client-intake**: Populate a new client's context files properly after creating the folder structure
- **agency-positioning**: Understand what the agency offers before scoping client work
- **client-reporting**: Pull from active-campaigns.md and history.md when building reports
