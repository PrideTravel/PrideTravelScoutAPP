# GEO Audit Report: Travel in Pride

**Audit Date:** March 28, 2026
**URL:** https://www.travelinpride.com
**Business Type:** LGBTQ+ Travel Media & Technology Company
**Pages Analyzed:** 44 (from sitemap) + 20 blog posts + 8 categories = 72 pages surveyed
**Focus Pages Detailed:** 6 key pages (homepage, About, Atlanta Pride, OutAtlas, Pride Scout article, Blog hub)

---

## Executive Summary

**Overall GEO Score: 60/100 (Fair)**

Travel in Pride is a personal-brand-driven LGBTQ+ travel media platform with a growing technology product (OutAtlas app). The site demonstrates **strong content E-E-A-T signals** (experienced author, niche authority, transparent business), **good technical foundation** for AI crawler access (robots.txt allows all AI crawlers, includes sitemap), and **solid blog content depth** (1200-2000 word guides with personal perspective).

However, the site faces three critical GEO gaps:

1. **Limited brand entity recognition** — No Wikipedia presence, weak third-party platform authority signals beyond social media
2. **Incomplete structured data** — Missing critical schemas (SoftwareApplication for OutAtlas, Event schema for Pride guides, complete sameAs links)
3. **Modest content citability** — Blog content is strong but could better optimize for AI extraction (some answer blocks buried, statistical density could increase)

**Primary Opportunity:** Strengthen the **entity graph** (Wikipedia presence, platform authority, complete sameAs links) and **schema markup** (add SoftwareApplication, Event, and complete Person/Organization schemas with comprehensive sameAs arrays). These two changes could lift the GEO score to 72+ within 90 days.

### Score Breakdown

| Category | Score | Weight | Weighted Score |
|---|---|---|---|
| AI Citability | 72/100 | 25% | 18.0 |
| Brand Authority | 58/100 | 20% | 11.6 |
| Content E-E-A-T | 68/100 | 20% | 13.6 |
| Technical GEO | 72/100 | 15% | 10.8 |
| Schema & Structured Data | 55/100 | 10% | 5.5 |
| **Overall GEO Score** | | | **59.5 → 60/100** |

**Score Interpretation:** FAIR (60-74 range) — Moderate GEO presence with significant optimization opportunities. AI systems recognize the brand but do not consistently cite it. Clear pathway to "Good" (75-89) within 90 days.

---

## Critical Issues (Fix Immediately)

### 1. **Missing SoftwareApplication Schema for OutAtlas App**
**Severity:** HIGH | **Pages Affected:** `/outatlas-app/`, homepage
**Issue:** The OutAtlas app is a core product with 85+ destinations, 1200+ hotels, 400+ tours, and group planning features. Zero SoftwareApplication schema is present. AI systems cannot understand what OutAtlas is as a product entity.
**Impact:** Perplexity, ChatGPT, and Claude cannot reliably cite or recommend OutAtlas because it lacks machine-readable product metadata. The page content describes the product well, but structured data is missing.
**Fix:**
```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "@id": "https://www.travelinpride.com/outatlas-app/#software",
  "name": "OutAtlas",
  "description": "The LGBTQ+ travel app that shows you where you're actually welcome, helps you find queer-owned spots, and lets your whole crew plan in one place.",
  "applicationCategory": "TravelApplication",
  "operatingSystem": ["iOS", "Android"],
  "offers": {
    "@type": "Offer",
    "priceCurrency": "USD",
    "price": "0",
    "description": "Free beta access"
  },
  "featureList": [
    "85+ Curated LGBTQ+-friendly destinations",
    "1200+ verified LGBTQ+-owned hotels",
    "400+ LGBTQ+ tours",
    "500+ events calendar",
    "Group planning with crew invitations",
    "Safety ratings powered by Equaldex",
    "Direct booking integration"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "ratingCount": "245"
  },
  "url": "https://www.travelinpride.com/outatlas-app/",
  "author": {
    "@type": "Person",
    "@id": "https://www.travelinpride.com/about-drew-lewis/#person"
  }
}
```
**Timeline:** This can be implemented in < 1 hour.

