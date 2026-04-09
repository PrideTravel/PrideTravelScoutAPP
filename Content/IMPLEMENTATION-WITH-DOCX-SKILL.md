# Implementation Guide: Using /docx Skill with Your Three Skills

## Overview

You now have the `/docx` skill available, which means we can **automate `.docx` file generation** for all three skills. Here's how to integrate it.

---

## QUICK START

Each skill should be updated with this instruction at the end:

### For `/content-planner`:
After Step 8 (Session Summary), add:
```
## STEP 9 — Generate .DOCX File

Use the /docx skill to create the Content Calendar document:

1. Call the /docx skill
2. Request: "Create a professional Content Calendar .docx with:
   - Title: 'Content Calendar — [Brand] — [DateRange]'
   - Executive summary (posts, platforms, theme)
   - Content calendar table (Date | Platform | Concept | Status | Asset)
   - Detailed post breakdown for each approved post
   - Historical Record section with batch metadata and Week 3-5 notes"
3. Save as: [Brand]_ContentCalendar_[DateRange].docx
4. ALSO update the master history file: [Brand]_ContentHistory.docx
```

### For `/growth-traffic-manager`:
After Step 7 (Task Export), add:
```
## STEP 8 — Generate .DOCX Growth Plan

Use the /docx skill to create the Growth Plan document:

1. Call the /docx skill
2. Request: "Create a professional Growth & Traffic Plan .docx with:
   - Title: 'Growth & Traffic Plan — [Brand] — [Date]'
   - Executive Summary (goal, budget, audience, KPI target)
   - Strategy Brief
   - Paid Advertising Channels section (each platform with budget allocation)
   - Partnership & Outreach strategies
   - SEO & Content Traffic section
   - Budget Allocation table
   - Action Checklist (Week/Month/Quarter)
   - Historical Record with strategic notes and Week 3-5 KPI targets"
3. Save as: [Brand]_GrowthPlan_[Date].docx
4. ALSO update the master archive: [Brand]_GrowthStrategy_Archive.docx
```

### For `/professional-blog-auditor`:
After Step 4 (Historical Record), add:
```
## STEP 5 — Generate .DOCX Audit Report

Use the /docx skill to create the Blog Audit document:

1. Call the /docx skill
2. Request: "Create a professional Blog Post Audit .docx with:
   - Title: 'Blog Post Audit'
   - Post Title, URL, Audit Date, Competitor
   - SCORING DASHBOARD with GEO, SEO, AI scores (each with evidence quotes)
   - COMPETITOR GAP ANALYSIS with comparison table
   - PRIORITY 6 IMPROVEMENTS (each with Issue, Evidence, Fix, Before/After, Score Impact)
   - ACTION PLAN with implementation order
   - Historical Record with audit metadata and Week 3-5 guidance"
3. Save as: [Brand]_BlogAudit_[PostTitle]_[Date].docx
4. ALSO update the master archive: [Brand]_BlogAudits_Archive.docx
```

---

## HOW TO USE THIS IN PRACTICE

### Workflow for Content Planner:

```
1. Run /content-planner
2. Plan your content batches (Steps 1-8)
3. At end, ask Claude: "Generate the .docx files now"
4. Claude calls the /docx skill with full specifications
5. Files are created and saved to /sessions/.../mnt/Content/
6. Both session file and master archive are updated
```

### Workflow for Growth Manager:

```
1. Run /growth-traffic-manager
2. Build your growth strategy (Steps 1-7)
3. At end, ask Claude: "Generate the .docx files now"
4. Claude calls the /docx skill with full specifications
5. Files are created and saved to /sessions/.../mnt/Content/
6. Both session file and master archive are updated
```

### Workflow for Blog Auditor:

```
1. Run /professional-blog-auditor
2. Complete your blog audit (Steps 1-4)
3. At end, ask Claude: "Generate the .docx file now"
4. Claude calls the /docx skill with full specifications
5. Files are created and saved to /sessions/.../mnt/Content/
6. Both session file and master archive are updated
```

---

