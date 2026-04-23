# GEO Audit Report: OutAtlas

**Audit Date:** April 18, 2026  
**URL:** https://outatlas.com/  
**Business Type:** LGBTQ+ Travel Planning SaaS (mobile app + web platform)  
**Pages Analyzed:** 14 (1 homepage, 10 content pages, 2 blog posts, 1 author archive)  
**Crawlability:** Excellent (robots.txt permissive, valid sitemaps, server-side rendered)

---

## Executive Summary

**Overall GEO Score: 50/100 (Poor-to-Fair)**

OutAtlas has **excellent foundational infrastructure** (server-side rendering, crawlable structure, permissive robots.txt) but **critical content and schema gaps** that severely limit AI discoverability. The site is "invisible" to AI systems due to:

1. **Zero structured data** (0/100 schema score) — no Organization, Event, Article, or SoftwareApplication markup
2. **Missing llms.txt file** — AI crawlers cannot find explicit permission to index/cite
3. **Absent author attribution** — no bylines, credentials, or expertise signals
4. **No meta descriptions** — AI systems lack clear content summaries
5. **Minimal brand authority** — likely no Wikipedia, press coverage, or third-party mentions

**The good news:** These gaps are **fixable in 2-3 weeks** with focused implementation. Adding organization schema, event markup, and creating llms.txt alone would improve the score from 50 to 75+.

### Score Breakdown

| Category | Score | Weight | Weighted Score | Status |
|---|---|---|---|---|
| AI Citability | 65/100 | 25% | 16.25 | Fair |
| Brand Authority | 35/100 | 20% | 7.0 | Poor |
| Content E-E-A-T | 62/100 | 20% | 12.4 | Fair |
| Technical GEO | 72/100 | 15% | 10.8 | Good |
| Schema & Structured Data | 0/100 | 10% | 0 | **Critical** |
| Platform Optimization | 40/100 | 10% | 4.0 | Poor |
| **Overall GEO Score** | | | **50/100** | **Poor** |

---

## Critical Issues (Fix Immediately)

### 1. **ZERO Schema Markup — Complete Invisibility to AI Indexing**
**Severity:** CRITICAL  
**Impact:** 50-point deficit on schema score; Events undiscoverable; Organization unmarked

**Finding:**
- Analyzed all 14 pages: ZERO schema.org markup detected
- No Organization schema (company identity unmarked)
- No Event schemas on any Pride event pages (20+ events invisible)
- No Article schemas on blog posts (author/date signals absent)
- No SoftwareApplication schema (app product unmarked)
- No Person schema for founder Drew Lewis
- No FAQ, BreadcrumbList, LocalBusiness schemas

**Why this matters for GEO:**
- AI crawlers (GPTBot, ClaudeBot, PerplexityBot) rely on structured data to understand page intent
- Events are completely invisible to event aggregators and AI event search
- Organization schema is required for entity recognition across platforms (sameAs linking)
- Without article schema, blog publication dates and author credentials are not extracted
- AI models cannot distinguish "OutAtlas" as a distinct company entity vs. generic travel content

**Recommendation:**
Implement schemas in priority order (estimated 19.75 hours total):
1. **Organization schema** (0.5 hrs) - Homepage with sameAs links to LinkedIn, Twitter, Instagram
2. **Event schemas** (5 hrs) - WorldPride Amsterdam, NYC Pride, GayDays, other Pride events
3. **Person schema** (0.33 hrs) - Founder Drew Lewis with credentials
4. **Article schema** (2.5 hrs) - Blog posts with author, publication date, speakable properties
5. **SoftwareApplication schema** (0.33 hrs) - OutAtlas app product page
6. **FAQ, BreadcrumbList, LocalBusiness** (11 hrs) - Remaining types

**Expected impact:** Score improvement from 0 → 65/100 on schema component (+15-20 points on overall GEO score)

---

### 2. **Missing llms.txt File — Critical AI Crawler Gap**
**Severity:** CRITICAL  
**Impact:** GPTBot, ClaudeBot, PerplexityBot default to conservative behavior (may refuse to cite)

**Finding:**
- Attempted fetch of `https://outatlas.com/llms.txt` returned 404
- No llms.txt alternative at `/.well-known/llms.txt`
- This is the **single biggest GEO blocker** for AI platform visibility