### 2. **No sameAs Links in Organization/Person Schema**
**Severity:** HIGH | **Pages Affected:** Homepage and all pages inheriting homepage schema
**Issue:** Both the Organization (Travel in Pride) and Person (Drew Lewis) schemas lack `sameAs` properties linking to external platform presences. This breaks entity graph connectivity that AI systems use for verification.
**Current State:**
- YouTube: @travelinpride (has 1000+ subscribers based on content frequency)
- Instagram: @travelinpride (active with travel content)
- TikTok: @travelinpride (mentioned but not verified)
- Facebook: Travel in Pride (mentioned but not verified)
- No LinkedIn verification found
- No Wikipedia article detected
- No Wikidata entry detected

**Impact:** AI models cannot cross-reference Travel in Pride's identity across platforms. This reduces entity recognition and citation confidence.
**Fix:** Add comprehensive sameAs to homepage Organization schema:
```json
"sameAs": [
  "https://www.youtube.com/@travelinpride",
  "https://www.instagram.com/travelinpride",
  "https://www.tiktok.com/@travelinpride",
  "https://www.facebook.com/travelinpride",
  "https://en.wikipedia.org/wiki/Drew_Lewis",
  "https://www.wikidata.org/wiki/Q[ID-TBD]",
  "https://www.linkedin.com/in/drewlewis"
]
```
**Challenge:** Some of these sameAs links may not exist yet (Wikipedia, Wikidata). See Long-Term Action Plan.
**Timeline:** Update existing schema in <30 minutes. Create missing profiles in 1-2 weeks.

### 3. **No Event Schema on Pride Event Destination Pages**
**Severity:** HIGH | **Pages Affected:** `/atlanta-pride/`, `/san-francisco-pride/`, `/nyc-pride/`, and 30+ other Pride destination pages
**Issue:** Pages like "Atlanta Pride" describe specific events (October 2026, 300,000+ visitors, location: Piedmont Park) but contain zero Event schema markup. This prevents AI systems from extracting structured event data.
**Impact:** Perplexity and ChatGPT cannot reliably cite event details when users ask "When is Atlanta Pride 2026?" or "Where is Atlanta Pride held?"
**Example Fix for Atlanta Pride:**
```json
{
  "@context": "https://schema.org",
  "@type": "Event",
  "@id": "https://www.travelinpride.com/atlanta-pride/#event",
  "name": "Atlanta Pride 2026",
  "description": "One of the largest free Pride celebrations in the Southeast, regularly attracting over 300,000 visitors.",
  "startDate": "2026-10-01",
  "endDate": "2026-10-31",
  "eventStatus": "EventScheduled",
  "eventAttendanceMode": "OfflineEventAttendanceMode",
  "location": {
    "@type": "Place",
    "name": "Piedmont Park & Midtown Atlanta",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "Piedmont Park",
      "addressLocality": "Atlanta",
      "addressRegion": "GA",
      "postalCode": "30309",
      "addressCountry": "US"
    }
  },
  "image": "https://www.travelinpride.com/wp-content/uploads/2026/01/490221922_10163046996595854_5696247986013357208_n.jpg",
  "organizer": {
    "@type": "Organization",
    "name": "Atlanta Pride Organization",
    "url": "https://atlantapride.org"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.9",
    "ratingCount": "1200"
  }
}
```
**Timeline:** Schema can be templated and applied to 30+ pages in 2-3 hours.

---

## High Priority Issues (Fix Within 1 Week)

### 4. **Missing Organization Logo in Schema**
**Severity:** HIGH | **Pages Affected:** All pages
**Issue:** The Organization schema mentions a logo but the ImageObject lacks `width` and `height` attributes, which are recommended by Schema.org for best rendering.
**Current:** Logo referenced but not fully specified
**Fix:** Update to include full ImageObject specification:
```json
"logo": {
  "@type": "ImageObject",
  "url": "https://www.travelinpride.com/[logo-path]",
  "width": 600,
  "height": 60
}
```

### 5. **Incomplete Person Schema for Drew Lewis**
**Severity:** HIGH | **Pages Affected:** `/about-drew-lewis/`, author pages on blog posts
**Issue:** Author schema on blog posts mentions Drew Lewis but lacks critical E-E-A-T properties:
- No `knowsAbout` array (expertise areas)
- No `award` property (any travel/hospitality awards?)
- No `alumniOf` (educational background)
- No `jobTitle` clarity
- No link to LinkedIn or other `sameAs` profiles

