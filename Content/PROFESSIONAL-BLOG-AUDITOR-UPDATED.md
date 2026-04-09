---
name: professional-blog-auditor
description: Advanced blog performance auditor delivering detailed GEO, SEO, and AI writing forensics with competitor comparison. **NEW: All audits documented in .docx files with persistent records for campaign strategy validation.** Use whenever the user wants to analyze a blog post, check if content is AI-generated, optimize for search visibility, improve citation likelihood, or benchmark against competitors. Provides three 0-100 scores (GEO likelihood for AI citations, SEO search optimization, AI writing style detection) with exact text evidence for each, direct competitor gap analysis, and a Priority 6 improvement report with before/after examples. Perfect for content creators, marketers, publishers, and anyone wanting to understand exactly why content performs or doesn't perform in search and AI systems.
---

# Professional Blog Auditor — UPDATED VERSION
**Enhanced with .docx output files and persistent audit records**

---

## 🆕 WHAT'S NEW IN THIS VERSION

This updated skill now produces:
1. **Professional .docx audit reports** documenting all analysis and recommendations
2. **Persistent audit archive** (`[Brand]_BlogAudits_Archive.docx`) tracking all audits across sessions
3. **Performance history for weeks 3-5** reference when validating content strategy during ad campaigns

### Why This Matters
When running Google Ads campaigns in weeks 3-5, you need to reference which blog posts were audited, their scores, and what improvements were recommended. This file documents the quality and optimization level of content supporting your campaigns.

---

## UPDATED WORKFLOW

### STEP 3 (UPDATED) — DOCX Audit Report Generation

When the audit is complete, Claude will:

