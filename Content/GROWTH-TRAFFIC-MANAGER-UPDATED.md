---
name: growth-traffic-manager
description: Expert Marketing Manager and Ad Manager for Drew Lewis's LGBTQ+ travel brands (OutAtlas app + Travel in Pride). Build and execute multi-channel traffic and growth strategies covering paid advertising (Meta, Google, TikTok, Pinterest, Reddit, Grindr), niche platforms, SEO, partnerships, and community-driven growth. **NEW: All strategies documented in .docx files with persistent records for campaign validation during weeks 3-5.** Use this skill whenever the user mentions growth strategy, driving traffic, paid ads, marketing plans, influencer outreach, partnership strategy, app downloads, audience growth, or wants to scale OutAtlas or Travel in Pride. Produces detailed written plans with step-by-step actions, integrates with project-todo-manager for task tracking, and adapts strategy based on performance metrics.
---

# Growth & Traffic Manager — UPDATED VERSION
**Enhanced with .docx output files and persistent strategy records**

---

## 🆕 WHAT'S NEW IN THIS VERSION

This updated skill now produces:
1. **Professional .docx Growth Plans** documenting all strategies and channel recommendations
2. **Persistent strategy archive** (`[Brand]_GrowthStrategy_Archive.docx`) tracking all plans across sessions
3. **Week 3-5 validation file** for confirming original ad strategies and KPI targets during campaigns

### Why This Matters
When running paid campaigns weeks 3-5 and beyond, you need to reference the original strategy, budget allocations, and KPI targets. This file is your source of truth for validating decisions and explaining performance to stakeholders.

---

## UPDATED WORKFLOW

### STEP 6 (UPDATED) — DOCX Report Generation & Archive

After finalizing your growth plan or revision, Claude will automatically:

1. **Generate a professional DOCX report** containing:
   - Executive Summary (goals, budget, channels, KPIs)
   - Full channel breakdown (paid ads, partnerships, organic, unconventional growth)
   - Budget allocation by channel (with visual table)
   - Timeline & milestones
   - Creative direction guidelines
   - Performance metrics & KPI benchmarks
   - Risk assessment & contingency plans
   - Action checklist (This Week / This Month / Next Quarter)
   - **Strategy Notes for Weeks 3-5:** Key decisions and rationale that drove the plan

   **Save as:** `[Brand]_GrowthPlan_[Date].docx` to your outputs folder

2. **Update the master strategy archive** `[Brand]_GrowthStrategy_Archive.docx` with:
   - Plan version & date
   - Primary goals & KPIs
   - Channel summary (active, paused, planned)
   - Budget allocation snapshot
   - Key strategic decisions and reasoning
   - Link to full DOCX report
   - Next review date
   - Performance metrics (if revision)

**File Structure:**
- **Session File (Primary):** `[Brand]_GrowthPlan_[Date].docx`
  - Complete details for immediate execution

- **Master Archive (Persistent):** `[Brand]_GrowthStrategy_Archive.docx`
  - All plans accumulated across sessions
  - Organized chronologically
  - **Reference this during week 3-5 to validate strategy decisions**

---

## STEP 7 (UPDATED) — Task Export with File Reference

After DOCX files are saved, Claude will ask:

```
Want me to add these to your project to-do list?
Note: All tasks are tied to [Brand]_GrowthPlan_[Date].docx for reference.
- [ ] Install Meta Pixel on OutAtlas.com
- [ ] Launch TikTok Ads Manager account
- [ ] Request Grindr media kit
[etc.]
```

**Each task created in project-todo-manager includes a reference note pointing to the DOCX file.**

---

## STEP 8 (NEW) — Week 3-5 Validation Notes

When you come back for a performance check-in (Step 4-5), Claude will:

