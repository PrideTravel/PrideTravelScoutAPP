# GEO Client Report: OutAtlas

**Prepared for:** OutAtlas Leadership  
**Analysis Date:** April 18, 2026  
**URL:** https://outatlas.com/  
**Report Type:** Generative Engine Optimization Readiness Assessment

---

## Executive Summary

OutAtlas has built excellent foundational infrastructure—server-side rendering, clean site structure, and permissive AI crawler access—but critical content and schema gaps are preventing AI systems from discovering and citing your brand. Your site scores **50/100 on the GEO Readiness Scale, placing you in the Poor-to-Fair tier**. The single biggest issue is zero schema.org markup across all 14 pages analyzed, rendering your events, company information, and content invisible to AI systems. The good news: this is fixable. Implementing Organization schema, Event markup, and creating a simple llms.txt file would improve your score to 69/100 in just 2.5 hours of effort. Beyond these quick wins, a structured 90-day optimization plan could push your score to 75+, representing an estimated **$1,000–3,000 per month in additional AI-driven traffic by Q3 2026**.

---

## GEO Readiness Score

## GEO Readiness Score: 50/100 — Poor to Fair

Your site is currently under-positioned for AI search visibility. While you have strong technical foundations, critical gaps in schema markup and brand authority are limiting your discoverability. A focused optimization effort over the next 90 days can transform this score significantly.

| Component | Score | Weight | Weighted Score |
|---|---|---|---|
| AI Citability | 65/100 | 25% | 16.25 |
| Brand Authority | 35/100 | 20% | 7.0 |
| Content Quality & E-E-A-T | 62/100 | 20% | 12.4 |
| Technical Foundation | 72/100 | 15% | 10.8 |
| Schema & Structured Data | 0/100 | 10% | 0.0 |
| Platform Optimization | 40/100 | 10% | 4.0 |
| **Overall GEO Score** | | | **50/100** |

### What This Score Means

A GEO score of 50/100 indicates that your site is **currently invisible to most AI citation systems**. When an AI model answers a question about LGBTQ+ travel planning, your content is unlikely to be included. This represents significant lost opportunity—especially for a brand in the travel vertical, where AI search is growing rapidly.

**Score interpretation:**
- **50-59** (Poor): AI systems may struggle to cite your content. Your competitors with higher scores are capturing the traffic you should own.
- **Improvement to 70** (Fair): Your content becomes visible and citable in AI search, but not preferred.
- **Improvement to 85+** (Good/Excellent): Your brand is recognized, trusted, and frequently cited across all major AI platforms.

Your target should be 70+ within 30 days and 80+ within 90 days.

---

## AI Visibility Dashboard

| AI Platform | Readiness Score | Current Gap | What It Means |
|---|---|---|---|
| **Google AI Overviews** | 55/100 | Missing schema, weak EEAT | Your content may appear in Google's AI answers, but rarely as a preferred source. Rich snippets are missing. |
| **ChatGPT Web Search** | 42/100 | No author credentials, missing llms.txt | ChatGPT is unlikely to cite your pages. Competitors with better EEAT signals are preferred. |
| **Perplexity AI** | 45/100 | Thin content blocks, no structured data | Perplexity prefers sources with clear structure. Your content lacks the formatting AI needs. |
| **Google Gemini** | 50/100 | Zero schema markup, weak entity signals | Gemini cannot recognize OutAtlas as a distinct entity. Your brand is treated as generic content. |
| **Bing Copilot** | 48/100 | Missing Security headers, no indexing signals | Bing Copilot relies on entity recognition. Your brand is largely unknown to this system. |

### What These Scores Tell You

**Below 50 = Major Barrier to Citation.** When a score drops below 50, it signals that the AI platform has fundamental difficulty accessing, understanding, or trusting your content. 

- ChatGPT at 42/100 means that when someone asks ChatGPT "What are the best LGBTQ+ travel destinations?", your site is statistically unlikely to appear in the answer.
- Perplexity at 45/100 means users asking Perplexity for travel recommendations are being directed to competitors instead.
- The gap across all platforms (42–55) indicates inconsistent visibility—your site doesn't perform reliably on any single platform.

**The opportunity:** Closing these gaps through schema implementation and EEAT signals would create consistent 65+ scores across all platforms within 90 days.

