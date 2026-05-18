---
name: ppc-media-planning
description: Generate structured performance marketing media plans for paid campaigns across META, LinkedIn, and Google Ads. Use when building a media plan for a client, when the user mentions PPC, media buying, paid social, Google Ads campaign, LinkedIn Ads, Meta Ads, media budget allocation, agency fee structure, or campaign architecture. Also use when asked to estimate CPL/CPA benchmarks or plan multi-channel paid campaigns.
---

# PPC Media Planning — Multi-Channel Campaign Framework

This skill equips you to generate consistent, data-grounded media plans for paid campaigns across LinkedIn, Google Ads, and Meta (Facebook/Instagram). The Xerovan media plan (generated in-session) serves as the canonical reference pattern.

## Quick Reference: When to Load Additional Files

- **Client details / RFP**: Check the workspace `Client detail/` directory for client PDFs, intros, and assets.
- **Logos**: Available in `Logos/` directory — use in final deliverable formatting if producing a deck or document.
- **Local PPC context**: For geographically targeted local business campaigns, load `local-ppc-ads` skill in addition to this one.
- **LSA / map pack ads**: Load `lsa-ads` or `local-search-ads` for those specific ad types — this skill covers standard search/social/display.

---

## 1. Media Plan Document Structure

Every media plan follows this exact section sequence:

1. **Client & Market Context** — Industry, value proposition, competitive positioning summary
2. **Target Audience Segmentation** — Segments mapped to LTV and channel fit
3. **Channel Strategy & Rationale** — Why each platform, what role it plays in the funnel
4. **Budget Allocation** — Media spend split with agency/creative fees
5. **Campaign Architecture** — Platform-by-platform campaign/ad set breakdown with targeting, formats, bid strategies
6. **Creative Strategy & Messaging Matrix** — Messaging by audience, ad format assignments, CTA hierarchy
7. **Timeline & Flight Plan** — Week-by-week phase breakdown
8. **KPIs & Measurement Framework** — Benchmarks per platform, conversion tracking setup, success criteria
9. **Agency / Service Provider Fee Structure** — Fee model, what's included, what's out of scope
10. **Total Budget Summary** — Clean summary table
11. **Risks, Assumptions & Pre-Launch Checklist** — 10-step go-live checklist
12. **Scale Path (Month 2+)** — Green/yellow/red scenarios with budget and channel recommendations

---

## 2. Channel Roles & Platform Selection

### 2.1 Default Channel Mapping

| Channel | Primary Role | Best For | Typical Budget Share |
|---------|-------------|----------|---------------------|
| **LinkedIn** | B2B Lead Gen (TOF→MOF) | High-LTV B2B segments, job title / industry targeting | 35–45% of media spend |
| **Google Ads** | Intent Capture (BOF) | Search intent across all audiences; remarketing | 25–35% of media spend |
| **Meta** | Awareness + Community (TOF) | Broad reach, visual storytelling, interest-based targeting | 20–30% of media spend |

### 2.2 When to Add or Replace Channels

| Scenario | Action |
|----------|--------|
| B2C product, visual-heavy | Increase Meta share to 40%+; add TikTok if audience < 35 |
| Enterprise B2B only | LinkedIn 50%+; consider dropping Meta; add Google Display for ABM |
| Local / geo-targeted business | Load `local-ppc-ads`; replace LinkedIn with Google Maps/LSA |
| E-commerce / DTC | Meta 40%, Google Shopping 35%, TikTok 25% |
| Early-stage startup, awareness-first | Flip Meta to 50%, LinkedIn 25%, Google 25% |

### 2.3 Budget Sufficiency Check

| Total Media Budget | Viable Channels | Notes |
|--------------------|-----------------|-------|
| < $2,000/month | 1 channel only | Spreading too thin kills learning; pick the highest-intent channel |
| $2,000–$5,000 | 2 channels | LinkedIn + Google OR Google + Meta |
| $5,000–$15,000 | 3 channels | Full three-channel playbook viable |
| $15,000+ | 3+ channels | Add TikTok, YouTube, programmatic |