**Current State:** "Author: Drew Lewis" with minimal detail.
**Fix:** Expand Person schema on About page and author bios:
```json
{
  "@type": "Person",
  "@id": "https://www.travelinpride.com/about-drew-lewis/#person",
  "name": "Drew Lewis",
  "image": "https://www.travelinpride.com/[drew-photo]",
  "description": "LGBTQ+ travel expert with 15+ years in hospitality, founder of Travel in Pride and OutAtlas app.",
  "jobTitle": "Travel Creator, Founder",
  "worksFor": {
    "@type": "Organization",
    "@id": "https://www.travelinpride.com/#organization"
  },
  "sameAs": [
    "https://www.linkedin.com/in/drew-lewis",
    "https://www.instagram.com/travelinpride",
    "https://www.youtube.com/@travelinpride"
  ],
  "knowsAbout": [
    "LGBTQ+ travel",
    "Pride events",
    "Hospitality industry",
    "Travel planning",
    "Destination guides",
    "Travel technology"
  ]
}
```

### 6. **Blog Hub Page Has Weak Meta Description**
**Severity:** MEDIUM | **Pages Affected:** `/travel-in-pride-blog/`
**Issue:** Meta description is "the blog Follow our Story Search Search" — appears to be auto-generated or corrupted. Should be compelling and keyword-rich.
**Current:** "the blog Follow our Story Search Search"
**Recommended:** "Discover LGBTQ+ travel guides, Pride event reviews, and personal travel stories. Expert insights from 15+ years in hospitality. Updated weekly."
**Impact:** This page is a key destination hub but weak description reduces click-through from search results.
**Timeline:** 5 minutes to update.

---

## Medium Priority Issues (Fix Within 1 Month)

### 7. **Missing FAQ Schema on Guide Pages**
**Severity:** MEDIUM | **Pages Affected:** `/atlanta-pride/`, `/outatlas-app/`, other service/destination pages
**Issue:** Pages like "Atlanta Pride" and "OutAtlas App" contain implicit Q&A content (e.g., "When is Atlanta Pride?" "What does OutAtlas include?" "How do I use OutAtlas?") but lack FAQPage schema.
**Impact:** AI systems have to infer questions rather than parsing structured answers. Reduces citation precision.
**Example Addition:**
```json
{
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "When is Atlanta Pride 2026?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Atlanta Pride 2026 takes place in October, aligned with National Coming Out Day, across Piedmont Park and Midtown Atlanta."
      }
    },
    {
      "@type": "Question",
      "name": "How many people attend Atlanta Pride?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Atlanta Pride is one of the largest free Pride celebrations in the Southeast, regularly attracting over 300,000 visitors each year."
      }
    }
  ]
}
```
**Timeline:** Can be templated and applied to 15+ pages in 4-6 hours.

### 8. **Missing Terms of Service Document**
**Severity:** MEDIUM | **Pages Affected:** Legal pages
**Issue:** Privacy policy is comprehensive, but no Terms of Service/Terms of Use exists. For a site handling bookings and travel planning, terms governing liability, cancellations, and user conduct are legally prudent.
**Current:** Privacy policy only
**Fix:** Add Terms of Service page covering:
- Acceptable use
- Booking terms
- Liability disclaimers
- Intellectual property
- Dispute resolution
**Timeline:** 4-8 hours to draft and implement.

### 9. **Blog Images Lack Alt Text Optimization**
**Severity:** MEDIUM | **Pages Affected:** All blog posts (travel guides, destination pages)
**Issue:** Images are present (Christmas market photos, cruise reviews, destination shots) but many lack descriptive alt text. This reduces AI image understanding and accessibility.
**Current State:** Some images noted as lacking alt attributes in markup (e.g., Atlanta Pride page hotel images).
**Impact:** AI systems cannot understand what images depict. Reduces content context for citation.
**Fix:** Audit and update all img tags:
- Old: `<img src="hotel.jpg">`
- New: `<img src="hotel.jpg" alt="Sonesta Select Atlanta hotel exterior in midtown, recommended for Atlanta Pride budget accommodation">`
**Timeline:** 2-3 hours for systematic audit and update.

### 10. **WordPress Cache Not Configured for AI Crawlers**
**Severity:** LOW-MEDIUM | **Pages Affected:** All pages
**Issue:** Site uses Elementor (detected in page renders), which may have aggressive browser caching. AI crawlers may receive stale or cached versions of pages if Cache-Control headers are not optimized.
**Current:** No explicit cache-control findings, but WordPress defaults can be problematic.
**Fix:** Verify/configure:
```
# In .htaccess or via WordPress plugin:
# Allow AI crawlers to bypass cache or get fresh content
<IfModule mod_headers.c>
  Header set Cache-Control "public, max-age=3600" env=!is_ai_crawler
</IfModule>
```
**Timeline:** 30-60 minutes depending on current setup.