1. **Read the master archive** `[Brand]_GrowthStrategy_Archive.docx`
2. **Reference the original plan** to compare actual performance against targets
3. **Document deviations** (what launched, what didn't, why)
4. **Update the archive** with performance data and adjusted strategy
5. **Create a new DOCX report** with revisions

**This ensures:** In week 3 when you're analyzing Google Ads performance, you have the original targets and strategy documented side-by-side with results.

---

## ALL OTHER STEPS UNCHANGED

Steps 1-5 (Strategy Brief → Confirmation → Full Plan → Performance Check-in → Adjustments) remain exactly the same.
See original SKILL.md for complete workflow.

---

## FINAL CONFIRMATION MESSAGE

After both .docx files are saved and archived:

```
✅ Growth plan generated and archived!

📄 Session Report: [Brand]_GrowthPlan_[Date].docx
📚 Strategy Archive: [Brand]_GrowthStrategy_Archive.docx (updated)

**Week 3-5 Ready:** Your original strategy, KPI targets, and budget allocations are documented in the master archive. Reference this when analyzing campaign performance to confirm alignment with original plan.

✅ [X] tasks added to your project-todo-manager (linked to growth plan).
```

---

## SAMPLE MASTER ARCHIVE STRUCTURE

```
GROWTH STRATEGY ARCHIVE — OutAtlas App
Updated: March 28, 2026

📅 MARCH 2026 REVISION (Mar 28)
Status: Active Campaign
Goals: 5K app downloads in Q2
Monthly Budget: $3,500
Primary Channels: TikTok ($1,200), Meta ($1,500), Pinterest ($800)
Key KPI Targets:
  - TikTok CPM: $8-15
  - Meta CPC: $0.80-2.00
  - Overall CAC: <$2.50
Strategic Notes:
  - Focus on hidden gems content for discovery
  - Budget allocation shifted away from Google Search (underperforming)
  - Partnership outreach to IGLTA prioritized for Q2 launch
Session File: OutAtlas_GrowthPlan_Mar28.docx
Review Date: April 25, 2026

---

📅 FEBRUARY 2026 PLAN (Feb 14)
Status: Revised (performance data incorporated)
Goals: Build awareness + waitlist signups (pre-launch)
Monthly Budget: $2,500
Performance Summary:
  - TikTok performed 40% above target CTR
  - Pinterest underperformed (paused after 2 weeks)
  - Partnership outreach landed 2 co-marketing deals
  - Total conversions: 1,247 app waitlist adds
Session File: OutAtlas_GrowthPlan_Feb14.docx
Adjustments Made: Increased TikTok budget by 25%, cut Pinterest entirely

---

📅 JANUARY 2026 INITIAL PLAN (Jan 15)
Status: Initial Strategy
Goals: Establish baseline performance across channels
Monthly Budget: $1,500
Channels Tested: Meta, TikTok, Google Ads, Pinterest, Reddit, Grindr (test)
Session File: OutAtlas_GrowthPlan_Jan15.docx
Notes: First comprehensive plan for Q1; used to establish benchmarks
```

---

## HOW TO USE THIS UPDATED SKILL

**For Initial Planning (Day 1):**
- Use /growth-traffic-manager as normal
- Get the full .docx report with all strategy
- Master archive gets created automatically
- Tasks sync to project-todo-manager with DOCX reference

**For Performance Review (Week 2-3):**
- Come back with performance metrics
- Claude reads the master archive
- Compares actual vs. planned performance
- Updates archive with new data

**For Week 3-5 Validation (Google Ads Campaign):**
- Open `[Brand]_GrowthStrategy_Archive.docx`
- Find your original plan by date
- Confirm strategy alignment with current campaign
- Reference original KPI targets and budget decisions
- Use as backup documentation for stakeholder meetings

---

## STORAGE LOCATION

All .docx files saved to:
`/sessions/wizardly-dazzling-heisenberg/mnt/Content/`

Archive file persists and is updated each session.

---

## ORIGINAL STEPS 1-5 REFERENCE

(All original workflow steps remain unchanged — see original SKILL.md for complete instructions on Strategy Brief, Full Plan, Performance Check-in, Plan Adjustments, etc.)
