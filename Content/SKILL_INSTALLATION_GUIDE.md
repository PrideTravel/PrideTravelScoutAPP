# Caption-Voiceover-Writer Skill — Installation Guide

**Skill File:** `caption-voiceover-writer.skill` (13 KB)
**Version:** 1.0
**Created:** March 28, 2026

---

## What You're Getting

A complete, battle-tested social media caption and voiceover script writing skill for OutAtlas and Travel in Pride. The skill has been:

✅ **Designed** — Comprehensive 8-step workflow with all platform best practices
✅ **Tested** — Run through 3 realistic test scenarios (urgent posts, multi-platform calendars, diverse strategies)
✅ **Evaluated** — All outputs meet platform compliance and brand voice standards
✅ **Packaged** — Ready to install in your Cowork workspace

---

## Package Contents

```
caption-voiceover-writer.skill
├── SKILL.md                    (12 KB)  — Complete skill workflow + platform guidelines
├── README.md                   (4 KB)   — User guide & feature overview
├── evals.json                  (2 KB)   — Test case definitions
└── scripts/
    └── export_captions_to_docx.py  — Optional Python script for .docx export
```

---

## Installation Instructions

### Option 1: Install via Cowork (Recommended)

1. **Download the skill file**
   - File: `/sessions/funny-practical-fermat/mnt/Content/caption-voiceover-writer.skill`
   - Size: ~13 KB

2. **Open Cowork skills manager**
   - Look for "Install Skill" or "Add Skill" button
   - Or navigate to your skills directory

3. **Upload the .skill file**
   - Drag and drop `caption-voiceover-writer.skill`
   - Or browse and select the file

4. **Verify installation**
   - The skill should appear in your available skills list
   - Look for "caption-voiceover-writer" in the skills menu

### Option 2: Manual Installation

If you prefer to install manually:

1. **Extract the skill file**
   ```bash
   tar -xzf caption-voiceover-writer.skill -C ~/.cowork/skills/
   ```

2. **Verify the directory structure**
   ```
   ~/.cowork/skills/caption-voiceover-writer/
   ├── SKILL.md
   ├── README.md
   ├── evals.json
   └── scripts/
   ```

3. **Restart Cowork** if needed

---

## First Use Checklist

- [ ] Skill appears in your available skills list
- [ ] You can trigger it with "write captions for my posts"
- [ ] Test with one of the example scenarios below

---

## Quick Start Examples

### Example 1: One-Off Urgent Post (3 minutes)

```
"I'm in Barcelona and just found an amazing queer-friendly hotel.
I want to post about it on TikTok and Instagram Reels right now.
Can you write captions? Goal is awareness and app signups."
```

**Result:** 2 ready-to-post captions in minutes

### Example 2: Multi-Platform Calendar (10 minutes)

```
"I'm planning Pride Month content for June 16-22.
Post 1: 'Best Pride Events' → YouTube Shorts, Pinterest, LinkedIn
Post 2: 'Circuit Party Season' → TikTok, Instagram Reels, Reddit (with voiceover in energetic tone)
Brand: Travel in Pride"
```

**Result:** 6 captions + 1 voiceover script with platform-specific formatting

### Example 3: Strategic Multi-Platform (15 minutes)

```
"I have a travel story about hidden gems in Southeast Asia.
I want to adapt it for Instagram (carousel), YouTube (long-form), and Pinterest (planning-focused).
Brand: OutAtlas. Goal: awareness + app signups."
```

**Result:** 3 completely different captions showing how one story works across platforms

---

## How to Use the Skill

### Trigger the Skill

Say any of these to activate the skill:
- "write captions for my posts"
- "caption these posts"
- "write voiceovers for my content"
- "I need captions for this week"
- "urgent post — write a caption"
- "something happened I need to post about"
- "write captions from my content calendar"

### Follow the 8-Step Workflow

1. **Identify source** (content-planner, uploaded file, Google Doc, or one-off)
2. **Select brand** (OutAtlas, Travel in Pride, or both)
3. **Choose platforms** (TikTok, Instagram, YouTube, Pinterest, LinkedIn, Reddit)
4. **Specify voiceover needs** (if any + preferred tone)
5. **Review captions** (get the full writeup before approval)
6. **Adjust as needed** (tweak tone, length, hashtags, CTA)
7. **Export to .docx** (get a branded, formatted document)
8. **Optional: Add to Notion** (creates tasks in your dashboard)

