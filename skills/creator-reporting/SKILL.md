---
name: creator-reporting
description: Set up tracking for creator campaigns and produce end-of-campaign reports showing ROI, reach, engagement, and conversion performance per creator. Use during campaign setup (UTM links, promo codes) and at campaign end to summarize results. Trigger phrases: "track influencer campaign," "creator campaign report," "influencer ROI," "did this creator perform," "measure influencer results," "UTM for creator," "promo code tracking," "creator campaign analytics," "influencer reporting," "campaign wrap report," "which creators drove results," "attribution for influencer." Covers TikTok, Instagram, and YouTube.
metadata:
  version: 1.0.0
---

# Creator Reporting

You are an expert at setting up creator campaign tracking and producing clear reports that show what worked, what didn't, and what to do next.

Most influencer campaigns are badly measured — brands track vanity metrics (likes, impressions) and declare success or failure without any real signal. Good reporting ties creator activity to business outcomes and gives you data to make smarter decisions on the next campaign.

## Before You Start

**Check for product marketing context first:**
If `.agents/product-marketing.md` exists (or `.claude/product-marketing.md`), read it before asking questions.

Gather this context (ask if not provided):

1. **Campaign goal** — Awareness, traffic, conversions, app installs, email signups, UGC collection
2. **Creator list** — Who ran content, which platforms, when it went live
3. **Tracking setup** — Are UTM links and/or promo codes in place? (Set these up at campaign start)
4. **Time window** — Reporting period (e.g. 30 days post-go-live)
5. **Access to analytics** — GA4, Shopify, platform dashboards, etc.

---

## Phase 1: Pre-Campaign Tracking Setup

Set this up before any content goes live. You cannot retroactively attribute conversions.

### UTM Links

Create a unique UTM link for each creator. This lets you see exactly how much traffic and how many conversions each creator drove in GA4 or any analytics platform.

**UTM structure:**
```
https://yourdomain.com/[landing-page]
  ?utm_source=[platform]
  &utm_medium=influencer
  &utm_campaign=[campaign-name]
  &utm_content=[creator-handle]
```

**Example:**
```
https://brand.com/shop
  ?utm_source=tiktok
  &utm_medium=influencer
  &utm_campaign=summer-launch
  &utm_content=sarahfit
```

Use a URL shortener (Bit.ly, Dub.co) to make the link clean for bio/link stickers/descriptions. Each creator gets their own shortened URL that resolves to their unique UTM.

### Promo Codes

Give each creator a unique promo code. This is the most reliable conversion signal — especially when UTM links aren't available (TikTok bio links are restricted to 1k+ accounts, Instagram allows one link in bio).

**Format:** `[CREATORNAME]10` or `[INITIALS][DISCOUNT]` — memorable and creator-specific
**Discount:** 10–15% is standard for audience incentive; consider whether it matches the brand's margin

Track promo code usage in:
- Shopify: Analytics → Discount codes
- WooCommerce: Reports → Coupons
- Any ecommerce platform with discount code analytics

### TikTok-Specific Tracking

TikTok's native analytics (available to creator after 1k followers) show:
- Video views, likes, comments, shares, saves
- Reach and profile visits
- Audience demographics per video

For conversion tracking, TikTok Pixel integration captures website events attributed to TikTok ads. For organic creator content, promo codes are the primary conversion signal.

### Instagram-Specific Tracking

- Creators with a Professional account can share their Instagram Insights
- Stories: reach, link taps (if using link sticker), replies, exits
- Reels: reach, plays, shares, saves
- Feed: reach, impressions, profile visits, link clicks

Ask creators to screenshot and share their insights within 7 days of posting (Stories expire from analytics).

### YouTube-Specific Tracking

- YouTube Studio shows views, watch time, click-through rate (thumbnail/card), and traffic sources
- Ask creator to share a screenshot of the video's analytics at 7 days and 30 days post-upload
- The unique UTM link in the description is the primary conversion signal

---

## Phase 2: During the Campaign

Monitor these signals in the first 48–72 hours after each piece of content goes live:

- Is the content performing well? (Views, engagement in first 24 hours)
- Are there any negative comments or brand safety issues to address?
- Is the promo code being used? (Even early redemptions signal intent)
- Is UTM traffic showing up in analytics?

If content underperforms significantly, note it — but don't ask the creator to re-post or edit without contractual grounds. Use this to inform future creator selection.

---

## Phase 3: End-of-Campaign Reporting

### Data to collect from each creator

Request this data 7 days and 30 days after go-live:

**TikTok:**
- Views, likes, comments, shares, saves
- Profile visits from the video
- Follower change during campaign window

**Instagram:**
- Reels: reach, plays, shares, saves
- Stories: reach, link taps (if applicable), exits at each slide
- Feed: reach, impressions, profile visits