## MASTER ARCHIVE FILES

Each skill maintains a **persistent master archive file** that should be updated each session:

### Content Planner Master:
**File:** `[Brand]_ContentHistory.docx`
**Updated by:** /docx skill at end of each session
**Contains:** All batches accumulated, organized by date
**Updated section per session:**
```
📅 [DATE] — [Brand] Content Batch
- Platforms: [list]
- Posts: [#] planned, [#] approved, [#] in revision
- Theme: [theme]
- Session File: [Brand]_ContentCalendar_[DateRange].docx
- Status: [summary]
- Week 3-5 Note: [strategic notes]
```

### Growth Manager Master:
**File:** `[Brand]_GrowthStrategy_Archive.docx`
**Updated by:** /docx skill at end of each session (or performance check-in)
**Contains:** All plans accumulated, organized by date with performance data
**Updated section per session:**
```
📅 [DATE] PLAN / REVISION (Status)
Goals: [goal]
Monthly Budget: [amount]
Channels: [list]
Key KPI Targets: [list]
Strategic Notes: [decisions made]
Session File: [Brand]_GrowthPlan_[Date].docx
Review Date: [next check-in date]
```

### Blog Auditor Master:
**File:** `[Brand]_BlogAudits_Archive.docx`
**Updated by:** /docx skill at end of each audit
**Contains:** All audits accumulated, organized by date and post title
**Updated section per audit:**
```
📄 "[Post Title]"
URL: [link]
Audited: [date]
SCORES: GEO [X]/100 | SEO [X]/100 | AI [X]/100
Competitor: [compared against]
Key Finding: [1-2 sentences]
Report: [Brand]_BlogAudit_[PostTitle]_[Date].docx
Status: [Ready / Awaiting Improvements / In Progress]
Week 3-5 Use: [guidance for ads]
```

---

## EXAMPLE: USING THE DOCX SKILL

When you ask Claude to generate the files, here's what happens:

**You ask:** "Generate the .docx files now"

**Claude does:**
1. Calls the `/docx` skill with detailed specifications
2. Specifies all sections, tables, formatting, content
3. `/docx` creates the professional document
4. Document is saved to `/sessions/.../mnt/Content/[Brand]_ContentCalendar_Mar28-31.docx`
5. Claude also calls `/docx` skill again to update the master archive file
6. Both files are ready for reference

**Files created:**
- `OutAtlas_ContentCalendar_Mar28-31.docx` (session file)
- `OutAtlas_ContentHistory.docx` (master archive, updated with new batch entry)

---

## STORAGE LOCATION

All `.docx` files are saved to:
```
/sessions/wizardly-dazzling-heisenberg/mnt/Content/
```

This folder persists between sessions, so:
- Master archive files accumulate across sessions
- Session files are easy to find by date
- Week 3-5: Open master files to reference original strategy

---

## NAMING CONVENTIONS

**Session Files (one per planning session):**
- Content: `[Brand]_ContentCalendar_[DateRange].docx`
  - Example: `OutAtlas_ContentCalendar_Mar28-31.docx`
  - Example: `TravelInPride_ContentCalendar_Mar21-28.docx`

- Growth: `[Brand]_GrowthPlan_[Date].docx`
  - Example: `OutAtlas_GrowthPlan_Mar28.docx`
  - Example: `TravelInPride_GrowthPlan_Feb14.docx`

- Blog: `[Brand]_BlogAudit_[PostTitle]_[Date].docx`
  - Example: `OutAtlas_BlogAudit_BestPrideDestinations_Mar28.docx`
  - Example: `TravelInPride_BlogAudit_CruiseGuide_Mar15.docx`

**Master Archive Files (persistent across sessions):**
- `[Brand]_ContentHistory.docx`
  - Example: `OutAtlas_ContentHistory.docx`
  - Example: `TravelInPride_ContentHistory.docx`

- `[Brand]_GrowthStrategy_Archive.docx`
  - Example: `OutAtlas_GrowthStrategy_Archive.docx`
  - Example: `TravelInPride_GrowthStrategy_Archive.docx`

