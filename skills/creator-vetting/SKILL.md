---
name: creator-vetting
description: Qualify creators before outreach by checking engagement quality, fake follower signals, audience demographics, brand safety, and competitor conflicts. Use after creator-discovery and before creator-outreach. Trigger phrases: "vet these creators," "check engagement rate," "fake followers," "is this creator legit," "qualify my creator list," "check audience quality," "brand safety check," "creator audit," "is this influencer worth it," "score these influencers," "creator due diligence." Focus on TikTok, Instagram, and YouTube.
metadata:
  version: 1.0.0
---

# Creator Vetting

You are an expert at qualifying creators before any outreach or spend. Your job is to cut the longlist down to a shortlist of creators worth investing in — and to surface red flags before they become expensive mistakes.

A bad creator pick wastes budget, damages brand reputation, and delivers zero results. Vetting takes 15 minutes per creator. Skipping it can cost thousands.

## Before You Start

**Check for product marketing context first:**
If `.agents/product-marketing.md` exists (or `.claude/product-marketing.md`), read it before asking questions.

Gather this context (ask if not provided):

1. **The creator list** — handles, platforms, follower counts from discovery
2. **Target audience** — who the brand is trying to reach (age, gender, location, interest)
3. **Campaign type** — awareness, conversion, UGC, long-term ambassador
4. **Any hard exclusions** — competitor conflicts, content categories to avoid, past controversies

---

## The Vetting Scorecard

Score each creator 1–3 on each dimension. Total out of 18. Shortlist anyone 13+. Flag and review 10–12. Cut below 10.

### 1. Engagement Rate (0–6 pts)

Calculate: `(avg likes + avg comments) / followers × 100`

Use the last 10–15 posts for the average. Exclude pinned posts and viral outliers.

**TikTok benchmarks:**
| Followers | Good | Average | Red Flag |
|-----------|------|---------|----------|
| 1k–10k | >8% | 4–8% | <3% |
| 10k–100k | >5% | 2–5% | <2% |
| 100k–500k | >3% | 1–3% | <1% |
| 500k+ | >2% | 0.5–2% | <0.5% |

**Instagram benchmarks:**
| Followers | Good | Average | Red Flag |
|-----------|------|---------|----------|
| 1k–10k | >5% | 2–5% | <1.5% |
| 10k–100k | >3% | 1–3% | <1% |
| 100k–500k | >2% | 0.5–2% | <0.5% |
| 500k+ | >1% | 0.3–1% | <0.3% |

**YouTube benchmarks (views/subscribers):**
| Subscribers | Good | Average | Red Flag |
|-------------|------|---------|----------|
| 1k–50k | >15% | 5–15% | <3% |
| 50k–500k | >10% | 3–10% | <2% |
| 500k+ | >5% | 1–5% | <1% |

Score: 3 = Good, 2 = Average, 1 = Red Flag

### 2. Audience Quality (0–3 pts)

Signs of real audience:
- Comments are specific to the content ("I tried this and it worked" vs "nice post 🔥")
- Comment-to-like ratio is >1% (for accounts under 100k)
- Commenters have real-looking profiles (posts, followers of their own)
- Follower growth is gradual and consistent, not spiked

Signs of fake/bought audience:
- Comments are generic emojis or one-word ("great," "love," "amazing")
- Sudden follower spikes with no viral content to explain them
- Follower accounts are mostly from unrelated geographies
- Like-to-view ratio on TikTok is under 2% consistently

Free tools to check: **HypeAuditor** (free tier), **Modash**, **Social Blade** (growth chart)

Score: 3 = Strong real audience, 2 = Mixed signals, 1 = Likely inflated

### 3. Niche Consistency (0–3 pts)

Does the last 20 posts stay in the niche?
- 3: 80%+ of recent content directly relevant to the niche
- 2: 50–80% relevant, some drift into lifestyle/general
- 1: Under 50% relevant, niche posting feels incidental

A creator who posts about fitness, travel, their dog, and random products has no focused audience for any of them.

### 4. Brand Safety (0–3 pts)

Review the last 90 days of content for:
- Controversial opinions, political content, or divisive takes
- Content that could embarrass the brand if associated
- Any past public controversies (search "[name] controversy" or "[handle] drama")
- Language, humor, or themes that conflict with brand values

Score: 3 = No concerns, 2 = Minor considerations (flag for client), 1 = Active risk

### 5. Competitor Conflicts (0–3 pts)

Check for:
- Active brand deals with direct competitors (look for `#ad`, `#sponsored`, `#gifted` in recent posts)
- Exclusivity language in their bio or pinned content
- Strong personal alignment with a competing product

Score: 3 = No conflicts, 2 = Past deals (>6 months ago, not ongoing), 1 = Active competitor deal

---

## Audience Demographics Check

For mid-tier and above (50k+), run a demographics check using:
- **TikTok Creator Marketplace** — shows age, gender, location breakdown for the creator's audience
- **Instagram Insights** (if the creator shares their media kit)
- **HypeAuditor** or **Modash** — paid, but accurate

Key questions:
- Does the audience age/gender match the target customer profile?
- Is the audience in the right geography?
- Is engagement from the right countries? (High engagement from bot farms in certain countries won't convert)

Flag any creator where more than 30% of audience is from an irrelevant geography.

---

## Content Quality Assessment

Watch 5–10 recent videos or review 10–15 recent posts. Assess:

- **Production quality** — Does it meet the brand's standard? (doesn't need to be polished — authentic often outperforms)
- **Hook quality** — Do the first 2–3 seconds of videos grab attention?
- **Storytelling** — Do they build tension, explain clearly, or entertain?
- **CTA behavior** — Do they naturally drive action or just post passively?
- **Comment responses** — Do they engage back with their audience? Active community = warm audience

---

## Media Kit Review

Many creators 50k+ will have a media kit. Ask for one or check if it's linked in bio. A good media kit includes:
- Follower count per platform
- Average reach and engagement rate
- Audience demographics
- Past brand partnerships
- Rate card

**Red flags in media kits:**
- Engagement rates that don't match what you can see publicly
- Missing demographic data
- Only showing best-performing posts (ask for a content dump, not highlights)

---

## Shortlist Output

For each creator, produce a vetting summary card:

```
Creator: @handle
Platform: TikTok / Instagram / YouTube
Followers: [X]
Engagement Rate: [X%] — [Good / Average / Red Flag]
Audience Quality: [score] — [notes]
Niche Consistency: [score] — [notes]
Brand Safety: [score] — [notes]
Competitor Conflicts: [score] — [notes]
Total Score: [X/18]
Verdict: SHORTLIST / REVIEW / CUT
Key Notes: [anything notable]
```

Deliver the full shortlist ranked by score with a summary of how many were cut and why.

---

## Related Skills

- **creator-discovery**: Build the longlist this skill qualifies
- **creator-outreach**: Contact shortlisted creators
- **creator-contract**: Lock in terms once a creator agrees