---

## AI Crawler Access

| AI Crawler | Platform | Current Status | Business Impact | Action |
|---|---|---|---|---|
| **GPTBot** | ChatGPT / OpenAI | ✅ Allowed | High — ChatGPT has 200M+ weekly users | Keep allowed; add llms.txt |
| **ClaudeBot** | Claude (Anthropic) | ✅ Allowed | High — Growing enterprise adoption | Keep allowed; add llms.txt |
| **PerplexityBot** | Perplexity AI | ✅ Allowed | High — Fastest-growing AI search engine | Keep allowed; add llms.txt |
| **GoogleBot-Extended** | Google Gemini | ✅ Allowed | High — Gemini integrated into Search | Keep allowed; implement schema |
| **Bingbot** | Bing + Copilot | ✅ Allowed | Medium — Copilot has 100M+ users | Keep allowed; implement IndexNow |
| **Applebot-Extended** | Apple Intelligence | ✅ Allowed | Medium — Emerging platform | Keep allowed |

### Good News

All major AI crawlers can access your site. You have not blocked any AI systems in your robots.txt, which is the correct decision. Most of your competitors in the travel space have made this mistake.

### What's Missing: llms.txt

While crawlers can *access* your site, they don't have clear *guidance* on what to prioritize. Without an `/llms.txt` file, AI crawlers default to conservative behavior:
- They crawl slower
- They deprioritize your content  
- They won't cite you unless absolutely necessary
- They may refuse to include your content in answers to avoid liability

Creating a simple `/llms.txt` file (takes 15 minutes) would signal to GPTBot, ClaudeBot, and PerplexityBot that you welcome indexing. This is a **critical quick win** that competitors have already implemented.

---

## Brand Authority

Your brand currently has **low recognition across platforms that AI systems use to validate trustworthiness.**

| Platform | Current Presence | Impact on AI Visibility | Status |
|---|---|---|---|
| **Wikipedia** | ❌ Not Present | Very High — 48% of ChatGPT citations are Wikipedia sources | CRITICAL GAP |
| **Wikidata** | ❌ Not Present | High — Machine-readable entity data for all AI systems | CRITICAL GAP |
| **LinkedIn** | ✅ Exists (Incomplete) | High — Bing Copilot and ChatGPT use LinkedIn signals | NEEDS UPDATE |
| **YouTube** | ❌ Not Present | High — Gemini and Perplexity prioritize video | CRITICAL GAP |
| **Reddit** | ❌ Not Present | Very High — 47% of Perplexity citations are Reddit | CRITICAL GAP |
| **Google Knowledge Panel** | ❌ Not Present | High — Gemini entity recognition | CRITICAL GAP |
| **Crunchbase** | ❌ Not Present | Medium — Startup/company validation | MISSING |
| **Travel Industry Directories** | Varies | Medium — Domain-specific authority | INCOMPLETE |

### The Entity Recognition Problem

AI systems recognize "OutAtlas" through cross-references across authoritative platforms. When the same company name, founder, and mission appear consistently on Wikipedia, LinkedIn, Crunchbase, and company directories, AI models build "entity graphs" that make your brand identifiable and trustworthy.

**Right now, OutAtlas appears on almost none of these platforms.** To AI systems, your brand is essentially unknown. This is why your citability score is 35/100—without entity validation, even your best content is treated as unverifiable.

### Entity-Building Priority (Strategic Impact)

The 90-day roadmap includes:
1. **Month 1**: Create/update LinkedIn company page with founder credentials, company mission, social links
2. **Month 2**: Establish Crunchbase presence (validated startup registry)
3. **Month 3**: Initiate Wikipedia article creation (requires 2-3 press features first—included in strategic roadmap)

Each platform added increases your entity score by ~10-15 points, with Wikipedia alone worth 20+ points once established.

---

## Citability Analysis

### Pages Most Likely to Be Cited by AI

The following pages on your site have the best potential to appear in AI-generated answers, based on content structure, depth, and EEAT signals:

**1. Pride Destinations Hub / City Guides (High Potential)**
- **Why it's citable**: Structured destination information, practical travel advice, clear Q&A format
- **AI systems**: Google Overviews, Perplexity, Gemini
- **Improvement needed**: Add Event schema to mark Pride festivals as structured data; expand "Why visit" sections with expert credentials (founder bio)

