---
name: content-planner
description: Act as Drew Lewis's personal content strategist and creator. Plan, write, and prep social media content for OutAtlas and Travel in Pride across TikTok, Instagram (Reels, Feed, Stories), YouTube (Shorts + Long-form), Pinterest, LinkedIn, and Reddit. Present 2–3 posts at a time for review, batch-prepped for the next few days or a long weekend. All approved tasks should be added to the `project-todo-manager` skill's task list. **NEW: All work is now documented in .docx files with persistent historical records for ads campaign reference (weeks 3-5).** Triggers on requests like "let's plan content", "what should I post this week", "help me batch content", "create posts for the weekend", "content for OutAtlas / Travel in Pride", "what should I post on TikTok / Instagram / YouTube", "plan my social media", or "I need content ideas".
---

# Content Planner Skill — UPDATED VERSION
**Enhanced with .docx output files and persistent historical record tracking**

---

## 🆕 WHAT'S NEW IN THIS VERSION

This updated skill now produces:
1. **Professional .docx files** documenting all content plans
2. **Persistent historical record** (`[Brand]_ContentHistory.docx`) that accumulates across sessions
3. **Week 3-5 reference file** for confirming original strategy instructions during Google Ads campaigns

### Why This Matters
When running paid ads in weeks 3-5, you need to reference the exact instructions and strategy from when content was originally planned. This file serves as the source of truth.

---

## KEY WORKFLOW CHANGES

### STEP 7 (UPDATED) — Generate DOCX Content Calendar Report
At session end, create and save **a professional Word document** containing:

**DOCX Report Structure:**
- **Title:** "Content Calendar — [Brand Name] — [Date Range]"
- **Executive Summary:** (2–3 lines: total posts, platforms, theme, assets needed)
- **Detailed post breakdown** (one section per post):
  - Post concept + platform
  - Hook, caption, CTAs
  - Asset guidance
  - Platform-specific timing
  - Hashtags
- **Content calendar table** (visual overview of all posts by date/platform)
- **Asset checklist** (what needs to be created/captured)
- **Next steps & scheduling dates**
- **Historical Record Section:**
  - Status of each post (Approved / Rejected / In Revision)
  - Approval date and any notes from review
  - Links to this session's tasks in project-todo-manager
  - Strategy notes for future reference

**File Structure:**
1. **Session File (Primary):** `[Brand]_ContentCalendar_[DateRange].docx`
   - Everything from this specific batch
   - Ready for immediate reference

2. **Master History File (Persistent):** `[Brand]_ContentHistory.docx`
   - Accumulates ALL batches across sessions
   - Organized by date, platform, and approval status
   - Updated automatically each session
   - **This is your week 3-5 reference during Google Ads campaigns**

---

## ALL STEPS 1-6 REMAIN THE SAME
(See original SKILL.md for full workflow — no changes to:
- Session Kickoff
- Content Strategy Brief
- Generate 2-3 Posts
- Review & Adjust
- Add to Project To-Do List
- Continue Batching)

---

## STEP 8 (NEW) — Historical Record Update

Before concluding the session:

1. **Read the master file** `[Brand]_ContentHistory.docx` (if it exists)
2. **Append this batch's entries** with:
   - Date of planning
   - Brand (OutAtlas / Travel in Pride)
   - Platforms included
   - Number of posts planned
   - Approval status summary
   - Link to this session's .docx report
   - Any strategic notes for week 3-5 reference

3. **Save the updated master file** as `[Brand]_ContentHistory.docx`

**Sample master file structure:**
```
MARCH 2026 — CONTENT HISTORY

📅 March 28 — OutAtlas Content Batch
- Platforms: TikTok, Instagram Reels, YouTube Shorts
- Posts: 3 planned, 2 approved, 1 in revision
- Theme: Hidden Gems in Spanish Cities
- Session File: OutAtlas_ContentCalendar_Mar28-31.docx
- Status: Ready for asset capture by April 1
- Week 3-5 Note: Focus on AI image generation for consistency

📅 March 21 — Travel in Pride Weekly
- Platforms: Instagram Feed, LinkedIn, Reddit
- Posts: 4 planned, 4 approved
- Theme: Pride Season Prep & Early Events
- Session File: TravelInPride_ContentCalendar_Mar21-28.docx
- Status: 3 posts scheduled, 1 awaiting asset approval
- Week 3-5 Note: Use the "Pride Month Calendar" angle in Google Ads retargeting

[etc.]
```

---

## FINAL CONFIRMATION MESSAGE

After both files are saved and updated, say:

```
✅ Content calendar generated and saved!

📄 Session Report: [Brand]_ContentCalendar_[DateRange].docx
📚 Master History: [Brand]_ContentHistory.docx (updated with this batch)

**Week 3-5 Reference Ready:** Your content strategy is documented in the master history file. When running Google Ads campaigns in weeks 3-5, reference this file to confirm the original instructions and strategy.

✅ [X] tasks added to your project-todo-manager.
```

---

## BRAND VOICE & PLATFORM CHEAT SHEET
(No changes — see original SKILL.md for full reference)

---

## HOW TO USE THIS UPDATED SKILL

**For Day 1-2 Planning:**
- Use /content-planner as normal
- Get the session .docx file with all details
- Add approved tasks to project-todo-manager
- Master history file auto-updates

**For Weeks 3-5 (Google Ads Verification):**
- Open `[Brand]_ContentHistory.docx`
- Find the relevant batch by date and platform
- Confirm the original strategy, CTAs, and asset guidance
- Use this to validate ad creative and messaging alignment

---

## STORAGE LOCATION

All .docx files should be saved to:
`/sessions/wizardly-dazzling-heisenberg/mnt/Content/`

This keeps them in your workspace for easy access and version history.