---

## 3. Agency Fee Structure Standards

### 3.1 Fee Models for Campaigns Under $10K/Month Media Spend

| Fee Model | Typical Range | When to Use |
|-----------|--------------|-------------|
| **Percentage of Ad Spend** | 20–30% of media spend | When ad spend fluctuates; incentive-aligned |
| **Flat Monthly Retainer** | $1,000–$3,000/month | Stable scope; includes strategy + execution |
| **Hybrid** | $500–$1,000 retainer + 10–15% of spend | Balances baseline costs with performance incentive |
| **Performance-Based** | Base fee + % of leads/revenue | Mature campaigns with reliable attribution only |

### 3.2 Recommended Default (for Sub-$5K Media Spend)

**Percentage of Ad Spend at 25%** — the industry floor for small accounts. Below this rate, agencies typically won't take the business without a minimum retainer clause.

### 3.3 Creative Support (Separate Line Item)

Creative production is typically billed separately from media management:

| Creative Scope | Monthly Range |
|----------------|---------------|
| Basic (2–3 statics, ad copy) | $300–$500 |
| Standard (5 statics, 1 carousel, copy) | $500–$800 |
| Full (2 videos + 5 statics + carousel + copy refresh) | $800–$1,500 |

Always ask whether the client has in-house creative or needs creative support from the agency. If creative is in-house, note: "Client provides creative assets; agency provides creative briefs and copywriting."

### 3.4 What Management Fee Covers vs. Excludes

**Included (standard):**
- Campaign strategy & architecture design
- Audience research & targeting setup
- Ad creative brief & copywriting
- Campaign build-out across platforms
- Conversion tracking & pixel implementation
- Landing page optimization recommendations
- Weekly bid/budget optimization
- Search term mining & negative keyword management
- A/B creative testing (2 variants per ad set)
- Weekly performance reporting
- Biweekly client sync (30 min)
- End-of-campaign report with scale recommendation

**Excluded (additional scope):**
- Creative production (video, design) — separate creative retainer or client-provided
- Landing page development — client dev team or separate project scope
- Third-party tools (CallRail, SEMrush, etc.) — subscriptions billed separately
- Additional platforms beyond original scope — add $300–$500/platform

---

## 4. Platform-Specific Architecture Templates

### 4.1 LinkedIn Ads

**Default campaign structure:**
```
Campaign: [Segment]_LeadGen
├── Ad Set A: [Primary Title/Function Target]          ~35% budget
│   ├── Target: Job Title, Industry, Company Size
│   ├── Format: Single Image Ad → Lead Gen Form
│   └── Bid: Max Conversions
│
├── Ad Set B: [Secondary Title Target]                  ~35% budget
│   ├── Target: Job Titles, Skills
│   ├── Format: Carousel Ad → Lead Gen Form
│   └── Bid: Max Conversions
│
└── Ad Set C: [Adjacent Industry / Persona]            ~30% budget
    ├── Target: Industry + Seniority
    ├── Format: Video / Document Ad → Landing Page
    └── Bid: Max Conversions
```

**LinkedIn benchmarks (fintech/payments/B2B SaaS):**
- Avg CPC: $6–$12
- Lead Gen Form conversion rate: 3–8%
- Est. CPL: $75–$400 (varies heavily by industry and seniority)
- Recommended minimum budget per ad set: $500/month

**Targeting rules:**
- Geography: Limit to English-speaking, crypto/tech-friendly jurisdictions unless otherwise specified
- Audience expansion: OFF at budgets under $5K — keep targeting tight
- Lead Gen Form fields: First Name, Last Name, Company, Work Email, + 1 qualifying question (e.g., "Monthly ad spend range")
- Exclude: Students, entry-level, internship roles

### 4.2 Google Ads