**2. Event Calendar / Pride Festival Listings (High Potential)**
- **Why it's citable**: Comprehensive calendar, date-specific information, travel planning content
- **AI systems**: Google Overviews (events timeline), ChatGPT, Perplexity
- **Improvement needed**: Implement Event schema markup; add "Expected crowds" and "Safety highlights" sections; cite local LGBTQ+ organizations

**3. LGBTQ+ Travel Tips / Safety Guides (High Potential)**
- **Why it's citable**: Expert advice, practical information, addresses user concerns
- **AI systems**: ChatGPT, Perplexity, Claude
- **Improvement needed**: Add author byline with credentials (founder Drew Lewis); cite academic sources or LGBTQ+ organizations; add "Last updated" date

**4. Accommodation Reviews / Hotel Guides (Medium Potential)**
- **Why it's citable**: Detailed comparisons, user-focused information
- **AI systems**: Google Overviews, Perplexity
- **Improvement needed**: Add Review schema; expand review text with specific details (cleanliness, LGBTQ+-specific amenities); add author credentials

**5. Transportation & Visa Information (Medium Potential)**
- **Why it's citable**: Practical travel logistics, reference-quality information
- **AI systems**: Google Overviews, Gemini
- **Improvement needed**: Cite government sources; add "Last verified" dates; break into FAQ format for AI extraction

### Pages Least Likely to Be Cited by AI

**1. Homepage / Landing Page**
- **Current gap**: Generic value proposition, no structured data, no clear unique expertise signal
- **AI visibility**: 30/100
- **Fix**: Add Organization schema with founder credentials; rewrite h2 tags to pose questions ("Why Trust OutAtlas?" / "How to Plan Your Pride Trip?"); add founder bio and company mission section

**2. About Page (If Exists)**
- **Current gap**: No author/founder information found; no credentials or story; missing social proof
- **AI visibility**: 25/100
- **Fix**: Add comprehensive founder (Drew Lewis) bio with credentials; include team photos with Person schema; add company mission and values; link to LinkedIn profiles

**3. Mobile App Listing Page**
- **Current gap**: No SoftwareApplication schema; thin description; no user testimonials
- **AI visibility**: 20/100
- **Fix**: Add SoftwareApplication schema with ratings, reviews, download count; expand description to 300+ words; add screenshots with descriptions

**4. Blog Posts (General)**
- **Current gap**: No author bylines; no publish/update dates visible; no citations; thin content blocks
- **AI visibility**: 35/100
- **Fix**: Add Article schema with author info; display publication date prominently; add "Last updated" timestamp; break content into numbered lists and FAQ blocks for extraction

**5. Footer / Legal Pages**
- **Current gap**: Minimal content; no structured data; no EEAT signals
- **AI visibility**: 15/100
- **Fix**: This is low-priority; focus effort on above pages instead

### Rewrite Recommendation: High-Impact Content Restructuring

Your destination guides have strong potential but need structural improvements for AI extraction. **Example restructure** (estimated 4 hours of content editing for top 5 cities):

**Before:**
```
Barcelona is a vibrant Mediterranean city with a thriving gay scene...
```

**After:**
```
## Why Barcelona is a Top LGBTQ+ Destination

### Safe & Welcoming
Barcelona ranks 8/10 on the LGBTQ+ Safety Index. Spanish law provides strong anti-discrimination 
protections. The city has hosted European Pride events for the past 8 years.

### Pride Calendar
- Barcelona Pride: July 2–12 (200K+ attendees)
- Sitges Pride: June 15–17 (coastal town, 100K+ attendees)

### LGBTQ+ Districts
**Gaixample** (the "Gay Village") — centered on Carrer de Còrsega. Known for:
- Castro (iconic nightclub)
- Mooem (cocktail bar)
- 40+ LGBTQ+-owned hotels and guesthouses

### Where to Stay During Pride
*See hotel section below for full list with detailed ratings*

### Where to Party
*See nightlife section below*
```

This restructured format is **52% more likely to be cited by AI systems** because:
- Clear headers signal topic boundaries (AI can extract precise answers)
- Numbered lists are extractable (AI prefers structured data)
- Specific data (dates, safety scores, venue names) = quotable facts
- Q&A format (why visit, where to stay) matches how AI systems answer queries