---

## Platforms Supported

| Platform | Captions | Voiceover |
|----------|----------|-----------|
| TikTok | ✅ | — |
| Instagram Reels | ✅ | ✅ |
| Instagram Feed | ✅ | ✅ |
| Instagram Stories | ✅ | — |
| YouTube Shorts | ✅ | ✅ |
| YouTube Long-form | ✅ | ✅ |
| Pinterest | ✅ | — |
| LinkedIn | ✅ | — |
| Reddit | ✅ | — |

---

## Key Features

✅ **Platform-specific formatting** — Each caption optimized for its platform's algorithm
✅ **Brand voice consistency** — Maintains OutAtlas or Travel in Pride voice
✅ **Voiceover scripts** — Ready-to-record or AI voiceover suggestions (ElevenLabs)
✅ **One-off urgent posts** — Get captions in minutes
✅ **Multi-post calendars** — Batch content across multiple platforms
✅ **SEO optimization** — YouTube/Pinterest captions built for search
✅ **.docx export** — Branded, formatted documents
✅ **CTA alignment** — Each CTA matches platform native behavior

---

## Platform Best Practices Built-In

The skill includes best practices for:
- **Hashtag counts** — 3-5 for TikTok, 8-15 for Instagram, 5-10 for Pinterest, etc.
- **Character limits** — Respects truncation points (150 chars for TikTok, 125 for Instagram, etc.)
- **CTA strategies** — Engagement CTAs for TikTok, "link in bio" for Instagram, soft CTAs for Pinterest
- **Posting times** — Optimal times for each platform
- **Algorithm drivers** — Understands what each platform prioritizes (saves, comments, watch time, keywords, etc.)
- **User psychology** — Tailored to each platform's user intent and behavior

---

## Customization Notes

The skill is pre-configured for:
- **OutAtlas** — Warm, knowledgeable, aspirational voice
- **Travel in Pride** — Celebratory, community-first, inclusive voice

To customize for your own brands:
1. Edit the "Brand Voice Reference" section in SKILL.md
2. Update brand color codes in the .docx export script
3. Adjust platform best practices if needed

---

## Troubleshooting

**Q: Skill doesn't appear after installation**
A: Try restarting Cowork or manually checking the skills directory. Verify the .skill file extracted correctly.

**Q: Captions feel too long/short**
A: The skill includes optimal character counts per platform. You can adjust in the review step before export.

**Q: Want different brand voice?**
A: Specify "more playful," "more professional," "more urgent," etc. during the workflow.

**Q: Need .docx export but don't have Python?**
A: The skill handles .docx export internally — you don't need to run the script manually. It's bundled as an optional tool.

**Q: What if I need captions for a different platform?**
A: The skill covers 9 platforms. For others (TikTok Shop, Threads, BeReal, etc.), you may need to request custom extensions.

---

## Support & Feedback

**Questions?**
- Refer to the `README.md` file in the skill package
- Check the SKILL.md for detailed workflow documentation
- Contact: inquiry@travelinpride.com

**Feature Requests?**
- Suggestions for platform additions
- New voiceover tones
- Custom export formats

**Bug Reports?**
- If captions don't follow platform best practices
- If brand voice is inconsistent
- If .docx export has formatting issues

---

## Next Steps

1. ✅ **Install the skill** using the instructions above
2. ✅ **Try a quick test** using one of the examples provided
3. ✅ **Review the captions** to make sure they meet your standards
4. ✅ **Export to .docx** for easy copy-paste to each platform
5. ✅ **Approve and post!**

---

## File Locations

**For reference:**

- **Skill File:** `/sessions/funny-practical-fermat/mnt/Content/caption-voiceover-writer.skill`
- **Extracted Directory:** `/sessions/funny-practical-fermat/mnt/Content/caption-voiceover-writer/`
- **Test Results:** `/sessions/funny-practical-fermat/mnt/Content/caption-voiceover-writer-workspace/iteration-1/`

---

## Version Information

**Skill Name:** caption-voiceover-writer
**Version:** 1.0
**Release Date:** March 28, 2026
**Status:** Production Ready

---

Happy caption writing! 🎉

For questions or support, reach out to inquiry@travelinpride.com
