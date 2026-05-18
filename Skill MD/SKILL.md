---
name: gnext-gxlocate-proposal
description: Generate structured website migration / redesign proposals for GNEXT × GXLOCATE clients. Use when building a proposal document for a client website project (migration, rebuild, redesign), when the user mentions GNEXT, GXLOCATE, Career Lab, website audit, pricing plans, or proposal generation, or when asked to apply the GXLOCATE Portfolio System design tokens to a new document.
---

# GNEXT × GXLOCATE Proposal System

This skill equips you to generate consistent, brand-aligned proposal documents for GNEXT × GXLOCATE — two award-winning UAE digital firms operating from a single office in MBZ City. The reference proposal at `careerlab-pitch.html` is the canonical output; everything below distills its patterns into reusable building blocks.

## Quick Reference: When to Load Additional Files

- **Full proposal HTML template**: The `careerlab-pitch.html` file in the project workspace is the canonical reference. Load it when you need exact CSS or structural patterns.
- **Client details / RFP**: Check `Client detail/` for client PDFs and assets.
- **Logos**: Available in `Logos/` directory — use in footer and hero sections.

---

## 1. Design System — GXLOCATE Portfolio System

### 1.1 Color Tokens

```
--navy:       #0B1D3A    (backgrounds, footer, dark sections)
--navy-light: #0F2650    (subtle variations)
--blue:       #1A56DB    (primary accent, links, interactive)
--cyan:       #00C2FF    (highlight, emphasis, badges, featured)
--mid-blue:   #2D7DD2    (mid-tone transitions)
--light-blue: #E8F4FD    (tinted backgrounds, code blocks)
--off-white:  #F9FAFB    (page background)
--white:      #FFFFFF    (card backgrounds, light sections)
--dark:       #111827    (body text)
--steel:      #4B5563    (secondary text, descriptions)
--border:     #E5E7EB    (card borders, dividers)
--muted:      #9CA3AF    (subtle text, footnotes)
```

### 1.2 Gradients

**Hero / dark section gradient:**
```css
--grad-hero: linear-gradient(135deg, #0B1D3A 0%, #1A3A7A 60%, #1A56DB 100%);
```
Direction: 135° (top-left to bottom-right). Used on: hero header, CTA section.

**Accent / interactive gradient:**
```css
--grad-accent: linear-gradient(90deg, #1A56DB 0%, #00C2FF 100%);
```
Direction: left-to-right. Used on: accent lines, buttons, stat values, hover effects, card top borders.

### 1.3 Typography

```
--font-body: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
--font-mono: 'JetBrains Mono', 'Courier New', monospace;
```

Load from Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700;14..32,800;14..32,900&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet" />
```

**Type scale rules:**
- Hero heading: `clamp(2.6rem, 6vw, 4.6rem)`, weight 900
- Section titles: `clamp(1.8rem, 3.8vw, 2.8rem)`, weight 800
- Labels / eyebrows: `0.68rem`, weight 700, letter-spacing `0.16em`, uppercase
- Body: `16px` / `1rem`, weight 400, line-height 1.6
- Meta / footnotes: `0.62–0.78rem`, weight 500–700
- Monospace used for: plan prices, code snippets, section numbers, footer meta, office notes

### 1.4 Border Radii

```
--radius-sm: 10px   (badges, pills, small cards)
--radius-md: 14px   (cards, stat blocks)
--radius-lg: 18px   (partner cards, plan cards)
```

### 1.5 Visual Patterns

**Accent line**: 52–60px wide, 3px tall, `var(--grad-accent)`, `border-radius: 2px`. Always placed below the section lead text with `margin: 18px 0 40px`.

**Card hover pattern**: All cards use `transition: 0.22s` and lift on hover via `transform: translateY(-3px)` or `-4px`, with a `box-shadow` using `rgba(26,86,219,0.07–0.1)`. Card top borders (3px height) animate from opacity 0 → 1 on hover using the accent gradient.

**Hero glow orbs**: Two pseudo-element radial gradients behind the hero — one cyan-tinted in the top-right, one blue-tinted bottom-center. Non-interactive, `pointer-events: none`.

**Section alternation**:
- Default sections: `background: var(--off-white)`
- Alt sections: `background: var(--white)` (`section-alt`)
- Dark sections: `background: var(--navy)` (`section-dark`), with white text and cyan accents

**Responsive breakpoints**: 640px, 720px, 800px, 860px, 880px, 920px, 960px, 1600px. Cards stack to single column at 640px. Plans go 3-column at 920px.

---

## 2. Service Provider Profiles

### 2.1 GNEXT LLC

- **Type**: Full-service digital agency
- **Tagline**: Brand · Web · Marketing
- **Description**: Full-service digital firm specialising in brand strategy, web engineering, software development, and performance marketing — building end-to-end digital foundations for growth-oriented UAE businesses.
- **TechBehemoths 2025 Awards**: WordPress, SEO, PPC
- **Email**: info@gnext.ae
- **Website**: www.gnext.ae
- **Phone**: +971 55 611 5985 · +971 50 611 5911
- **Services**: Web Development, Brand Strategy, Performance Marketing, PPC & Paid Social, Software Development, UI/UX Design, Content Strategy, Digital Consulting

### 2.2 GXLOCATE

- **Type**: Local SEO & GBP specialist
- **Tagline**: Local SEO · GBP Specialist
- **Description**: Specialist local SEO and search visibility firm — helping UAE businesses locate their audience, optimise their digital presence, and dominate local search results across Google and the wider search ecosystem.
- **TechBehemoths 2025 Awards**: WordPress, Web Development, SEO
- **Email**: info@gxlocate.com
- **Website**: www.gxlocate.com
- **Phone**: +971 58 556 8611
- **Services**: Local SEO, GBP Management, GBP Reinstatement, Google Maps Optimisation, Citation Building, Review Strategy, Keyword Research, Competitor Analysis

### 2.3 Office

- **Address**: Mazyad Mall, Tower 1, Office 603, MBZ City, Abu Dhabi, UAE
- Both firms operate from the same office floor.

### 2.4 Additional Recognition

- **DesignRush**: UAE Top SEO Agency (both firms)
- **Total awards**: 6 TechBehemoths 2025 Awards across WordPress, SEO, PPC, and Web Development

### 2.5 Portfolio Industries

Interior & Construction, Industrial & Engineering, Maritime & Logistics, Legal Services, Fashion & Retail, Auto Services, Industrial Heritage, Print & Advertising, Locksmith & Keys, Moving & Transport, Restaurant & F&B.

### 2.6 Key Stats for Hero Section

- 40+ clients built across UAE
- 11 industries served
- 6× TechBehemoths 2025 Awards
- 10-week (or 4–6 week) kickoff-to-live timeline (adjust per project scope)

---

## 3. Website Audit Framework

When auditing a client's existing website, produce findings in three severity tiers. Each finding follows this structure:

### 3.1 Severity Levels

| Level | Color | Dot | Border-left |
|-------|-------|-----|-------------|
| Critical | `#DC2626` (red) | Solid red dot | 4px red |
| Warning | `#D97706` (amber) | Solid amber dot | 4px amber |
| Opportunity | `#059669` (green) | Solid green dot | 4px green |