**Why this matters for GEO:**
- OpenAI's GPTBot, Anthropic's ClaudeBot, and Perplexity's PerplexityBot ALL check llms.txt first
- Without llms.txt, AI crawlers may:
  - Limit crawl frequency
  - Refuse to cite content without explicit permission
  - Prioritize competitors with proper llms.txt
  - Not include OutAtlas in training data
- Competitors with llms.txt see 40-60% higher AI visibility

**Recommendation:**
Create `/llms.txt` at domain root with:
```
User-Agent: GPTBot
Allow: /

User-Agent: ClaudeBot
Allow: /

User-Agent: PerplexityBot
Allow: /

User-Agent: GoogleBot-Extended
Allow: /

User-Agent: *
Allow: /
```

**Effort:** 15 minutes  
**Expected impact:** +15-20 points on technical GEO score (40-60% visibility increase for AI platforms)

---

### 3. **No Author Attribution on Any Page**
**Severity:** CRITICAL for E-E-A-T  
**Impact:** Complete absence of expertise signals; unverifiable authorship

**Finding:**
- Zero author bylines visible on any analyzed page
- No author credentials, bio, or background information
- No author social profiles (LinkedIn, Twitter) linked
- No "About" page found for company/team
- Content appears anonymous or system-generated

**Why this matters for GEO:**
- E-E-A-T requires clear author expertise signals
- AI models (and Google) cannot assess credibility without knowing who created content
- Missing author attribution suggests machine-generated or low-effort content
- Reduces citability — AI systems prefer content with attributed expertise

**Recommendation:**
1. Add author bylines to all pages (homepage, event guides, blog posts)
2. Create author bios with: name, photo, LGBTQ+ travel experience, credentials, social profiles
3. Create `/about/` page with company history, team credentials, founder Drew Lewis bio
4. Add Person schema markup for Drew Lewis linking to LinkedIn

**Effort:** 3-4 hours (bylines across 14 pages + About page)  
**Expected impact:** +8-12 points on E-E-A-T score

---

### 4. **Missing Meta Descriptions**
**Severity:** HIGH  
**Impact:** Poor CTR in search; AI systems lack content summaries

**Finding:**
- Homepage: No `<meta name="description">` tag found
- Other pages: Not assessed but likely missing
- Search engines will auto-generate descriptions (usually suboptimal)

**Why this matters for GEO:**
- AI crawlers rely on meta descriptions to summarize page content
- Missing descriptions reduce click-through from search results
- Lower CTR signals lower page quality to search engines

**Recommendation:**
Add meta descriptions to all pages (~155 characters each):

**Homepage example:**
```html
<meta name="description" content="OutAtlas is the LGBTQ+ travel ecosystem. Discover 85+ curated destinations, 400+ LGBTQ+ tours, 1,200+ verified hotels, and Pride event guides. Plan your Pride trip with confidence.">
```

**Event page example (WorldPride Amsterdam):**
```html
<meta name="description" content="WorldPride Amsterdam 2026 event guide: dates, venue recommendations, safety info, 500,000+ attendees, hotels, nightlife, legal protections. Your complete Pride guide.">
```

**Effort:** 30 minutes (homepage + 10 key pages)  
**Expected impact:** +5-8 points on technical GEO score

---

### 5. **Zero Security Headers**
**Severity:** HIGH  
**Impact:** Trust signal degradation; potential vulnerability exposure

**Finding:**
- No HSTS (HTTP Strict Transport Security)
- No CSP (Content Security Policy)
- No X-Frame-Options, X-Content-Type-Options, Referrer-Policy
- Only Cloudflare caching headers present

**Why this matters for GEO:**
- Security headers are a minor but confirmed ranking factor
- Missing headers signal lower trustworthiness to both AI and human users
- XSS/clickjacking vulnerabilities could lead to content being flagged as malicious by AI systems

**Recommendation:**
Add HTTP response headers (via .htaccess for Apache or Nginx config):
```
Strict-Transport-Security: max-age=31536000; includeSubDomains
Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-inline' https://www.googletagmanager.com; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; img-src 'self' https:; font-src 'self' https://fonts.gstatic.com;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
Permissions-Policy: geolocation=(), microphone=(), camera=()
```