**YouTube:**
- Views, watch time (total and average %), likes, comments
- Click-through rate on cards/end screens with brand link
- Traffic source breakdown (search vs. suggested vs. external)

**Brand-side data:**
- UTM link sessions and conversions from GA4 (or analytics platform)
- Promo code redemptions per creator (from ecommerce platform)
- Revenue attributed to each creator's promo code

---

## Performance Benchmarks by Platform

Use these to contextualize results. Context-free numbers are meaningless — "10,000 views" is either great or terrible depending on the creator's tier and the platform.

### TikTok
| Creator Tier | Average Views/Post | Good Views | Engagement Rate |
|-------------|-------------------|-----------|-----------------|
| Nano (1k–10k) | 500–3k | 5k+ | >8% |
| Micro (10k–100k) | 3k–30k | 50k+ | >5% |
| Mid (100k–500k) | 30k–150k | 300k+ | >3% |
| Macro (500k+) | 150k+ | 1M+ | >2% |

TikTok CPM (cost per 1,000 views) benchmark for organic creator content: $5–$30 depending on niche and engagement quality.

### Instagram
| Creator Tier | Average Reel Reach | Average Story Views | Engagement Rate |
|-------------|-------------------|---------------------|-----------------|
| Nano | 500–2k | 200–800 | >5% |
| Micro | 2k–20k | 800–5k | >3% |
| Mid | 20k–100k | 5k–25k | >2% |
| Macro | 100k+ | 25k+ | >1% |

### YouTube
| Creator Tier | Average Views/Video | CTR on Cards | Watch Time Target |
|-------------|--------------------|--------------|--------------------|
| Small (1k–50k) | 1k–10k | >1% | >50% of video length |
| Mid (50k–500k) | 10k–100k | >1.5% | >40% |
| Large (500k+) | 100k+ | >2% | >35% |

---

## Calculating ROI

### For direct response campaigns (sales goal)

```
Revenue = sum of all orders using creator's promo code + UTM-attributed conversions

Cost = creator fee + product cost (if gifted) + any platform fee

ROI = (Revenue - Cost) / Cost × 100

ROAS = Revenue / Cost
```

A ROAS of 2x (every $1 spent returns $2) is break-even for most DTC brands at 50% margins. Target 3–5x for a healthy campaign.

### For awareness campaigns (no direct conversion goal)

Calculate **Cost Per Thousand Impressions (CPM)** and **Cost Per Engagement (CPE)**:

```
CPM = (Creator fee / Total reach) × 1,000
CPE = Creator fee / Total engagements (likes + comments + shares + saves)
```

Compare against paid social benchmarks:
- TikTok paid CPM: $10–$20 → organic creator CPM should beat this
- Instagram paid CPM: $5–$15 → organic creator CPM should beat this

### For traffic campaigns

```
Cost Per Click (CPC) = Creator fee / UTM link sessions

Compare to Google/Meta paid CPC in the same niche
```

---

## Campaign Wrap Report Template

Produce a clean summary for client or internal review:

---

**[Campaign Name] — Creator Campaign Report**
**Period:** [Start date] to [End date]
**Prepared by:** [Name]

**Campaign Goal:** [Awareness / Conversions / Traffic / UGC]
**Total Budget:** $[X]
**Creators Activated:** [N] across [platforms]

---

**Overall Results**

| Metric | Result | Benchmark | vs. Benchmark |
|--------|--------|-----------|--------------|
| Total Reach | [X] | — | — |
| Total Engagements | [X] | — | — |
| Avg. Engagement Rate | [X%] | [platform avg] | [+/-X%] |
| Promo Code Redemptions | [X] | — | — |
| Revenue Attributed | $[X] | — | — |
| ROAS | [X]x | 3x target | [+/-] |

---

**Per-Creator Breakdown**

| Creator | Platform | Followers | Views/Reach | Eng. Rate | Code Uses | Revenue | Cost | ROAS |
|---------|----------|-----------|-------------|-----------|-----------|---------|------|------|
| @handle | TikTok | 45k | 120k | 4.2% | 38 | $1,140 | $400 | 2.9x |
| ... | | | | | | | | |

---

**Top Performer:** @[handle] — [why: highest engagement / best conversion / most authentic fit]

**Underperformer:** @[handle] — [why: low engagement rate / no conversions / content felt off-brief]

**Key Learnings:**
1. [What worked — content style, creator type, platform, offer]
2. [What didn't work — be specific]
3. [What to test next campaign]

**Recommendation:**
- Renew: @[handles who performed]
- Cut: @[handles who didn't]
- New criteria to prioritize: [based on what worked]

---

## Related Skills

- **creator-discovery**: Build and track the initial creator list
- **creator-vetting**: Correlate vetting scores with actual performance to improve future selection
- **creator-brief**: Include UTM links and promo codes in the brief so they're set up before go-live
- **creator-contract**: Deliverables stated in the contract should match what you're tracking here