**Default campaign structure:**
```
Campaign: Search_BOF_Intent
├── Ad Group: [Core Product/Service Keywords]           ~45% budget
│   ├── 8–12 phrase-match + 3–5 exact-match keywords
│   ├── RSA with 12–15 headlines
│   └── Negatives: "free," "jobs," "reviews," unrelated modifiers
│
├── Ad Group: [Secondary/Adjacent Keywords]             ~30% budget
│   ├── 6–10 phrase-match variants
│   └── Negatives from Ad Group A learnings
│
├── Ad Group: Brand + Competitor Defense                 ~15% budget
│   ├── Brand name (exact + phrase)
│   ├── Competitor names (low-volume, defense only)
│   └── Separate budget cap
│
└── Remarketing: Display                                 ~10% budget
    ├── Target: Website visitors (30-day cookie)
    ├── Format: Responsive Display
    └── Frequency cap: 3–4/day
```

**Google Ads benchmarks (fintech/SaaS):**
- Avg Search CPC: $2–$8
- Conversion rate: 3–10%
- Est. CPA: $20–$260
- Display remarketing CPM: $2–$6

**Targeting rules:**
- Geography: Match business jurisdiction; start English-speaking markets
- Device: Desktop priority for B2B fintech (mobile bid adjustment −10% to −20%)
- Ad schedule: Business hours in target timezones (Mon–Fri, 6am–10pm)
- Landing pages: Match query intent — dedicated pages per keyword theme (not homepage)

### 4.3 Meta Ads (Facebook + Instagram)

**Default campaign structure:**
```
Campaign: [Audience]_Awareness
├── Ad Set A: [Interest-Based Audience]                 ~40% budget
│   ├── Target: Interests, Behaviors, Demographics
│   ├── Format: Video (15–30s, 9:16) → Landing Page
│   └── Optimization: Landing Page Views
│
├── Ad Set B: [Lookalike / Broad Audience]              ~30% budget
│   ├── Target: Lookalike (1–3%) of customer list
│   ├── Format: Carousel → Landing Page
│   └── Optimization: Link Clicks
│
└── Ad Set C: Retargeting                               ~30% budget
    ├── Target: Page engagers + website visitors (30d)
    ├── Format: Single Image + Social Proof
    └── Optimization: Conversions
```

**Meta benchmarks (crypto/fintech/tech):**
- Avg CPM: $5–$15
- CTR: 0.6–2.0%
- Est. CPC: $0.25–$2.50
- Landing page view rate: 60–80% of clicks
- Conversion rate (LP view → sign-up): 2–6%

**Placement defaults:**
- Instagram Feed + Stories: 60%
- Facebook Feed: 30%
- Reels: 10%
- Audience Network: OFF (quality concerns for B2B)

---

## 5. KPI Framework

### 5.1 Cross-Platform Success Criteria (Pilot)

| Tier | Threshold | Decision |
|------|-----------|----------|
| **Green** | Blended CPA < $100 or 30+ qualified leads | Scale budget 2–3× for Month 2; add channels |
| **Yellow** | Blended CPA $100–$200 or 15–29 leads | Optimize creative/audiences; maintain budget; re-evaluate |
| **Red** | Blended CPA > $200 or < 15 leads | Full audit: audience, creative, landing page CRO. Pause underperformers. |

Adjust CPA thresholds based on client LTV:
- LTV < $500 → Green threshold: CPA < $50
- LTV $500–$2,000 → Green threshold: CPA < $100
- LTV $2,000–$10,000 → Green threshold: CPA < $200
- LTV $10,000+ → Green threshold: CPA < $500

### 5.2 Conversion Tracking Checklist

| Platform | Must-Track Events | Tracking Method |
|----------|------------------|-----------------|
| LinkedIn | Lead Gen Form submit, Landing page demo request | LinkedIn Insight Tag + event snippet |
| Google Ads | Sign-up, Demo request, Phone call (optional) | Google Ads tag + GA4 events |
| Meta | Landing page view, Sign-up/registration, Lead | Meta Pixel + CAPI (Conversions API) |

### 5.3 Reporting Cadence

- **Weekly (internal)**: Spend pace, CTR by campaign, CPA trend, top-performing creative
- **Biweekly (client)**: Cross-channel dashboard, lead quality, budget reallocation recommendations
- **End-of-Campaign (client)**: Full performance report with Month 2 scale recommendation