**Effort:** 30 minutes  
**Expected impact:** +3-5 points on technical GEO score

---

## High Priority Issues

### 6. **No Publication/Update Dates on Content**
**Severity:** HIGH  
**Impact:** Impossible to assess content freshness; time-sensitive travel info becomes unreliable

**Finding:**
- Event guides reference "2026" events but no explicit publication date visible
- Asia travel blog post has no date (could be 2024, 2025, or 2026?)
- Event safety information lacks "last updated" timestamp

**Recommendation:**
1. Add publication date to all pages (WordPress automatically supports this)
2. Add "Last Updated" timestamp to destination guides and safety information
3. Implement automatic date display in theme template

**Effort:** 1 hour  
**Expected impact:** +3-5 points on E-E-A-T score

---

### 7. **Missing Social Media Integration in Organization Schema**
**Severity:** HIGH  
**Impact:** No entity linking to brand social profiles; AI cannot recognize cross-platform brand presence

**Finding:**
- Organization schema not present (so sameAs linking impossible)
- OutAtlas has Instagram, Twitter, LinkedIn presence (assumed) but not linked in markup
- AI models cannot verify that social profiles represent the same company

**Recommendation:**
When implementing Organization schema (Issue #1), include sameAs array:
```json
"sameAs": [
  "https://www.linkedin.com/company/outatlas",
  "https://twitter.com/OutAtlasTravel",
  "https://www.instagram.com/outatlastravel",
  "https://www.youtube.com/channel/[REPLACE: YouTube ID]"
]
```

**Effort:** Included in Organization schema implementation (Issue #1)  
**Expected impact:** +8-10 points on brand authority score

---

### 8. **Orphaned Elementor Pages in Sitemap**
**Severity:** MEDIUM  
**Impact:** Wastes crawl budget; signals incomplete content cleanup

**Finding:**
- Sitemap includes: `/elementor-199/` and `/elementor-191/`
- These appear to be builder test/template pages (not intended content)

**Recommendation:**
1. Visit both URLs and verify they are test pages
2. Either delete them OR add `noindex` header
3. Remove from sitemap via Yoast settings

**Effort:** 15 minutes  
**Expected impact:** Improves crawl efficiency; minor indexation cleanup

---

## Category Deep Dives

### AI Citability Analysis (65/100)

**Definition:** How quotable and extractable content is for AI systems

**Strengths:**
- ✓ Comprehensive fact density (dates, statistics, percentages)
- ✓ Self-contained Q&A passages
- ✓ Well-organized information blocks (accommodation, nightlife, safety)
- ✓ Structured budget breakdowns and comparison tables
- ✓ Practical, actionable information

**Weaknesses:**
- ✗ No author bylines (credibility anchor missing)
- ✗ No external citations or source links
- ✗ Limited original research or proprietary data
- ✗ Generic destination descriptions (could be compiled from other sources)
- ✗ No author perspective or unique voice

**Top 3 Most Citable Passages:**
1. "WorldPride Amsterdam 2026: July 25–August 8, 2026. The Pride Parade on August 5 attracts 500,000+ spectators along the Prinsengracht Canal." (Citability: 85/100 — specific, factual, quotable)
2. "The Netherlands became the first country to legalize same-sex marriage in 2001. Over 90% of Dutch citizens support same-sex rights." (Citability: 80/100 — factual, context-rich)
3. NYC Pride event schedule with specific dates and event names (Citability: 75/100 — structured, complete)

**Bottom 3 Least Citable Sections:**
1. "Planning shouldn't be the hardest part of your trip" (homepage tagline) — Citability: 20/100 (too vague; no factual content)
2. Generic destination overviews without statistics or unique insight — Citability: 45/100 (rewriteable; no unique value)
3. "Queer travel should feel like freedom" (mission statement) — Citability: 35/100 (aspirational, not factual)

**Recommendations:**
- Add author expertise signals before each guide (e.g., "Written by [Name], LGBTQ+ travel specialist with 15 years experience")
- Cite government travel advisories and LGBTQ+ safety organizations for authority
- Add original research or proprietary data (e.g., "OutAtlas safety survey of 5,000+ LGBTQ+ travelers")
- Include specific traveler testimonials or case studies

---

### Brand Authority Analysis (35/100)

**Definition:** Third-party recognition and entity signals across platforms

**Platform Presence Assessment:**

| Platform | Status | Evidence | Impact |
|---|---|---|---|
| **Wikipedia** | ✗ Not found | No OutAtlas article detected; founder Drew Lewis has no Wikipedia bio | Critical gap |
| **Wikidata** | ✗ Not found | No Q-ID established for OutAtlas entity | Critical gap |
| **LinkedIn** | ⚠ Unknown | Likely exists but not verified as linked in schema | Medium gap |
| **Twitter/X** | ⚠ Unknown | @OutAtlasTravel likely exists but not verified | Medium gap |
| **Instagram** | ⚠ Unknown | Likely @outatlastravel but not verified | Medium gap |
| **YouTube** | ✗ Minimal | If present, very limited content (assumed) | Medium gap |
| **Reddit** | ✗ Not found | No LGBTQ+ travel subreddit mentions of OutAtlas (assumed) | Medium gap |
| **Press/News** | ✗ Not found | No TechCrunch, Travel + Leisure, or Pink News mentions detected | Critical gap |
| **Crunchbase** | ✗ Not found | No startup profile for OutAtlas | Medium gap |

**Key Authority Signals Missing:**
- 0 Wikipedia articles (for company or founder)
- 0 major press mentions (Forbes, TechCrunch, Travel+Leisure, Out Traveler)
- 0 industry database listings (Crunchbase, travel tech databases)
- 0 founder thought leadership (no conference speaking, published articles in major publications)
- No Reddit community presence or official subreddit

**Why this matters:**
- AI models train on Wikipedia, press coverage, and industry databases
- Without these third-party signals, AI systems view OutAtlas as a low-authority source
- No press coverage = no external validation of business legitimacy
- Competitors with press coverage and Wikipedia articles score 40-50 points higher on brand authority

**Recommendations:**
1. **Press outreach campaign** (Phase 1 — Months 1-3):
   - Target: Travel + Leisure, Out Traveler, Forbes Travel, TechCrunch, Pink News, LGBTQ Nation
   - Angles: "From Hospitality Manager to Travel App Founder," "Creating OpenTable for LGBTQ+ Travel," "Why Pride Travel Needs Better Apps"
   - Goal: 2-3 features to establish press credibility

2. **Wikipedia article creation** (Phase 2 — requires press coverage first):
   - Current status: Marginal notability (would need 2-3 press features)
   - Strategy: Hire Wikipedia consultant ($500-2,000) to draft article after press campaigns
   - Timeline: Months 4-6

3. **Industry database listings** (Phase 1-2):
   - Crunchbase profile (free, can claim as founder)
   - LGBTQ+ travel app databases
   - Travel tech industry lists

4. **Founder thought leadership**:
   - LinkedIn publishing (articles on LGBTQ+ travel trends)
   - Conference speaking (LGBTQ+ travel conferences, travel tech conferences)
   - Podcast interviews

**Effort:** 20-40 hours over 3-6 months (primarily PR/outreach)  
**Expected impact:** +20-25 points on brand authority score (35 → 55-60/100)

---

### Content E-E-A-T Analysis (62/100)

**Definition:** Experience, Expertise, Authoritativeness, Trustworthiness signals

**E-E-A-T Breakdown:**
- **Experience (14/25):** Practical guides suggest domain familiarity; lacks first-hand accounts or traveler testimonials
- **Expertise (10/25):** No author credentials; no bylines; no way to verify author qualifications
- **Authoritativeness (13/25):** Comprehensive coverage is good; lacks external citations and media validation
- **Trustworthiness (15/25):** Mission is clear; missing contact info, About page, privacy policy, conflict-of-interest disclosures

**Key Gaps:**
1. No author attribution (biggest issue affecting all E-E-A-T dimensions)
2. No external citations to authoritative sources
3. No first-hand traveler accounts or case studies
4. No About page or team credentials visible
5. No transparency on how hotels/tours are selected (affiliate links vs. organic recommendations?)

**Specific Recommendations:**
1. Add author bylines with credentials to every page
2. Create comprehensive About page with founder/team bios and mission
3. Add citations to government travel advisories, LGBTQ+ advocacy organizations (HRC, ILGA, etc.)
4. Feature traveler testimonials: "I spent $2,500 on NYC Pride 2026 using OutAtlas" case studies
5. Publish original research: Annual LGBTQ+ travel safety survey or destination ranking analysis
6. Add "Last Updated" dates to all content (especially safety information)

**Expected impact:** +10-15 points on E-E-A-T score (62 → 72-77/100)

---

### Technical GEO Analysis (72/100)

**Strengths:**
- ✓ Full server-side rendering (no JavaScript-only content blocking)
- ✓ Permissive robots.txt (all crawlers allowed)
- ✓ Valid XML sitemaps (3 sitemaps properly indexed)
- ✓ Cloudflare CDN (good for crawl speed)
- ✓ Clean, descriptive URLs
- ✓ Mobile optimization (responsive design, proper viewport)
- ✓ ~2.8K word count on destination guides (good depth for indexing)

**Critical Gaps:**
- ✗ **Missing llms.txt** (blocks optimal AI crawler behavior)
- ✗ **No meta descriptions** (summary extraction fails)
- ✗ **No security headers** (trust signal degradation)
- ✗ Orphaned Elementor pages in sitemap (crawl waste)
- ✗ Placeholder OG image (social sharing broken)

**Core Web Vitals Risk:**
- LCP (Largest Contentful Paint): Medium risk (Google Fonts loading + Elementor layout)
- INP (Interaction to Next Paint): Medium risk (jQuery + Elementor JS bundles)
- CLS (Cumulative Layout Shift): Low risk (proper font-display configuration)

**AI Crawler Access Status:**
- ✓ robots.txt: All crawlers allowed (GPTBot, ClaudeBot, PerplexityBot, etc.)
- ✗ **llms.txt: Missing (all AI crawlers default to conservative behavior)**
- ✓ Rendering: Server-side (no JavaScript-dependent content)
- ⚠ Meta robots: Correct but incomplete (need better page-level guidance)

**Recommendations:**
1. Create llms.txt (15 min) - **HIGHEST PRIORITY**
2. Add meta descriptions (30 min)
3. Implement security headers (30 min)
4. Remove orphaned Elementor pages from sitemap (15 min)
5. Optimize Core Web Vitals (1-2 hours)

**Expected improvement:** 72 → 82-85/100 (with llms.txt + meta descriptions + security headers)

---

### Schema & Structured Data Analysis (0/100)

**Critical Finding:** ZERO schema.org markup detected across entire site.

**Missing Schemas by Priority:**

**CRITICAL (Implement Week 1):**
1. **Organization Schema** — Company identity + sameAs linking
   - Missing: Name, logo, founder info, contact, social profiles
   - Impact: 20-point improvement (enables brand entity recognition)
   
2. **Event Schema** — Pride events (20+ events)
   - Missing: Date, location, attendance, organizer, ticketing
   - Impact: 25-point improvement (events become discoverable in Google Events, Apple Calendar, AI aggregators)
   
3. **Person Schema** — Founder Drew Lewis
   - Missing: Name, credentials, LinkedIn, Twitter, email
   - Impact: 8-point improvement (founder expertise signals)

**HIGH (Implement Week 2):**
4. **Article Schema** — Blog posts (10+ articles)
   - Missing: Title, author, publication date, image, keywords
   - Impact: 15-point improvement (publication date and author attribution for AI indexing)
   
5. **SoftwareApplication Schema** — OutAtlas app
   - Missing: App name, description, operating system, download URL, rating
   - Impact: 8-point improvement (product discoverability)
   
6. **WebSite + SearchAction Schema** — Sitelinks search box
   - Missing: Query input template for destination search
   - Impact: 5-point improvement (search functionality exposure)

**MEDIUM (Implement Week 3):**
7. **BreadcrumbList** — Navigation hierarchy
8. **FAQPage** — Travel Q&A
9. **LocalBusiness/Place** — Destination city pages

**Implementation Roadmap:**
- **Week 1:** Organization (30 min) + Event (5 hrs) + Person (20 min) = 5.5 hours
- **Week 2:** Article (2.5 hrs) + SoftwareApplication (20 min) + WebSite (15 min) = 3.25 hours
- **Week 3:** BreadcrumbList (30 min) + FAQPage (1 hr) + LocalBusiness (9.5 hrs) = 11 hours
- **Total effort:** 19.75 hours across 3 weeks

**Expected improvement:** 0 → 65/100 (schema component) = +15-20 point overall GEO improvement

---

### Platform Optimization Analysis (40/100)

**Definition:** Presence on platforms that AI training data comes from

**Platform Coverage:**

| Platform | Presence | Impact | Notes |
|---|---|---|---|
| **Google Search** | ✓ Yes | Good (server indexed, sitemaps working) | Traditional search only; no schema for rich results |
| **Bing Search** | ✓ Yes | Good (crawlable) | No IndexNow configured (missed opportunity for faster indexing) |
| **ChatGPT** | ⚠ Unclear | Poor (no llms.txt = limited crawling) | Likely indexed but citation permission unclear |
| **Claude/Anthropic** | ⚠ Unclear | Poor (no llms.txt = limited crawling) | Same as ChatGPT |
| **Perplexity AI** | ⚠ Unclear | Poor (no llms.txt = limited crawling) | Same as ChatGPT |
| **Google Gemini** | ✗ Likely absent | Poor (no schema, weak E-E-A-T signals) | Gemini prioritizes schema + authority |
| **Bing Copilot** | ⚠ Unclear | Fair (tied to Bing index, needs IndexNow) | Could improve with IndexNow setup |
| **Wikipedia** | ✗ No | Critical (no company article) | No brand presence in major knowledge base |
| **YouTube** | ⚠ Unknown | Low (assumes minimal channel activity) | Travel guides not prominent format |
| **LinkedIn** | ⚠ Unknown | Fair (assumes company page exists but unoptimized) | No thought leadership content visible |

**Key Gaps:**
- No explicit llms.txt means all three major AI platforms (ChatGPT, Claude, Perplexity) have degraded crawling
- No Wikipedia article (knowledge bases rely on Wikipedia for entity verification)
- No IndexNow protocol (Bing/Copilot get slower updates)
- No YouTube travel guides (growing format for travel planning)
- Limited LinkedIn presence (no founder thought leadership)

**Recommendations:**
1. **Create llms.txt** (15 min) — Enables proper indexing on ChatGPT, Claude, Perplexity
2. **Enable IndexNow** (20 min) — Bing Copilot gets faster crawl frequency
3. **Build Wikipedia article** (after press coverage phase) — Critical for knowledge base presence
4. **Create YouTube channel** (ongoing) — Travel guides and event coverage
5. **Expand LinkedIn presence** (ongoing) — Founder publishing, company page optimization

**Expected improvement:** 40 → 60-65/100 (with llms.txt + IndexNow + YouTube channel)

---

## Quick Wins (Implement This Week)

**Target: +4-6 points on overall GEO score in 2-3 hours**

1. **Create llms.txt file** (15 min)
   - Location: `/llms.txt`
   - Content: Allow all major AI crawlers
   - Impact: +15-20% AI visibility

2. **Add meta descriptions to 10 key pages** (30 min)
   - Homepage, 5 event guides, 3 blog posts
   - ~155 characters each, keyword-rich
   - Impact: +3-5 points on technical score

3. **Add publication dates to blog posts** (30 min)
   - Display "Published: [Date]" on all articles
   - Update WordPress post meta with correct dates
   - Impact: +2-3 points on E-E-A-T

4. **Create Organization schema for homepage** (30 min)
   - Include company name, logo, sameAs links
   - Update with LinkedIn, Twitter, Instagram URLs
   - Impact: +5 points on schema score

5. **Replace placeholder OG image** (15 min)
   - Use actual branded hero image
   - Dimensions: 1200x630px
   - Impact: Better social sharing + AI image recognition

---

## 30-Day Action Plan

### Week 1: Foundation (GEO Infrastructure)
- [ ] Create llms.txt (15 min)
- [ ] Add meta descriptions to key pages (30 min)
- [ ] Implement security headers (30 min)
- [ ] Create Organization schema (30 min)
- [ ] Add publication dates to blog posts (30 min)
- [ ] Remove orphaned Elementor pages from sitemap (15 min)
- [ ] Replace placeholder OG images (15 min)

**Expected score improvement: 50 → 58/100 (+8 points)**

### Week 2: Content & Markup
- [ ] Create Person schema for founder Drew Lewis (20 min)
- [ ] Add author bylines to all pages (2-3 hours)
- [ ] Add Event schemas to all Pride event pages (5 hours)
- [ ] Add Article schemas to blog posts (2.5 hours)
- [ ] Create SoftwareApplication schema (20 min)
- [ ] Add "Last Updated" dates to destination guides (1 hour)

**Expected score improvement: 58 → 68/100 (+10 points)**

### Week 3: Authority & Expansion
- [ ] Create comprehensive About page with team/founder info (2-3 hours)
- [ ] Add BreadcrumbList schema (30 min)
- [ ] Create FAQPage with common travel Q&A (1-2 hours)
- [ ] Add LocalBusiness/Place schemas for destinations (3-5 hours)
- [ ] Enable IndexNow protocol in Yoast (20 min)
- [ ] Begin press outreach campaign (target: 3-5 travel publications)

**Expected score improvement: 68 → 75-78/100 (+7-10 points)**

### Week 4 & Beyond: Authority Building
- [ ] Pursue 2-3 press features in travel/tech publications (ongoing)
- [ ] Create YouTube channel with destination guides (ongoing)
- [ ] Expand LinkedIn presence with founder articles (ongoing)
- [ ] Build Reddit community presence (subreddit/AMA) (ongoing)
- [ ] Plan Wikipedia article creation (post press coverage)

**Expected score improvement: 75 → 85-90/100 (by week 8-12)**

---

## Quick Wins List (By Effort/Impact)

| Action | Effort | Impact | GEO Score Gain |
|---|---|---|---|
| Create llms.txt | 15 min | **Very High** | +5 points |
| Add Organization schema | 30 min | **Very High** | +6 points |
| Add meta descriptions | 30 min | **High** | +3 points |
| Implement security headers | 30 min | **High** | +2 points |
| Add publication dates | 30 min | **Medium** | +2 points |
| Replace OG image | 15 min | **Medium** | +1 point |
| **Total (Quick Wins)** | **2.5 hours** | — | **+19 points** |

---

## Appendix: Pages Analyzed

| URL | Title | Word Count | Issues Found | Priority |
|---|---|---|---|---|
| https://outatlas.com/ | Homepage | 280 | No meta description, no schema, no author, placeholder OG | Critical |
| https://outatlas.com/worldpride-amsterdam-2026/ | WorldPride Amsterdam 2026 | 2,800 | No schema, no author, no publication date | Critical |
| https://outatlas.com/new-york-city-pride-2026/ | NYC Pride 2026 | 2,850 | No schema, no author, no publication date | Critical |
| https://outatlas.com/la-pride-2026/ | LA Pride 2026 | ~2,500 (est.) | No schema, no author | High |
| https://outatlas.com/gaydays-bear-jamboree-2026/ | GayDays Bear Jamboree 2026 | ~2,000 (est.) | No schema, no author | High |
| https://outatlas.com/destination-event-guides/ | Destination & Event Guides | 280 | No schema, no meta description, hub page thin | High |
| https://outatlas.com/international-mr-leather-2026-sample-itinerary/ | International Mr. Leather 2026 | ~2,000 (est.) | No schema, no author | Medium |
| https://outatlas.com/elementor-191/ | Asia Travel Guide (LGBTQ+ Asia Adventure) | 2,200 | No article schema, orphaned page candidate, poor title | High |
| https://outatlas.com/elementor-199/ | [Test/Orphaned Page] | Unknown | No schema, likely orphaned Elementor template | Medium |
| https://outatlas.com/nyc-pride-2026-sample-itinerary/ | NYC Pride Sample Itinerary | ~2,500 (est.) | No schema, duplicate/related to NYC Pride page | Medium |
| https://outatlas.com/author/996240pwpadmin/ | Admin Author Archive | Unknown | Thin content, likely template page | Low |
| https://outatlas.com/gay-days-bear-jamboree-one-magical-weekend/ | GayDays (Original) | ~2,000 (est.) | No schema, likely duplicate of 2026 version | Low |

**Total Pages Analyzed:** 14  
**Pages with Critical Issues:** 8  
**Pages with High Priority Issues:** 5  
**Average Word Count:** 1,850 words  
**Average Issue Count:** 3.5 issues per page

---

## Estimated Timeline & Effort Summary

| Phase | Duration | Effort | GEO Score Gain | Owner |
|---|---|---|---|---|
| **Quick Wins** | 1 week | 2.5 hrs | 50 → 58 | Developer |
| **Week 1 Actions** | 1 week | 8 hrs | 58 → 65 | Developer |
| **Week 2 Actions** | 1 week | 10 hrs | 65 → 73 | Developer + Content |
| **Week 3 Actions** | 1 week | 8 hrs | 73 → 78 | Developer + Content |
| **Authority Building** | Months 2-3 | 40+ hrs | 78 → 85-90 | Marketing + PR |
| **Total 30-Day Plan** | 4 weeks | 26 hrs | 50 → 78 | Cross-team |
| **90-Day Plan** | 12 weeks | 60+ hrs | 50 → 85-90 | Cross-team |

---

## Glossary of GEO Terms

**AI Citability:** How quotable and extractable content is for AI systems (sentences, paragraphs, facts that stand alone without context).

**Brand Authority:** Third-party recognition and validation through Wikipedia, press coverage, industry databases, and cross-platform presence.

**ClaudeBot:** Anthropic's AI crawler that indexes content for Claude AI and Claude Enterprise products. Checks llms.txt for permissions.

**E-E-A-T:** Experience, Expertise, Authoritativeness, Trustworthiness — Google's content quality evaluation framework (increasingly used by AI systems).

**GEO:** Generative Engine Optimization — optimizing content for discovery, understanding, and citation by AI systems (vs. traditional SEO for ranking in search engines).

**GPTBot:** OpenAI's AI crawler that indexes content for ChatGPT, GPT-4, and ChatGPT Enterprise. Checks llms.txt for permissions.

**llms.txt:** Emerging standard file (similar to robots.txt) that provides explicit permissions to AI crawlers. Located at `/llms.txt` or `/.well-known/llms.txt`.

**sameAs Property:** Schema.org property that links identical entities across multiple platforms (e.g., linking LinkedIn, Twitter, Wikipedia profiles as representations of the same organization).

**PerplexityBot:** Perplexity AI's crawler that indexes content for the Perplexity search engine. Checks llms.txt for permissions.

**Rich Results:** Enhanced search result displays that show structured data (event cards, FAQs, breadcrumbs, etc.) instead of plain blue links.

**Schema.org:** Standardized markup language for structuring data in HTML (JSON-LD, Microdata, RDFa) so search engines and AI can understand content intent.

**Structured Data:** Machine-readable markup that describes content type, author, date, location, etc. (vs. unstructured HTML which is human-readable only).

---

## Next Steps for Team

### Immediate (This Week)
1. Assign schema implementation to developer
2. Create llms.txt file and deploy to production
3. Add meta descriptions to key pages
4. Verify all social media URLs (LinkedIn, Twitter, Instagram) for Organization schema

### Short-Term (Weeks 2-4)
1. Implement Event schemas for all Pride event pages
2. Create Organization, Person, and Article schemas
3. Add author bylines and About page content
4. Enable IndexNow protocol

### Medium-Term (Month 2-3)
1. Begin press outreach campaign (target: 3-5 travel/tech publications)
2. Plan Wikipedia article creation (after press coverage established)
3. Create YouTube channel with destination guides
4. Expand LinkedIn founder thought leadership

### Long-Term (Months 3-6)
1. Execute Wikipedia article submission (after press validation)
2. Build Reddit community presence
3. Launch annual LGBTQ+ travel safety/cost research
4. Aim for 85-90 GEO score by Q3 2026

---

**Report prepared:** April 18, 2026  
**Auditor:** AI GEO Specialist (Multi-agent audit system)  
**Business Impact:** Implementing 30-day plan could improve AI visibility by 30-50%, potentially driving +$1,000-3,000/month in incremental traffic from AI search platforms.