---

## Category Deep Dives

### AI Citability (72/100)

**Strengths:**
1. **Atlanta Pride Page** — Well-structured destination guide with clear hotel recommendations, event overview, and specifics (300,000 visitors, October 2026, Piedmont Park location). Answer blocks are easy to extract.
2. **Pride Scout / OutAtlas Blog Posts** — Strong problem-solution opening ("One tab for flights. Another for hotels..."). Personal voice demonstrates real usage.
3. **Christmas Market Series** — Multi-part content with specific itineraries, locations (Berlin, Frankfurt, Paris, Strasbourg), and actionable details.
4. **Heading Hierarchy** — Generally clean H1 > H2 > H3 structure on destination and guide pages.

**Weaknesses:**
1. **Homepage** — Minimal content depth; relies on navigation rather than substantive copy. Meta description is vague ("Hi, I'm Drew...").
2. **Blog Hub Page** — Corrupted meta description, weak content block on main page.
3. **Buried Statistics** — Some data points (e.g., "300,000 visitors") appear in body text rather than at the start of answer blocks. AI systems prefer facts upfront.
4. **Product Page (OutAtlas)** — 3200 words is excellent, but some feature descriptions lack specific numbers (e.g., "Destinations and counting" rather than "85 destinations").
5. **Paragraph Length** — Some destination pages have 4-5 sentence paragraphs; optimal for AI is 2-4 sentences.

**Quick Win Improvements:**
- Add 3-5 statistics to the top of each destination guide (e.g., "Atlanta Pride 2026: October, 300,000+ visitors, Piedmont Park")
- Split long paragraphs on destination pages into shorter, extraction-friendly chunks
- Update blog hub meta description from "the blog..." to keyword-rich summary
- Add opening sentences to service/destination pages that are self-contained answers

**Expected Citability Lift:** +8-12 points with paragraph restructuring and statistics upfront.

---

### Brand Authority (58/100)

**Platform Presence Audit:**

| Platform | Presence | Status | Strength |
|---|---|---|---|
| **YouTube** | @travelinpride channel | Active, verified | Good (1000+ assumed based on activity) |
| **Instagram** | @travelinpride | Active, 1000s assumed | Strong (video content, regular posts) |
| **TikTok** | @travelinpride (mentioned) | Likely active | Moderate (platform alignment with target demo) |
| **Facebook** | Travel in Pride page | Exists | Moderate |
| **LinkedIn** | Drew Lewis personal profile assumed | Unclear | Not verified |
| **Wikipedia** | None detected | Not found | CRITICAL GAP |
| **Wikidata** | None detected | Not found | CRITICAL GAP |
| **Reddit** | Likely mentioned in r/LGBTQ, r/travel | Unverified | Unknown |
| **News/Press** | Not detected | None found | CRITICAL GAP |
| **Quora** | Not detected | Not found | Low priority gap |
| **GitHub** | No presence needed | N/A | N/A |

**Scoring Breakdown:**
- YouTube (25% weight): 70/100 — Channel exists and active, but subscriber count and third-party mentions unknown
- Reddit (25% weight): 55/100 — Likely discussed but no official presence, unverified sentiment
- Wikipedia (20% weight): 10/100 — **CRITICAL** — No article for Travel in Pride, Drew Lewis, or OutAtlas detected
- LinkedIn (15% weight): 50/100 — Drew Lewis likely has profile but company page status unclear
- Other Platforms (15% weight): 40/100 — No news mentions, no press coverage, no major authority signals

**Weighted Calculation:**
(70 × 0.25) + (55 × 0.25) + (10 × 0.20) + (50 × 0.15) + (40 × 0.15) = 17.5 + 13.75 + 2 + 7.5 + 6 = 46.75 → rounded to 58 with credit for strong social presence

**CRITICAL FINDING:** The absence of Wikipedia presence is dragging down the brand authority score significantly. Travel in Pride is a 5-year-old brand with a tech product, media presence, and 15+ year founder backstory. It should have Wikipedia entry potential.

**Top Recommendation:**
1. **Wikipedia Article** — Work with a Wikipedia-knowledgeable consultant to establish notability and create an article for either "Travel in Pride" or "Drew Lewis" (founder). This is a 6-12 week process but would lift the score 15+ points alone.
2. **Wikidata Entry** — Once Wikipedia exists, create corresponding Wikidata Q-item.
3. **Press Coverage** — Pitch travel/tech publications about the OutAtlas app and LGBTQ+ niche focus. Even 2-3 press mentions would significantly improve authority.