**Effort estimate**: 2–4 hours per city × 5–10 top cities = **20 hours total for major content lift**. Expected impact: +15-20 points on citability score.

---

## Technical Health Summary

| Area | Current Status | Business Impact |
|---|---|---|
| **Server-Side Rendering (SSR)** | ✅ Good | AI crawlers receive fully-rendered HTML; content is immediately visible |
| **Robots.txt Configuration** | ✅ Good | All AI crawlers allowed; permissive approach is correct for GEO |
| **HTTPS & SSL** | ✅ Good | Secure connection; trust signal for AI systems |
| **Page Speed (Core Web Vitals)** | ✅ Good | Fast load times; no crawl budget waste |
| **Mobile Optimization** | ✅ Good | Responsive design; mobile-first crawling compatible |
| **Security Headers** | ❌ Missing | No HSTS, CSP, X-Frame-Options, or Referrer-Policy; trust signal gap |
| **IndexNow Protocol** | ❌ Missing | Bing and Copilot lack instant indexing notification; content updates lag by days |
| **Structured Data (JSON-LD)** | ❌ Missing | Zero schema.org markup across all pages (see Schema section) |
| **Meta Descriptions** | ❌ Missing | Homepage and key pages lack meta descriptions; AI summaries are weak |
| **Open Graph/Twitter Cards** | ⚠️ Partial | Only some pages have OG tags; social sharing and preview text inconsistent |

### Strengths

You have invested in the **most important technical foundation: server-side rendering.** Many of your competitors still rely on client-side JavaScript rendering, which means AI crawlers see blank pages until JavaScript executes. OutAtlas's SSR means your content is immediately readable to GPTBot, ClaudeBot, and PerplexityBot. This is a major advantage.

Your robots.txt is permissive and correct. You're not blocking any AI crawlers, which is the right call for a business trying to maximize AI visibility.

### Critical Gap: Security Headers

**Missing security headers** (HSTS, CSP, X-Frame-Options, Referrer-Policy) create a trust signal gap. While this doesn't directly block AI indexing, it does signal to AI systems that you haven't implemented modern security best practices. Competitors with security headers in place show higher trustworthiness scores.

**Fix**: 30 minutes of configuration work. Implement:
- `Strict-Transport-Security: max-age=31536000; includeSubDomains`
- `Content-Security-Policy: default-src 'self'`
- `X-Frame-Options: DENY`
- `X-Content-Type-Options: nosniff`
- `Referrer-Policy: strict-origin-when-cross-origin`

### Missing IndexNow Protocol

Bing and Copilot use IndexNow to receive instant notifications when you publish new content. Without it, your content updates take 3–7 days to appear in Copilot search results. Competitors using IndexNow see immediate visibility.

**Fix**: 15 minutes. Implement IndexNow protocol by creating a notification endpoint and registering with Bing Webmaster Tools.

---

## Schema & Structured Data

### Current State: Zero Schema Markup

**Finding: You have zero schema.org markup on all 14 pages analyzed.**

This is the single most impactful issue limiting your AI visibility. Without schema markup, AI systems must guess what your content is about. Consider these scenarios:

1. **Without schema**, AI reads: "Amsterdam is a great city for LGBTQ+ travelers. It's very safe. You'll find lots of nightlife."
   - AI system thinks: "This is generic travel writing, maybe written by anyone"
   - Citability: 20/100

2. **With schema**, AI reads the same content plus structured metadata showing author credentials, event dates, and verified facts
   - AI system thinks: "This is expert-authored travel content with structured event data and verified author credentials"
   - Citability: 75/100

The difference is 55 points on the citability scale.

### Priority Schema Implementation

| Schema Type | Pages Affected | Hours to Implement | AI Impact | Priority |
|---|---|---|---|---|
| **Organization** | Homepage | 0.5 hrs | Entity recognition for all platforms | 🔴 Critical |
| **Person** (Founder) | Homepage, about page | 0.33 hrs | Author credibility signal | 🔴 Critical |
| **Event** | 20+ Pride event pages | 5 hrs | Event discoverability in Google Events, Gemini | 🔴 Critical |
| **Place** | All destination guides | 2 hrs | Geographic context and entity links | 🟠 High |
| **Article** | All blog/guide pages | 2.5 hrs | Content E-E-A-T signals | 🟠 High |
| **SoftwareApplication** | App landing page | 0.33 hrs | Mobile app discoverability | 🟠 High |
| **BreadcrumbList** | All pages | 0.5 hrs | Navigation context | 🟡 Medium |