### 3.2 Finding Card Structure

Each finding card contains:
1. **Header row**: severity badge (dot + label) + finding number (`FINDING 01`, etc.)
2. **Title**: bold, navy, descriptive headline
3. **Finding body**: plain explanation, with `<code>` for URLs/technical terms, `<strong>` for key phrases
4. **Impact footer**: bordered-top section explaining "Why it matters" with concrete business impact

### 3.3 Common Audit Categories to Check

- **SEO metadata**: page titles, meta descriptions, duplicate content
- **URL structure**: clean vs. platform-specific slugs (e.g., `/slides` vs. `/programs/name`)
- **Indexed admin/backend pages**: security risk
- **Content architecture**: thin pages, buried USPs, missing landing pages
- **Structured data / schema**: FAQ, Course, Event, EducationalOrganization, LocalBusiness
- **Content engine**: blog, insights, top-funnel content gaps
- **Performance**: Core Web Vitals, mobile responsiveness, page speed
- **Security**: SSL, admin URL exposure, CMS version leaks
- **Brand presentation**: homepage hero messaging, USP visibility

### 3.4 Audit Closing Statement

Always close the audit section with a summary card that:
- Acknowledges the content/programmes are strong; issues are platform limitations
- Frames migration as the unified solution to all findings
- Uses a blue left-border callout style

---

## 4. Three-Tier Pricing Plan Structure

Every proposal uses three clearly differentiated plans: **Starter**, **Professional** (featured/recommended), and **Premium**. Each plan includes one-time build pricing and an optional monthly maintenance tier.

### 4.1 Plan Card Anatomy

Each plan card contains:
1. **Eyebrow**: `Plan 0X · Plan Name`
2. **Plan name**: Large, weight 900
3. **Tagline**: Italic, one-line value proposition
4. **Price**: Currency label + large amount + "/one-time" unit
5. **Monthly sub-note**: "+ optional **AED XXX/mo** TierName maintenance"
6. **Best-for statement**: Italic, below a bordered separator
7. **Collapsible details**: Toggle button → expandable sections
8. **CTA button**: Gradient button with arrow

### 4.2 Plan Detail Sections (Standard)

Each plan's collapsible details include these sections:
- **Design & Development**: Theme type, page count, responsiveness, brand alignment
- **Content Migration**: Page count, redirects, image optimisation
- **Features Included**: Course catalog, events, forms, gallery, maps, social
- **Technical & SEO**: SSL, caching, analytics, backups, security
- **Hosting · Training · Support**: Hosting tier, training sessions, admin guide, post-launch support

### 4.3 Professional Plan (Featured)

The middle plan is always the recommended tier. It:
- Has `.plan-featured` class with elevated styling
- Gets a pulsing "★ Recommended" badge above the card
- Is elevated 14px above sibling cards on desktop
- Everything in Starter, plus advanced features, schema markup, GBP audit by GXLOCATE, staging environment
- Higher Core Web Vitals target