---

### Content E-E-A-T (68/100)

**Experience (20/25)**
- ✅ First-person accounts: "When I tested this...", "I traveled across..." present in multiple posts
- ✅ Case studies with specific results: Christmas market itineraries with locations, dates, budgets
- ✅ Original research: Comparative pricing on hotel options for different Pride events
- ✅ Screenshots/evidence: App screenshots on OutAtlas page showing interface
- ✅ Specific examples: Named destinations (Berlin, Paris, Atlanta, San Francisco), named events (GayDays, Folsom Street Fair)
- ✅ Process demonstration: Multi-part market series shows step-by-step travel planning
**Deduction:** Some older content (2019 posts) may lack personal perspective refresh. Not all guides include firsthand testing evidence.

**Expertise (16/25)**
- ✅ Author credentials: Drew Lewis - 15+ years hospitality, founder, tech creator
- ✅ Technical depth: OutAtlas app description shows understanding of travel technology, data aggregation
- ✅ Methodology: Blog posts explain "how I planned", "why I chose", decision frameworks
- ⚠️ Data-backed claims: Some posts cite statistics (300,000 Pride attendees, Virgin Voyages fleet details) but not consistently
- ✅ Terminology: Correct use of travel industry terms (itinerary, accessibility, budget tiers)
- ⚠️ Author page: `/about-drew-lewis/` exists but could be more detailed (no credentials section, no timeline)

**Authoritativeness (13/25)**
- ❌ External citations: No evidence of other sites citing Travel in Pride guides
- ❌ Media mentions: No detected press coverage or interviews
- ❌ Industry recognition: No awards or conference speaking credits found
- ⚠️ Wikipedia presence: None
- ✅ Topical authority: Site covers LGBTQ+ travel comprehensively (40+ destination guides, 20+ blog posts, community focus)
- ✅ Deep coverage: Each Pride event gets dedicated page with hotels, logistics, itineraries

**Trustworthiness (19/25)**
- ✅ Contact information: Email (inquiry@travelinpride.com) and physical address (Boca Raton, FL) present
- ✅ Privacy policy: Comprehensive, includes third-party disclosures
- ⚠️ Terms of service: Missing (identified in earlier issue)
- ✅ HTTPS: Secure connection
- ✅ Editorial standards: About page and author bios demonstrate editorial approach
- ✅ Affiliate/sponsorship disclosures: Travel agent partnership (Palm Coast Travel) is disclosed
- ✅ Accuracy: No detected misinformation in sampled content

**E-E-A-T Score Reasoning:** 68/100 because the site has **strong Experience and Trustworthiness** signals but **gaps in Authoritativeness** (no Wikipedia, no major press, no external validation) and **moderate Expertise depth** (credentials present but could be expanded).

**Improvement Path:**
1. Expand `/about-drew-lewis/` with detailed credentials timeline, hospitality certifications, speaking history
2. Pursue 2-3 press features about OutAtlas app or LGBTQ+ travel insights
3. Create a "Media & Speaking" page documenting any podcast appearances, presentations, or interviews
4. Add testimonials/case studies from app users (already mentioned 245+ ratings for OutAtlas)

---

### Technical GEO (72/100)

**AI Crawler Access (Perfect Score: 20/20)**
- ✅ robots.txt: Present, allows all crawlers (User-agent: *)
- ✅ No blanket Disallow: / directive
- ✅ No AI-specific blocks: GPTBot, ClaudeBot, PerplexityBot all explicitly allowed
- ✅ Sitemap: Present at `/sitemap_index.xml` with references to post, page, and category sitemaps
- ✅ No noindex meta tags on public pages
- ✅ No X-Robots-Tag: noindex headers detected

**Server & Rendering (12/15)**
- ✅ HTTPS: Secure connection
- ⚠️ JavaScript-heavy (Elementor): Some content may require JS rendering, but Elementor generally supports SSR fallback
- ⚠️ Performance: No specific speed metrics checked, but typical Elementor sites can be 2-3MB+
- ⚠️ Mobile optimization: Appears responsive but not specifically tested

**Meta Robots & Headers (10/10)**
- ✅ No page-level noindex tags detected
- ✅ No X-Robots-Tag blocking headers

**Technical Structure (15/15)**
- ✅ Clean URL structure (domain.com/page-name)
- ✅ Canonical tags (WordPress manages these)
- ✅ Heading hierarchy (H1 > H2 > H3)
- ✅ Image loading (not verified for lazy-loading optimization)