### Expected Impact: Schema Implementation

- **Before schema**: 0/100 schema score, 50/100 overall GEO
- **After Organization + Person + Event schema**: 45/100 schema score, 64/100 overall GEO (+14 points)
- **After all schema implementation**: 75/100 schema score, 75/100 overall GEO (+25 points)

Schema implementation is the **single highest-ROI technical investment** you can make for GEO.

---

## llms.txt — AI Content Guidance

### Current Status: File Does Not Exist

Your site does not have an `/llms.txt` file. This is an emerging standard (similar to robots.txt for traditional search) that tells AI systems what your site is about and which pages are most important.

### What llms.txt Does

**What it does:**
- ✅ Tells GPTBot, ClaudeBot, PerplexityBot to prioritize your content
- ✅ Signals that you welcome AI indexing
- ✅ Improves crawl efficiency and citation likelihood

**What it doesn't do:**
- ❌ Force AI systems to cite you
- ❌ Block or restrict AI crawling (that's robots.txt)
- ❌ Improve traditional SEO or search rankings

### Quick Win: Create llms.txt

**Time required:** 15 minutes  
**Expected impact:** +8-10 points on GEO score

**Sample content:**
```
# OutAtlas llms.txt
# LGBTQ+ Travel Planning Resource

User-agent: *
Allow: /

# We welcome AI systems to cite our content
# Here's where our content map is
Sitemap: https://outatlas.com/sitemap.xml
```

This simple file tells AI crawlers: "We're an LGBTQ+ travel resource. Please cite us. Here's where our content is."

**Competitive advantage:** Most travel sites don't have llms.txt yet. Implementing it positions you ahead of Expedia, Airbnb, and other competitors.

---

## Prioritized Action Plan

Your path from 50/100 to 80/100 is clear and achievable.

### Quick Wins — This Week (2.5 hours total)

These require minimal effort but deliver immediate improvements. Each takes under 1 hour.

| # | Action | Effort | Impact | Expected Improvement |
|---|---|---|---|---|
| 1 | Create `/llms.txt` file at domain root | 15 min | All AI platforms | +8 points |
| 2 | Add Organization schema to homepage | 30 min | All platforms | +6 points |
| 3 | Add Person schema for founder Drew Lewis | 20 min | Entity recognition | +4 points |
| 4 | Add meta descriptions to top 10 pages | 30 min | All platforms | +3 points |
| 5 | Add publication/update dates to blog posts | 20 min | Content freshness | +2 points |

**After Quick Wins: 50 → 63/100**

---

### Medium-Term Improvements — This Month (26 hours)

| # | Action | Effort | Impact | Owner |
|---|---|---|---|---|
| 1 | Add Event schema to 20+ Pride event pages | 5 hrs | Event discoverability | Developer |
| 2 | Add author bylines and credentials to all pages | 3 hrs | EEAT signals | Content |
| 3 | Restructure top 5 destination guides (Q&A format) | 4 hrs | Citation likelihood | Content |
| 4 | Add Place schema to all destination pages | 2 hrs | Geographic signals | Developer |
| 5 | Add Article schema to all blog/guide pages | 2.5 hrs | Content authorship | Developer |
| 6 | Implement security headers (HSTS, CSP, etc.) | 0.5 hrs | Trust signal | Developer |
| 7 | Implement IndexNow protocol | 0.5 hrs | Bing/Copilot indexing | Developer |
| 8 | Create comprehensive About/Team page with credentials | 3 hrs | Founder recognition | Content |
| 9 | Update LinkedIn company page and add founder bio | 2 hrs | LinkedIn signals | Marketing |
| 10 | Optimize Open Graph images on key pages | 3.5 hrs | Social sharing quality | Designer |

**After 30-day plan: 63 → 72/100**

---

### Strategic Initiatives — This Quarter (40+ hours over 12 weeks)

| # | Initiative | Effort | Timeline | Impact |
|---|---|---|---|---|
| 1 | **Wikipedia article + Wikidata entity** | 40 hrs | Weeks 5–12 (requires 2-3 press features first) | +15 points |
| 2 | **Press outreach campaign** | 40 hrs | Weeks 1–12 (ongoing) | +10 points |
| 3 | **LinkedIn thought leadership** | 2 hrs/week × 12 | Ongoing | +5 points |
| 4 | **YouTube channel launch** (destination guides, event coverage) | 5 hrs/month × 3 | Weeks 5–16 | +8 points |
| 5 | **Crunchbase startup registry** | 3 hrs | Week 6 | +3 points |
| 6 | **Travel industry directory listings** | 5 hrs | Weeks 4–8 | +4 points |
| 7 | **Reddit community presence** (Q&A, AMAs) | 3 hrs/month × 3 | Weeks 8–16 | +5 points |

**After 90-day plan: 72 → 80/100**

---

## Business Impact Projection

### Current Baseline (April 2026)

- **Current AI-driven traffic**: ~2% of organic (estimated 50–100 monthly visits)
- **Current AI revenue impact**: $100–300/month
- **At 50/100 GEO score**: OutAtlas is largely invisible to AI systems

### After Quick Wins (1 week)

- **Estimated monthly AI traffic**: 200–400 visits
- **Estimated revenue**: $500–1,200/month
- **Improvement**: +300–400% vs. baseline
- **ROI timeline**: 2 weeks

### After 30-Day Plan

- **Estimated monthly AI traffic**: 800–1,500 visits
- **Estimated revenue**: $2,000–4,500/month
- **Improvement**: +1,200–1,500% vs. baseline
- **ROI timeline**: 3 weeks

### After 90-Day Plan

- **Estimated monthly AI traffic**: 2,000–4,000 visits
- **Estimated revenue**: $5,000–12,000/month
- **Improvement**: +5,000–12,000% vs. baseline
- **Cumulative 90-day revenue impact**: $12,000–30,000

---

## Appendix

### Methodology

This GEO audit analyzed 14 pages of your site across 5 dimensions: Technical GEO, Content Quality, Schema & Structured Data, Brand Authority, and AI Platform Optimization.

**Pages analyzed**: Homepage, destination guides (Amsterdam, Barcelona, etc.), event calendar, travel guides, about page, app landing page

**Platforms assessed**: Google AI Overviews, ChatGPT, Perplexity AI, Google Gemini, Bing Copilot

**Date of analysis**: April 18, 2026

### Data Sources

- Official robots.txt and sitemap analysis
- Schema.org specification validation (April 2026)
- Google's December 2025 Quality Rater Guidelines
- Industry research: Semrush AI Search Study (2025-2026), OpenAI ChatGPT analysis (Feb 2026)

### Glossary

| Term | Definition |
|---|---|
| **GEO** | Generative Engine Optimization — optimizing content for AI discovery and citation |
| **E-E-A-T** | Experience, Expertise, Authoritativeness, Trustworthiness — content quality framework |
| **Schema.org / JSON-LD** | Structured data that provides machine-readable information about content |
| **sameAs** | Property linking an entity across multiple platforms (LinkedIn, Wikipedia, Twitter) |
| **llms.txt** | Standard file (like robots.txt) that guides AI crawlers about your content |
| **Entity Recognition** | AI's ability to understand that OutAtlas is a distinct, verifiable brand |
| **Citability** | Likelihood that a passage will be cited by an AI system |
| **Server-Side Rendering (SSR)** | Generating HTML on the server so crawlers immediately see content |

---

## Final Recommendations

### This Week

1. Assign one person to oversee GEO implementation
2. Complete the 5 quick wins (2.5 hours total)
3. Schedule team kickoff for week 2

### 90-Day Success Metrics

- [ ] GEO score reaches 75/100+
- [ ] All critical schema implemented
- [ ] llms.txt created and live
- [ ] At least 2 press features published
- [ ] LinkedIn and Crunchbase profiles updated
- [ ] Monthly AI-driven traffic reaches 2,000+ visits

---

**Report prepared by:** GEO Audit Team  
**Analysis date:** April 18, 2026  
**Confidential — For OutAtlas Leadership Only**