### 4.4 Premium Plan

- Fully custom design (zero template baseline)
- Unlimited pages, multi-language RTL-ready architecture
- CRM integration, payment gateways, live chat
- Full GXLOCATE SEO boost (technical audit, competitor benchmarking, CRO setup)
- Dedicated account manager, 6-month post-launch support

### 4.5 Comparison Table

A horizontal-scroll table with these section rows:
- Design & UI/UX
- Content Migration
- Features at Launch
- SEO & Performance
- Security & Hosting
- Training & Support
- Monthly Maintenance Tier

Headers: Feature | Starter (AED X) | Professional (AED Y ★) | Premium (AED Z)

### 4.6 Pricing Note Footer

```
All prices in AED · Exclusive of 5% UAE VAT · 50% upfront, 50% on launch · Year 1 hosting included
```

---

## 5. Maintenance Tiers

Aligned one-to-one with the build plans:

### 5.1 Essential (for Starter)
- AED 300/month or AED 3,200/year
- SLA: 24-hour ticket response, business hours
- Weekly backups, monthly updates, basic security, uptime monitoring, monthly report
- Excludes: content changes, new features, design work

### 5.2 Growth (for Professional)
- AED 600/month or AED 6,500/year
- SLA: 12-hour ticket response, Mon–Sat
- Daily backups (90-day retention), weekly updates, active security + malware scanning
- 2 hours/month included for content updates, image swaps, minor edits
- Quarterly SEO health check, priority bug fixes

### 5.3 Enterprise (for Premium)
- AED 1,200/month or AED 13,000/year
- SLA: 4-hour ticket response, priority queue, 7 days
- Daily geo-replicated backups, real-time security + intrusion prevention
- 5 hours/month for content, dev, or design work
- Quarterly business review, dedicated account manager, after-hours hotline

---

## 6. Delivery Timeline

Standard: 4 weeks / 5 phases for Starter and Professional. Premium: 5–6 weeks.

| Phase | Name | Days |
|-------|------|------|
| 01 | Discovery | 1–4 |
| 02 | Design | 5–11 |
| 03 | Development | 12–22 |
| 04 | Testing | 23–27 |
| 05 | Launch | 28–30 |

Each phase card includes: phase number, day range, italic title, and a bullet-style description of activities. Always add a timeline-note disclosure about Premium requiring extra time.

---

## 7. Proposal Document Structure (Section Order)

The canonical proposal follows this exact section sequence:

1. **Navigation** — Fixed top bar with GNEXT × GXLOCATE logo link + RFP reference badge
2. **Hero** — RFP badge, headline with `<em>` emphasis, sub-description, divider, 4 stat blocks
3. **Recognition Strip** — TechBehemoths certificates + DesignRush badge
4. **01 — Understanding the Brief** — Label, title, lead, 6 brief-cards in a grid
5. **02 — Audit Findings** — Label, title, lead, severity legend, 6–10 audit cards, closing statement
6. **03 — Service Providers** — Label, title, lead, 2 partner cards, office-note
7. **04 — Three Plans** — Label, title, lead, 3 plan cards, pricing-note footer
8. **05 — Comparison Table** — Label, title, lead, horizontal-scroll table
9. **06 — Maintenance Tiers** — Label, title, lead, 3 maint-cards
10. **07 — Delivery Timeline** — Label, title, lead, 5 timeline steps, disclosure note
11. **08 — Why Us** — Dark section: label-light, title-white, lead-white, 6 why-cards
12. **09 — Selected Recent Work** — 8 portfolio cards in a grid
13. **CTA / Contact** — Dark gradient CTA with 2 contact cards
14. **Footer** — 4-column grid: brand, GXLOCATE, GNEXT, quick links + bottom bar

---

## 8. Proposal Generation Workflow

When asked to generate a proposal:

1. **Gather inputs**: Client name, existing website URL, RFP reference number, known pain points, desired outcomes
2. **Audit the live site** if accessible: check page titles, meta descriptions, URL structure, schema markup, page speed, security
3. **Map findings to severity tiers**: critical / warning / opportunity
4. **Determine pricing**: Use the three-tier framework. Adjust AED amounts based on project scope — the reference values (4,000 / 7,500 / 11,000) are for a mid-complexity training/education site. Scale up for e-commerce, multilingual, or heavy custom functionality.
5. **Build the HTML**: Use the design tokens and section structure from this skill. Reuse the CSS verbatim from `careerlab-pitch.html` for visual consistency.
6. **Swap client-specific content**: Replace Career Lab references with the new client's details throughout.
7. **Verify all links and references** point to the correct client assets.

### Customisation Points per Client

- Hero headline and sub-description
- RFP reference number
- Brief cards (6 items tailored to the client's brief)
- Audit findings (generated from live site inspection)
- Plan pricing (scale based on project complexity)
- Portfolio items (select relevant industries from the portfolio list)
- CTA contact information
- Timeline (adjust if scope differs significantly)