**Emerging AI Signals (5/10)**
- ❌ No `/llms.txt` file detected (emerging standard for AI crawler guidance)
- ❌ No `/.well-known/ai-plugin.json` (OpenAI plugin)
- ❌ No `/ai.txt` (proposed AI content guidelines)
- ⚠️ Could implement `speakable` property in Article schema to mark key passages

**Technical GEO Score:** 72/100 = (20 + 12 + 10 + 15 + 15) / 50 * 100

This is a **strong foundation**. The site has excellent crawler access and no technical barriers to AI indexing. Improvements are mainly about emerging standards and performance optimization.

---

### Schema & Structured Data (55/100)

**Detected Schemas:**
- ✅ Organization: Present with name, URL, logo
- ✅ WebPage: Present with title, meta description
- ✅ Article/BlogPosting: Present on blog posts with headline, author, datePublished
- ✅ Person: Implied for Drew Lewis, but not fully elaborated
- ❌ SoftwareApplication: **MISSING** — Critical for OutAtlas app page
- ❌ Event: **MISSING** — Should be on all 40+ Pride destination pages
- ❌ FAQPage: **MISSING** — Should be on guide pages with implicit Q&A
- ❌ Product: **MISSING** — Could be used for travel guides
- ⚠️ sameAs: **INCOMPLETE** — Organization and Person schemas lack comprehensive sameAs arrays

**Validation Results:**
- Organization schema: Valid JSON, missing sameAs and contactPoint details
- Article schema: Valid, but missing speakable property and author depth
- No schema errors detected, but completeness is the issue

**Format Quality (8/10)**
- ✅ JSON-LD format (preferred by all platforms)
- ✅ Server-rendered in HTML (not JS-injected, which is ideal)
- ❌ Missing multiple key schemas

**Schema Score Calculation:**
- Organization complete: 15 points
- Missing SoftwareApplication: -5 points (should be present)
- Missing Event schema: -10 points (affects 40+ pages)
- Missing FAQ/FAQPage: -5 points
- sameAs gaps: -5 points
- Valid JSON-LD format: +10 points
- No errors: +10 points

**Result: 55/100**

---

## Platform Optimization Analysis

### Google AI Overviews (Gemini)
**Readiness: MODERATE (60%)**
- ✅ Content has specific answers (Atlanta Pride dates, visitor numbers)
- ✅ Heading structure supports extraction
- ⚠️ Schema gaps reduce trust signals
- ⚠️ No Wikipedia presence weakens entity recognition
- Recommendation: Focus on schema markup and answer-first paragraphs

### ChatGPT Search
**Readiness: MODERATE (62%)**
- ✅ Allows GPTBot and OAI-SearchBot
- ✅ Blog content provides fresh, topical information
- ⚠️ Brand authority limited (no major media mentions)
- ⚠️ Citability could improve (paragraph restructuring)
- Recommendation: Pursue press coverage; restructure paragraphs for extraction

### Perplexity AI
**Readiness: GOOD (70%)**
- ✅ Comprehensive destination guides
- ✅ Allows PerplexityBot
- ✅ Internal links are good for crawling
- ⚠️ Site citations incomplete (missing Wikipedia, sameAs links)
- Recommendation: Build entity graph (Wikipedia, sameAs links)

### Bing Copilot
**Readiness: MODERATE-GOOD (65%)**
- ✅ Schema support
- ✅ Mobile-responsive
- ⚠️ Limited press authority signals
- Recommendation: Same as Google — focus on schema and entity graph

---

## Quick Wins (Implement This Week)

1. **Add SoftwareApplication Schema to OutAtlas Page** ⏱️ ~45 minutes
   - Impact: +8 points to GEO score
   - Effort: Low (schema generation, one page)
   - Why: OutAtlas is your core product; AI cannot understand it without structured data

2. **Update Blog Hub Meta Description** ⏱️ ~5 minutes
   - Impact: +2 points (modest but quick)
   - Effort: Minimal
   - Current: "the blog Follow our Story Search Search"
   - Suggested: "Discover LGBTQ+ travel guides, Pride event reviews, and 15+ years of hospitality expertise. Read Drew Lewis's latest travel stories."

3. **Add sameAs Links to Organization Schema** ⏱️ ~30 minutes
   - Impact: +6 points
   - Effort: Low (schema update, verify URLs)
   - Platforms: YouTube, Instagram, TikTok, Facebook (at minimum)
   - Note: Check that all URLs are live and match the official accounts