---

## 6. Pre-Launch Checklist

Always include this 10-step checklist in the media plan:

| # | Task | Owner | Timing |
|---|------|-------|--------|
| 1 | Confirm ad account access (LinkedIn, Google, Meta Business Suite) | Client | Week 0 |
| 2 | Install Meta Pixel + CAPI, LinkedIn Insight Tag, GA4 + Google Ads tag | Agency | Week 0 |
| 3 | Platform ad policy pre-clearance (if in restricted vertical: crypto, finance, health) | Agency | Week 0 |
| 4 | Build primary landing page(s) | Client | Week 0 |
| 5 | Build secondary/retargeting landing page if needed | Client | Week 0 |
| 6 | Creative production: video, statics, carousel | Client/Agency | Week 0 |
| 7 | Audience seed lists (CRM uploads, lookalike sources) | Client | Week 0 |
| 8 | Conversion tracking QA — test all events firing | Agency | Week 0 |
| 9 | Campaign build-out + internal review | Agency | Week 0 |
| 10 | **GO LIVE** | — | Week 1, Day 1 |

---

## 7. 4-Week Flight Plan Template

| Week | Phase | Activities |
|------|-------|------------|
| **Week 0** | Setup | Pixel/event setup, audience building, creative production, landing page prep, conversion tracking QA |
| **Week 1** | Launch + Learn | All campaigns live. Monitor CTR, CPC, early conversion signals. No pausing — let algorithms learn. |
| **Week 2** | Optimization I | Cut bottom 20% of ad creatives. Add negative keywords from search term reports. Adjust audiences. |
| **Week 3** | Optimization II | Scale winning ad sets (+15–20% budget shift). Pause underperformers. Test 1–2 new creative variants. |
| **Week 4** | Consolidate + Report | Final optimization pass. Compile cross-channel performance report. Deliver pilot insights + scale recommendation. |

---

## 8. Scale Path Template (Month 2+)

| Pilot Outcome | Month 2 Budget | New Channels / Tactics |
|---------------|---------------|----------------------|
| **Green** (>30 leads, CPA under threshold) | 2–3× pilot budget | Add TikTok Ads, LinkedIn Conversation Ads, YouTube pre-roll |
| **Yellow** (15–29 leads, CPA moderate) | 1–1.5× pilot budget | Consolidate top-performing channel + audience. Test 1 new creative angle. |
| **Red** (<15 leads, CPA high) | Same or reduced | Before scaling: full audit → landing page CRO → creative refresh → retargeting-only pivot |

---

## 9. Media Plan Generation Workflow

When asked to generate a media plan:

1. **Gather inputs**: Client name, industry, product/service, target audiences, total budget, campaign duration, existing ad accounts, landing page status, creative capacity
2. **Map audiences to channels**: Which segments are on which platforms? B2B → LinkedIn priority. Visual/B2C → Meta priority. Intent-driven → Google priority.
3. **Determine budget split**: Apply channel role framework (§2). Subtract agency fee + creative support from total to get net media spend.
4. **Build platform architectures**: Use the templates in §4, customized with client-specific targeting, keywords, and formats.
5. **Define creative messaging**: Per-audience pain points → Xerovan promise equivalent → key message → ad format assignments (§5 in the reference plan).
6. **Set KPIs and success thresholds**: Use §5, adjusted for client LTV.
7. **Structure fees**: Apply §3. State what's included and excluded explicitly.
8. **Compile and deliver**: Follow the document structure in §1. End with the pre-launch checklist and scale path.

### Customization Points per Client

- Total budget and fee model
- Number of channels (adjust based on budget sufficiency check, §2.3)
- Audience segments and their channel mapping
- Platform-specific targeting (job titles, interests, keywords)
- CPA/CPL thresholds (based on client LTV)
- Creative capacity (in-house vs. agency-provided)
- Jurisdictional restrictions (crypto, finance, health verticals)
- Campaign duration (default 4 weeks; adjust for longer pilots)