1. **Generate a professional DOCX audit report** containing:
   - **Title Page:** Blog post title, URL, date audited, brand
   - **Scoring Dashboard:**
     - GEO Score (0-100) with exact quote evidence
     - SEO Score (0-100) with exact quote evidence
     - AI Writing Style Score (0-100) with exact quote evidence
   - **Score Interpretation:** What each score means for visibility and performance
   - **Competitor Gap Analysis:**
     - Side-by-side score comparison
     - Win/loss summary
     - Specific gap analysis (what you're missing)
   - **Priority 6 Improvements:**
     - Each issue with evidence, fix, before/after example, and score impact
   - **Action Plan:**
     - Implementation order by impact
     - Effort estimate
     - Potential score improvements
   - **Export & Next Steps**

   **Save as:** `[Brand]_BlogAudit_[PostTitle]_[Date].docx` to your outputs folder

2. **Update the master audit archive** `[Brand]_BlogAudits_Archive.docx` with:
   - Date audited
   - Post title and URL
   - GEO, SEO, and AI scores (snapshot)
   - Competitor compared against
   - Key findings (1-2 sentences)
   - Link to full DOCX audit report
   - Status: "Awaiting improvements" / "Improvements in progress" / "Complete"

**File Structure:**
- **Session File (Primary):** `[Brand]_BlogAudit_[PostTitle]_[Date].docx`
  - Complete audit for immediate action

- **Master Archive (Persistent):** `[Brand]_BlogAudits_Archive.docx`
  - All audits accumulated across sessions
  - Organized by date and post
  - **Reference during weeks 3-5 to confirm content quality**

---

## STEP 4 (UPDATED) — Historical Record & Re-Audit Tracking

After the audit report is saved:

1. **If this is a re-audit** (of a previously improved post):
   - Compare scores against the previous audit
   - Document improvements made (score deltas)
   - Update the master archive with new scores and status
   - Note what improvements were most impactful

2. **Archive entry structure:**
   ```
   📄 "Best Pride Destinations in 2026" (OutAtlas)
   🔗 https://outatlas.com/blog/pride-destinations-2026
   📅 Audited: March 28, 2026

   SCORES:
   - GEO: 78/100 ↑ (+12 from Mar 15)
   - SEO: 82/100 ↑ (+8 from Mar 15)
   - AI: 28/100 ↓ (-5, more human, good!)

   KEY FINDING: Strong improvement after adding expert citations and reducing repetitive phrases. Ready for ad campaigns.

   COMPETITOR: "Top Pride Cities 2026" (competing blog)
   WIN/LOSS: You now win on GEO (+15 points) and AI authenticity

   REPORT: OutAtlas_BlogAudit_BestPrideDestinations_Mar28.docx
   STATUS: ✅ Ready for Ads Campaign Week 3-5
   ```

---

## STEP 5 (NEW) — Week 3-5 Content Validation

When planning Google Ads campaigns in weeks 3-5:

1. **Open the master archive** `[Brand]_BlogAudits_Archive.docx`
2. **Check each blog post's audit status:**
   - GEO score ≥75? (Good for AI citations and organic reach)
   - SEO score ≥75? (Good for organic search traffic)
   - AI score <30? (Good for human authenticity and reader trust)
3. **Reference the audit date** and any improvements noted
4. **Use audit insights** to inform ad copy and landing page strategy
   - High GEO post = emphasize specificity and data in ads
   - High SEO post = focus on search-driven CTAs
   - Low AI score = emphasize human expertise in testimonials

**Example Week 3-5 Validation:**
```
Google Ads Campaign Planning for OutAtlas (April 2026)

Blog Post: "Ultimate Gay Travel Guide to Barcelona"
Audit Status: Last audited Mar 15
GEO Score: 82/100 ✅ (Strong — emphasize data in ads)
SEO Score: 76/100 ✅ (Good — can drive organic traffic)
AI Score: 24/100 ✅ (Very human — use in campaign testimonials)

→ Ad Strategy: Feature specific Barcelona neighborhoods and insider tips
→ Landing Page: Link from blog post audit timestamp (establishes freshness)
→ Testimonial Approach: Use human voice from blog content in ad copy
```

---

## ALL OTHER STEPS UNCHANGED

Steps 1-2 (Content Input → Competitor Comparison) and the core audit analysis remain exactly the same.
See original SKILL.md for complete scoring methodology and improvement formulas.

---

## FINAL CONFIRMATION MESSAGE

After both .docx files are saved and archived:

```
✅ Blog audit completed and archived!

📄 Full Audit Report: [Brand]_BlogAudit_[PostTitle]_[Date].docx
📚 Audit Archive: [Brand]_BlogAudits_Archive.docx (updated)

**Week 3-5 Ready:** Your blog post performance metrics are documented in the master archive. When planning Google Ads campaigns, reference this file to confirm content quality and optimization levels.

📊 SCORES SUMMARY:
- GEO: [X]/100 — AI Citation Likelihood
- SEO: [X]/100 — Search Optimization
- AI: [X]/100 — Human Authenticity

⚡ TOP IMPROVEMENTS: [List top 3 Priority 6 items]
```

---

## SAMPLE MASTER ARCHIVE STRUCTURE

```
BLOG AUDIT ARCHIVE — OutAtlas
Updated: March 28, 2026

📄 "Best Pride Destinations in 2026"
URL: https://outatlas.com/blog/pride-destinations-2026
Audited: March 28, 2026
Competitor: "Top Pride Cities 2026" (Nomadic Boys blog)

SCORES:
  GEO: 78/100 ⚠️ (Needs expert citations)
  SEO: 82/100 ✅ (Strong keyword targeting)
  AI: 28/100 ✅ (Very human)

KEY FINDINGS: Well-structured post with good SEO foundation, but lacks specific data citations. Adding 5-10 expert quotes would boost GEO score to 90+.

REPORT: OutAtlas_BlogAudit_BestPrideDestinations_Mar28.docx
STATUS: ⏳ Awaiting improvements
WEEK 3-5 USE: Hold off on heavy promotion until GEO improvements are made (week 2 expected)

---

📄 "Hidden Gem LGBTQ+ Bars in Bangkok"
URL: https://outatlas.com/blog/lgbtq-bars-bangkok
Audited: March 22, 2026
Competitor: "Best Gay Bars in Thailand" (travel magazine)

SCORES:
  GEO: 85/100 ✅ (Strong citations)
  SEO: 78/100 ✅ (Good structure)
  AI: 19/100 ✅ (Very human, personal voice)

KEY FINDINGS: Excellent post. High authenticity with specific local details. Ready for paid campaigns immediately.

REPORT: OutAtlas_BlogAudit_HiddenGemBars_Bangkok_Mar22.docx
STATUS: ✅ Ready for Ads Campaign
WEEK 3-5 USE: Priority content for Google Ads landing pages. Emphasize "insider tips" angle in ad copy.

---

📄 "Complete Travel Safety Guide for LGBTQ+ Travelers"
URL: https://outatlas.com/blog/lgbtq-travel-safety
Audited: March 15, 2026 (Initial) → March 27, 2026 (Re-audit)
Competitor: "LGBTQ+ Travel Safety Handbook" (external blog)

SCORES (INITIAL Mar 15):
  GEO: 62/100 ⚠️
  SEO: 78/100 ✅
  AI: 35/100 ⚠️

SCORES (RE-AUDIT Mar 27):
  GEO: 78/100 ✅ (+16 points) — Added expert citations + statistics
  SEO: 84/100 ✅ (+6 points) — Revised H1 and added internal links
  AI: 22/100 ✅ (-13, more human) — Reduced repetitive phrases

IMPROVEMENTS MADE:
  ✅ Added 8 expert quotes from travel safety orgs
  ✅ Included 12 specific statistics with sources
  ✅ Revised H1 for better keyword targeting
  ✅ Added 5 internal links to related guides
  ✅ Replaced generic transitions with varied language

REPORT: OutAtlas_BlogAudit_TravelSafetyGuide_Mar27.docx (updated)
STATUS: ✅ Ready for Ads Campaign
WEEK 3-5 USE: High-priority content. Use GEO + SEO improvements in campaign messaging. Featured content for retargeting website visitors.
```

---

## HOW TO USE THIS UPDATED SKILL

**For Initial Blog Audits (Day 1):**
- Use /professional-blog-auditor as normal
- Get the full .docx audit report with all analysis
- Master archive gets created automatically
- Save both files to your workspace

**For Re-Audits (After Improvements):**
- Run the auditor again on the improved post
- Claude reads the master archive and compares scores
- Updates archive with improvement metrics
- Saves new .docx report showing before/after

**For Week 3-5 Google Ads Validation:**
- Open `[Brand]_BlogAudits_Archive.docx`
- Find your blog posts by date
- Check GEO/SEO/AI scores
- Use scores to inform campaign landing pages and ad copy
- Reference audit dates to show content freshness

---

## STORAGE LOCATION

All .docx files saved to:
`/sessions/wizardly-dazzling-heisenberg/mnt/Content/`

Archive file persists and is updated each session.

---

## INTEGRATION WITH CONTENT-PLANNER

These blog audits work together with /content-planner:
- Content Planner creates blog posts
- Professional Blog Auditor measures their performance
- Archive documents quality levels
- Week 3-5: Both archives inform ad campaign strategy

---

## ORIGINAL STEPS 1-2 REFERENCE

(All original workflow steps for input, analysis, and scoring remain unchanged — see original SKILL.md for complete instructions on scoring methodology, competitor comparison, and improvement formulas.)