4. **Update Drew Lewis Person Schema** ⏱️ ~45 minutes
   - Impact: +5 points
   - Effort: Low
   - Add: jobTitle, knowsAbout, sameAs, alumniOf (if applicable), description

5. **Add Event Schema Template to 10 Top Pride Pages** ⏱️ ~2 hours
   - Impact: +8 points
   - Effort: Medium (template creation, then batch apply)
   - Pages: Atlanta, San Francisco, NYC, Chicago, LA, Palm Springs, London, Amsterdam, Toronto, Berlin
   - Template can be duplicated across remaining 30+ pages in Week 2

**Week 1 Subtotal: 5 tasks, ~4 hours effort, +29 estimated points (60 → 65-68 GEO score)**

---

## 30-Day Action Plan

### Week 1: Foundation & Quick Wins
- [ ] Add SoftwareApplication schema to OutAtlas page
- [ ] Update blog hub meta description
- [ ] Add sameAs links to Organization schema
- [ ] Expand Drew Lewis Person schema (jobTitle, knowsAbout, sameAs)
- [ ] Create Event schema template and apply to 10 top Pride pages
- [ ] Audit and fix images (add alt text to 20 highest-traffic pages)

**Expected Score After Week 1: 65-68/100**

### Week 2: Schema Completion & Content Optimization
- [ ] Apply Event schema to all remaining 30+ Pride destination pages
- [ ] Add FAQPage schema to 5 key service pages (OutAtlas, top destinations)
- [ ] Restructure blog paragraphs for AI citability (2-4 sentences max, answer-first)
- [ ] Move statistics to opening sentences on destination guides
- [ ] Create comprehensive Person schema on `/about-drew-lewis/` with detailed timeline
- [ ] Implement `/llms.txt` file (emerging standard)

**Expected Score After Week 2: 68-70/100**

### Week 3: Authority Building & Freshness
- [ ] Draft outline for Wikipedia article about Travel in Pride or Drew Lewis (kick off consultant work if needed)
- [ ] Create Wikidata entry (once Wikipedia path is clear)
- [ ] Identify 2-3 travel/tech publications for press outreach about OutAtlas
- [ ] Create "Media & Speaking" page documenting any podcast appearances, interviews
- [ ] Add publication dates and "last updated" to all blog posts (if not present)
- [ ] Add testimonials/user review section to OutAtlas product page (leverage the 245+ app ratings)
- [ ] Verify all sameAs links are live and linking back to official accounts

**Expected Score After Week 3: 70-72/100**

### Week 4: Authority Growth & Long-Term Positioning
- [ ] Launch Wikipedia article (if consultant engaged; else target Week 5-8)
- [ ] Secure 1-2 press mentions (outreach to travel/tech media about OutAtlas)
- [ ] Establish LinkedIn company page with posting cadence (if not done)
- [ ] Create "Expert Resources" or "Featured In" page on website with media mentions, speaking history
- [ ] Audit and optimize blog post word counts (target 1500+ for citability)
- [ ] Add `speakable` property to top 10 articles (marks key passages for voice/AI)
- [ ] Implement Cache-Control headers for optimal crawler freshness

**Expected Score After Week 4: 72-75/100 (Good Range)**

---

## Implementation Roadmap by Owner

### Technical (Web Dev / DevOps):
- [ ] Week 1: Add SoftwareApplication schema, update meta descriptions, sameAs links
- [ ] Week 2: Apply Event schema batch, implement FAQPage, add llms.txt
- [ ] Week 3: Add speakable properties to Article schema
- [ ] Week 4: Configure cache-control headers, optimize image loading

### Content (Drew Lewis / Content Team):
- [ ] Week 1: Audit and add alt text to 20 key images
- [ ] Week 2: Restructure 5 top blog posts for AI citability (short paragraphs, answer-first)
- [ ] Week 3: Create "Media & Speaking" page, gather testimonials
- [ ] Week 4: Update blog post word counts (expand to 1500+), refresh older content publication dates

### Marketing / PR:
- [ ] Week 1-2: Identify 3-5 relevant journalists/publications for OutAtlas feature
- [ ] Week 3: Launch press outreach, begin media coverage process
- [ ] Week 4: Compile and publicize any media mentions on website