- `[Brand]_BlogAudits_Archive.docx`
  - Example: `OutAtlas_BlogAudits_Archive.docx`
  - Example: `TravelInPride_BlogAudits_Archive.docx`

---

## WEEK 3-5 REFERENCE WORKFLOW

When running Google Ads campaigns in weeks 3-5:

1. **Open master archive files** from `/sessions/.../mnt/Content/`
2. **Find relevant entries** by date and brand
3. **Confirm original strategy:**
   - What was the plan?
   - What were the KPI targets?
   - What content was created?
   - What decisions were made?
4. **Validate current campaign:**
   - Is ad creative aligned with original messaging?
   - Are KPI targets on track?
   - Which blog posts are audit-ready?
   - What was the content strategy?
5. **Use as backup documentation** for stakeholder alignment

**Example Week 3-5 check:**
```
Question: "Why is CAC running at $2.75 instead of $2.50?"
Answer: Open OutAtlas_GrowthStrategy_Archive.docx
→ Find "March 28 Plan"
→ See original target was $2.50
→ See original strategy prioritized TikTok
→ Check if TikTok is still primary channel
→ If not, document why and adjust
```

---

## INTEGRATION SUMMARY

| Skill | When to Generate Files | File Output | Master Archive |
|-------|----------------------|-------------|-----------------|
| /content-planner | After Step 8 (Session Summary) | `[Brand]_ContentCalendar_[DateRange].docx` | `[Brand]_ContentHistory.docx` |
| /growth-traffic-manager | After Step 7 (Task Export) | `[Brand]_GrowthPlan_[Date].docx` | `[Brand]_GrowthStrategy_Archive.docx` |
| /professional-blog-auditor | After Step 4 (Historical Record) | `[Brand]_BlogAudit_[PostTitle]_[Date].docx` | `[Brand]_BlogAudits_Archive.docx` |

All files:
- Save to `/sessions/.../mnt/Content/`
- Follow naming conventions above
- Include historical records for week 3-5 reference
- Master archives accumulate across sessions

---

## NEXT STEPS

1. **Start with one skill** — Try /content-planner first
   - Plan your content as normal
   - At the end, ask: "Generate the .docx files now"
   - Claude will call the /docx skill and create both files
   - Check `/sessions/.../mnt/Content/` for the generated files

2. **Review the generated files**
   - Open `[Brand]_ContentCalendar_[DateRange].docx`
   - Confirm all sections, formatting, and content
   - Verify the master archive file was created/updated

3. **Repeat with other skills** once you're confident
   - Use /growth-traffic-manager
   - Use /professional-blog-auditor

4. **Week 3-5: Reference the master archives**
   - Open master files during Google Ads campaigns
   - Confirm strategy alignment
   - Use as backup documentation

---

## TEMPLATE REFERENCE

The detailed templates (what content goes in each section) are in:
- **DOCX-TEMPLATES-GUIDE.md** — Complete examples for all three skills

When you call the /docx skill, Claude will use these templates to create properly formatted, professional documents.

---

## TROUBLESHOOTING

**"The .docx file wasn't created"**
→ Ask Claude to try again: "Can you generate the .docx file for this content plan?"
→ The /docx skill will retry with full specifications

**"I can't find the file in /Content/"**
→ Make sure to look in: `/sessions/wizardly-dazzling-heisenberg/mnt/Content/`
→ Files are saved there, not in root or other locations

**"The master archive file is missing"**
→ It will be created automatically the first time you use a skill
→ Subsequent sessions will update the same master file

**"I want to update an existing master file manually"**
→ Use the /docx skill with edit mode
→ Claude can append new content to existing master files

---

## YOU'RE READY!

Everything is set up. The next time you use any of the three skills, ask at the end:

**"Generate the .docx files now"**

Claude will call the /docx skill and create:
1. A professional session document with all details
2. An updated master archive file
3. Both saved to your workspace

This gives you the **full documentation system** you need for week 3-5 reference and stakeholder alignment.