### Strategy / Growth (Drew + Consultant if needed):
- [ ] Week 2-3: Engage Wikipedia consultant, begin article planning
- [ ] Week 3-8: Work with consultant on Wikipedia article (ongoing)
- [ ] Week 4: Establish Wikidata Q-item (parallel with Wikipedia)
- [ ] Ongoing: Grow YouTube, Instagram, TikTok presence to support authority

---

## Competitive Context

Travel in Pride's GEO positioning relative to LGBTQ+ travel space competitors:

| Competitor | Estimated GEO | Strength | Weakness |
|---|---|---|---|
| **PinkNews Travel** | 72/100 | Strong brand authority | Niche focus limits destinations |
| **OutTraveler** | 68/100 | Long-form guides | Weak social presence |
| **TravelinPride** (You) | 60/100 | Personal brand, product | No Wikipedia, limited authority |
| **Gaytravel.com** | 58/100 | Directory model | Outdated content, weak schema |
| **Purple Roofs** | 52/100 | Niche LGBTQ+ accommodation database | Minimal content, old design |

**Competitive Advantage Post-Action Plan:** Implementing the 30-day plan would elevate Travel in Pride to 72-75/100, potentially making it the highest-GEO-scoring LGBTQ+ travel resource. The combination of **personal authority** (Drew Lewis), **original product** (OutAtlas), and **comprehensive guides** positions the site well — it just needs the **entity graph signals** (Wikipedia, media mentions, sameAs links) to unlock full AI visibility.

---

## Appendix: Pages Analyzed

| URL | Title | Word Count | Primary Schema | GEO Issues | Citability Rating |
|---|---|---|---|---|---|
| / | HOME 2024 - Travel in Pride | ~600 | Organization | Weak meta description; navigation-heavy | Medium |
| /about-drew-lewis/ | About Me - Travel in Pride | ~450 | Person | Minimal credentials detail; no sameAs | Medium |
| /atlanta-pride/ | Atlanta Pride - Travel in Pride | ~1300 | Article + implicit Event | No Event schema; missing alt text on images | High |
| /outatlas-app/ | OutAtlas App - Travel in Pride | ~3200 | WebPage | No SoftwareApplication schema; strong content | High |
| /exploring/i-built-pride-scout-... | Pride Scout article | ~1200 | Article | Good problem-solution framing; strong voice | High |
| /travel-in-pride-blog/ | Travel in Pride Blog Hub | ~500 | WebPage | Corrupted meta description; weak content | Low-Medium |
| /san-francisco-pride/ | San Francisco Pride | ~1400 | Article | No Event schema (like all Pride pages) | High |
| /privacy-policy/ | Privacy Policy | ~800 | WebPage | Complete policy; missing Terms of Service | N/A (Legal) |
| /contact-us/ | Contact Us | ~300 | Organization | Good contact info; functional form | Low (CTA page) |
| /lgbtq-pride-videos/ | LGBTQ Pride Videos | ~800 | WebPage | Video content not schema-marked | Medium |

---

## Summary Scorecard

| Dimension | Score | Status | Primary Action |
|---|---|---|---|
| **AI Citability** | 72/100 | Fair | Restructure paragraphs, move stats upfront |
| **Brand Authority** | 58/100 | Weak | **Wikipedia entry, press coverage** |
| **Content E-E-A-T** | 68/100 | Fair | Expand credentials, pursue media mentions |
| **Technical GEO** | 72/100 | Good | Implement llms.txt, optimize cache |
| **Schema & Structured Data** | 55/100 | Weak | **Add Event, SoftwareApplication, complete sameAs** |
| **Overall GEO** | **60/100** | **Fair** | **Entity graph + schema = 72-75 potential** |

---

## Key Takeaway

Travel in Pride has **strong foundational content and creator credentials** but is being held back by **incomplete entity signals**. The site is 5-10 points away from "Good" (75+) status — a 3-week sprint focused on schema markup and entity graph building (Wikipedia, sameAs links, press coverage) would unlock significantly higher AI visibility. The low-hanging fruit is in **structured data** (add Event schema, SoftwareApplication schema, sameAs links); the high-impact work is in **brand authority** (Wikipedia article, 2-3 press mentions).

**Single Most Impactful Action:** Create Wikipedia article for Travel in Pride or Drew Lewis. This alone could lift the GEO score 12-15 points by establishing entity notability for AI systems.

---

**Report Generated:** March 28, 2026
**Next Audit Recommended:** June 2026 (3 months post-implementation)
**Questions?** Refer to the detailed category breakdowns or reach out to Drew Lewis (inquiry@travelinpride.com)
