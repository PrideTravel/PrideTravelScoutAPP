---
name: outatlas-blog
description: "Write 3300-4000 word Destination and Event Planning Guides for OutAtlas with GEO optimization and AI search visibility. CRITICAL: ONLY include venues already verified in the OutAtlas app. Features question-based headlines for AI citations, individual venue flagging with direct app verification links, separate ⚠️ PENDING YOUR APPROVAL section for non-app venues, corporate pride-washing detection and exclusion, strict copy+paste text format workflow with stop-if-unclear protocol, regional keyword optimization, 3-5 images, mega-modal forms, and 5-step approval workflow. Every venue requires individual user approval before inclusion. Event guides include dates, hotels, bars, restaurants, stores, weather. Use for comprehensive travel guides, destination content, and LGBTQ+ travel planning guides for OutAtlas/Travel in Pride."
---

# OutAtlas Blog Skill — Destination & Event Planning Guides with STRICT VENUE VERIFICATION

Write comprehensive, well-researched Destination and Event Planning Guides for www.outatlas.com in a conversational, friend-like brand voice. This skill handles destination deep-dives and event-specific planning content from research through multi-format delivery, including GEO optimization for AI citations, question-based headlines, image sourcing, and a structured discovery review workflow for new LGBTQ+ venues.

## ⚠️ CRITICAL VENUE VERIFICATION REQUIREMENT

**THE GUIDE CANNOT INCLUDE VENUES NOT ALREADY VERIFIED IN THE OUTATLAS APP.**

This is the single most important rule. Every hotel, bar, restaurant, store, tour, or other venue included in the final blog post MUST:
1. Already exist in the OutAtlas app database
2. Be individually flagged with a direct OutAtlas app link in the guide
3. Be explicitly approved by the user BEFORE inclusion
4. Be screened for corporate pride-washing (major chains doing performative LGBTQ+ support without genuine commitment)

If a venue is NOT in the app:
- Flag it separately in a **⚠️ PENDING YOUR APPROVAL** section
- Do NOT include it in the main blog content
- Present it for user approval with a direct link to where they can review/add it
- Wait for explicit user confirmation before adding to the guide

---

## Overview

The OutAtlas Blog skill creates professional, in-depth travel planning guides optimized for both human readers and AI search systems:

**Destination Planning Guides (3300-4000 words)**
- Geographic focus on LGBTQ+ destinations with regional keyword optimization
- Coverage of 2-3 major events with separate weather info for each
- Peak vs. off-peak travel analysis
- Recommended hotels with USD pricing (ONLY app-verified venues)
- Budget breakdown and money-saving strategies
- Packing recommendations
- LGBTQ+ legal status via Equaldex research
- Official tourism & LGBTQ+ resources
- Headlines converted to questions where beneficial for AI sources
- Natural split point at ~1600 words for content distribution

**Event Planning Guides (3300-4000 words)**
- Comprehensive event planning information collected via mega-modal form
- Event dates and timing
- Hotel recommendations with USD pricing (ONLY app-verified venues)
- Bar/club recommendations (ONLY app-verified venues)
- Restaurant recommendations (ONLY app-verified venues)
- Shopping/store recommendations (ONLY app-verified venues)
- Weather information
- Budget planning and cost breakdowns
- Packing recommendations
- LGBTQ+ legal status via Equaldex research
- Official event & tourism resources
- Headlines converted to questions where beneficial for AI sources
- Natural split point at ~1600 words for content distribution

**New: Strict Discovery Review Workflow with Venue Verification**
- During research, any LGBTQ+ hotels, bars, restaurants, or stores discovered are cross-checked against the OutAtlas app database
- Venues found in the app are flagged with direct app links and presented for individual user approval
- Venues NOT found in the app are presented separately in a **⚠️ PENDING YOUR APPROVAL** queue with sources
- Only venues approved by the user are written into the final guide, with app links embedded
- Corporate pride-washing companies (major chains with performative but not genuine LGBTQ+ support) are excluded
- Copy+paste text data is processed strictly — if the format cannot be read or understood, the process stops and the user is notified

Each blog post follows a 5-step approval-driven workflow to ensure research quality, GEO optimization, image sourcing, discovery vetting, brand alignment, and stakeholder approval before writing begins.

---

## The 5-Step Workflow

### Step 1: Gather Requirements & Interactive Popups

Ask the user to select their guide type first:

**"Are you creating a Destination Planning Guide or an Event Planning Guide?"**

---

#### FOR EVENT PLANNING GUIDES — Complete Mega-Modal (ALL Questions at Once)

**Present EVERY field in ONE complete popup modal.** No sequential forms. No accidental submissions. Answer all questions in one place.

After form submission, present this CRITICAL INSTRUCTION before proceeding:

**⚠️ VENUE DATA FORMAT REQUIREMENT:**

If you will provide venue data via copy+paste text, confirm:
- Format will be: plain text, line-by-line list, or structured table
- If format cannot be read or understood, Claude will STOP and ask for clarification
- User will review and approve venues INDIVIDUALLY before they are added to the guide
- Only venues already in the OutAtlas app (or approved by user for app addition) will be included

---

#### FOR DESTINATION PLANNING GUIDES — Complete Mega-Modal (ALL Questions at Once)

**Present EVERY field in ONE complete popup modal.** No sequential forms. No accidental submissions. Answer all questions in one place.

After form submission, present this CRITICAL INSTRUCTION before proceeding:

**⚠️ VENUE DATA FORMAT REQUIREMENT:**

If you will provide venue data via copy+paste text, confirm:
- Format will be: plain text, line-by-line list, or structured table
- If format cannot be read or understood, Claude will STOP and ask for clarification
- User will review and approve venues INDIVIDUALLY before they are added to the guide
- Only venues already in the OutAtlas app (or approved by user for app addition) will be included

---

### Step 2: Research & Analysis Phase with APP VERIFICATION

Conduct thorough research for credible sources, geographic optimization, pricing, and image sourcing:

**CRITICAL: App Database Cross-Reference (NEW)**

For every venue discovered during research (hotels, bars, restaurants, stores, tours):
1. Check if the venue exists in the OutAtlas app
2. If it exists: Note the app link, star the venue for individual approval
3. If it does NOT exist: Flag for **⚠️ PENDING YOUR APPROVAL** section
4. Exclude any company/venue known for corporate pride-washing (e.g., major chains with performative LGBTQ+ marketing but no genuine commitment)

**Corporate Pride-Washing Detection**
- Major chains doing token LGBTQ+ support without genuine commitment
- Example: Large retail chains that host Pride sales but oppose LGBTQ+ rights in their operations
- Solution: Prefer independently-owned venues, local businesses, and companies with authentic LGBTQ+ leadership and values
- Flag if uncertain — let user make the final call

**Copy+Paste Text Processing Protocol**
- If user provides venue data via copy+paste, process exactly as provided
- If format is unclear, inconsistent, or cannot be parsed: STOP immediately
- Present the data back to the user and ask for clarification
- Do NOT guess or fill in gaps
- Wait for user confirmation before proceeding

**Web Search** (5-10 searches per guide type)

For Destination Guides:
- "[City] tourism," "[City] LGBTQ+ scene," "[City] events 2026"
- "[City] hotels LGBTQ+ friendly," "[City] bars nightlife," "[City] restaurants"
- "[City] weather [season]," "[City] what to pack," "[City] safety"
- "Equaldex [Country]" for LGBTQ+ legal info
- "[Event name] dates schedule," "[Event] travel guide"

For Event Guides:
- "[Event name] 2026 dates," "[Event] schedule itinerary"
- "[Event location] hotels," "[Event city] bars clubs," "[Event city] restaurants"
- "[Event] weather," "[Event] what to pack"
- "[Event location] shopping," "[Event] LGBTQ+ legal"
- "[Event] official website," "[Event] travel guide"

**Peak vs. Off-Peak Research** (Destination Guides only)
- Identify peak travel seasons (highest prices, most crowds)
- Research shoulder seasons and off-peak advantages
- Document cost comparisons and crowd levels
- Provide recommendations based on budget/preference

**Hotel Pricing Research** (CRITICAL)
- Research 3-5 hotels from user input
- **ALWAYS provide pricing in USD** (convert if necessary)
- Include star rating, LGBTQ-friendly features, location details
- Provide price range (budget, moderate, luxury options)
- Note LGBTQ-specific perks or recognition
- **VERIFY each hotel exists in OutAtlas app**

**GEO-Specific Deep Research** (MANDATORY)
- Deep dive into LGBTQ+ scene, safety, attractions, vibe
- Search: "[City] LGBTQ+ community," "[City] gay scene 2026," "[City] Pride events"
- "[Destination] LGBTQ+ safety index," "[Country] laws for LGBTQ+ travelers"
- "[City] gay bars," "[City] LGBTQ+ neighborhoods," "[Destination] queer culture"
- Gather 2-4 geo-specific statistics
- Identify LGBTQ+ landmarks, bars, neighborhoods, hidden gems
- Document seasonal factors and climate considerations
- **Cross-reference all discoveries against OutAtlas app**

**Equaldex Integration** (ALL GUIDES - MANDATORY)
- Research destination/event country on Equaldex (equaldex.com)
- Document legal status: same-sex marriage, adoption, legal protections
- Note healthcare access and discrimination protections
- Include travel warnings if applicable
- This becomes a dedicated guide section

**Source Gathering** (8-15 sources per guide)
- Identify credible sources: tourism boards, LGBTQ+ guides, safety resources, hotels, restaurants, bars, events, legal resources
- Verify all facts before inclusion
- Note specific placement for each source
- **Prioritize local/regional sources** for GEO optimization
- Record OutAtlas app links for all verified venues

**Image Sourcing** (3-5 images per guide)
- Hero image (destination/event landmark or celebration)
- Event/attraction imagery (parade, festival, venue)
- Hotel/accommodation imagery
- Nightlife/bar imagery
- Dining/restaurant imagery
- Neighborhood/street imagery
- Search Unsplash, Pexels, Pixabay with GEO keywords
- Source with **DIRECT DOWNLOAD LINKS**
- Create Image Pack Summary with: filename, description, platform, download link, placement, alt text with geo keywords

**Internal Linking** (3-5 links)
- Link destination names to OutAtlas guides
- Link event names to OutAtlas resources
- Link LGBTQ+ topics to app features
- Suggest natural placement

**Compile Research Summary for Step 3:**
- GEO Focus Overview
- Peak vs. Off-Peak Analysis (Destination only)
- Image Pack Summary with download links
- All sources with placements and app links
- GEO keywords identified
- Hotel pricing in USD (app-verified only)
- Equaldex findings summary
- **CRITICAL: Discovery Review List** — ALL venues found during research, separated by: (A) In OutAtlas app, (B) NOT in app (pending approval), (C) Excluded for corporate pride-washing

---

### Step 2.5: Discovery Review with Individual Venue Flagging [CRITICAL APPROVAL REQUIRED]

**After completing research, present ALL discovered LGBTQ+ venues** in THREE CATEGORIES:

```
🏨 VENUES VERIFIED IN OUTATLAS APP — READY FOR APPROVAL

Below are venues discovered during research that ARE ALREADY in the OutAtlas app.
Review each one and confirm which you'd like to INCLUDE in the blog post.

═══════════════════════════════════════════════════════════════

**CATEGORY: Hotels**

📍 VENUE #1: [Name]
   Address: [Full address]
   Price Range: [Budget/Mid/Luxury]
   LGBTQ+ Features: [Recognition, events, staff diversity, etc.]
   ✓ VERIFIED IN OUTATLAS APP
   Link: [Direct OutAtlas app link]
   Source: [Verification URL]

   📋 YOUR DECISION:
   ☐ APPROVE — Include in blog post with app link
   ☐ SKIP — Don't include this time

[Repeat for each app-verified venue]

═══════════════════════════════════════════════════════════════

**CATEGORY: Bars & Clubs**

📍 VENUE #2: [Name]
   Address: [Full address]
   Specialties: [What they offer]
   LGBTQ+ Features: [Recognition, events, staff diversity, etc.]
   ✓ VERIFIED IN OUTATLAS APP
   Link: [Direct OutAtlas app link]
   Source: [Verification URL]

   📋 YOUR DECISION:
   ☐ APPROVE — Include in blog post with app link
   ☐ SKIP — Don't include this time

[Repeat for each app-verified venue]

═══════════════════════════════════════════════════════════════

**CATEGORY: Restaurants**

[Same format as above]

═══════════════════════════════════════════════════════════════

**CATEGORY: Stores/Shopping**

[Same format as above]

═══════════════════════════════════════════════════════════════
```

Then present non-app venues:

```
⚠️ VENUES NOT YET IN OUTATLAS APP — PENDING YOUR APPROVAL

These venues were discovered during research but are NOT currently in the OutAtlas app.
You can decide to:
(A) Add to blog post AND approve for app inclusion (Claude adds to app, then to blog)
(B) Skip entirely (Claude won't include)

═══════════════════════════════════════════════════════════════

**CATEGORY: Hotels**

⚠️ VENUE #1: [Name]
   Address: [Full address]
   Price Range: [Budget/Mid/Luxury]
   LGBTQ+ Features: [Recognition, events, staff diversity, etc.]
   ❌ NOT IN OUTATLAS APP (yet)
   Discovery Source: [URL where venue was found]

   📋 YOUR DECISION:
   ☐ APPROVE — Add to blog AND approve for app inclusion
   ☐ SKIP — Don't include this venue

[Repeat for each non-app venue]

═══════════════════════════════════════════════════════════════
```

Then present exclusions:

```
🚫 VENUES EXCLUDED — Corporate Pride-Washing Detection

These venues were found during research but are excluded because they appear
to engage in corporate pride-washing (performative LGBTQ+ support without
genuine commitment):

═══════════════════════════════════════════════════════════════

📍 EXCLUDED: [Name]
   Reason: [Major chain | Performative marketing only | Contradicts LGBTQ+ values in operations]
   Details: [Specific examples]

[Repeat for each excluded venue]

═════════════════════════════════════════════════════════════════

Feel free to override these exclusions if you disagree — your call.
```

**Why this structure exists:**
- Every venue in the final blog must be individually approved by you
- App-verified venues are flagged with direct links for easy reference
- Non-app venues are presented separately so you can decide if they should be added
- Corporate pride-washing is flagged so authentic LGBTQ+ businesses are prioritized
- Prevents unvetted or performative venues from being promoted

Proceed to Step 3 only after:
1. Approving all app-verified venues to include
2. Deciding on non-app venues (approve for app + blog, or skip)
3. Confirming exclusions are appropriate

---

### Step 3: Present Outline & Recommendations [APPROVAL REQUIRED]

Present to user in this exact order:

#### 🌍 GEO FOCUS (HIGHLIGHTED FIRST)
**Geographic Target: [City/Region/Event Name]**
- Geographic scope and significance for LGBTQ+ travelers
- Why relevant to topic and audience
- Key regional characteristics (climate, event calendar, LGBTQ+ scene, safety, community strength)
- How OutAtlas serves this geographic area
- Regional keywords for SEO optimization
- **AI Search Keywords:** Primary question phrases for AI citations (e.g., "What are the best LGBTQ+ destinations in [Region]?")

---

#### 📊 RESEARCH SUMMARY (APP-VERIFIED VENUES ONLY)

**Peak vs. Off-Peak Analysis** (Destination Guides only)
- Peak season: [months], characteristics, pricing, crowds
- Off-peak season: [months], advantages, cost savings
- Best times to visit for events
- Travel recommendations by budget

**Hotel Pricing & Recommendations** (ONLY APP-VERIFIED)
```
RECOMMENDED HOTELS (USD Pricing — ALL VERIFIED IN OUTATLAS APP)
- Hotel #1: [Name] — ⭐⭐⭐⭐ — $[price/night] — [LGBTQ features] — Link: [App link]
- Hotel #2: [Name] — ⭐⭐⭐ — $[price/night] — [Features] — Link: [App link]
- Hotel #3: [Name] — ⭐⭐ — $[price/night] — [Budget features] — Link: [App link]
```

**Equaldex Legal Status Summary**
- Summary of LGBTQ+ rights
- Key protections and legal status
- Any travel considerations or warnings

---

#### 1. Search Intent Analysis (UPDATED FOR AI OPTIMIZATION)
What travelers are searching for + how AI systems cite content about this destination/event:
- "People searching for '[Event]' want: dates, things to do, where to stay, safety info"
- "Searchers for '[Destination]' want: LGBTQ+ friendly spots, weather, costs, packing tips"
- "AI systems cite blog posts as authoritative when they answer these questions with specifics"

#### 2. Outline Structure (WITH VENUE VERIFICATION FLAGS)

**Outline of blog sections** with:
- Section titles
- Estimated word count per section
- **Venues to include** (ONLY those approved in Step 2.5) with app links
- Key points per section
- Image placements

Example:
```
OUTLINE — NYC Pride 2026 Event Planning Guide (3,300-4,000 words)

Section 1: Why NYC Pride Matters (400 words)
- Historical significance
- Modern celebration
- What to expect

Section 2: Before You Go (500 words)
- Planning timeline
- Budget breakdown

Section 3: Where to Stay (600 words)
- Hotels (ONLY APP-VERIFIED):
  * [Hotel Name] — [App link] ✓
  * [Hotel Name] — [App link] ✓
- Price comparisons
- Neighborhoods

Section 4: Where to Eat & Drink (700 words)
- Restaurants (ONLY APP-VERIFIED):
  * [Restaurant Name] — [App link] ✓
  * [Restaurant Name] — [App link] ✓
- Bars & clubs (ONLY APP-VERIFIED):
  * [Bar Name] — [App link] ✓

Section 5: Shopping & Experiences (500 words)
- Stores (ONLY APP-VERIFIED):
  * [Store Name] — [App link] ✓

Section 6: Practical Info (400 words)
- Weather & packing
- Safety & legal info
- Getting around

Section 7: Money-Saving Tips & Budget Guide (300 words)
- Cost breakdown
- Discounts

Section 8: Closing Narrative (300 words)
- Why Pride matters
- What to expect emotionally
```

#### 3. Image Pack Summary
- All sourced images with download links
- Placement in guide sections
- Alt text with geo keywords

#### 4. Sources & Citations
- All 8-15+ sources with placements
- OutAtlas app links for venues
- Equaldex reference
- Tourism resources
- Safety & legal resources

#### 5. SEO & AI Optimization Checklist
- Question-based headlines identified
- AI citation opportunities highlighted
- Geo keywords placed
- Internal linking suggestions
- FAQ opportunities noted

---

### Step 4: User Approval of Outline [CRITICAL]

Wait for explicit user confirmation on:
1. "Does the outline structure work?"
2. "Are all approved venues included?"
3. "Are there any sections to add/remove?"
4. "Any changes to SEO focus or keywords?"

**CRITICAL GATE:** Only proceed to Step 5 after outline approval.

---

### Step 5: Write Final Blog Post

Write the complete 3,300-4,000 word guide using:
- Approved outline structure
- ONLY app-verified venues (flagged with OutAtlas links in blog text)
- Question-based headlines where appropriate for AI optimization
- GEO keywords naturally integrated
- Conversational, friend-like brand voice
- Image placements as mapped in outline

**Output formats:**
1. .docx file (professional formatting with tables, colors, headers)
2. .html file (responsive, standalone, mobile-optimized)
3. Copy+paste ready text version

---

## Critical Notes

- **NO venues outside the OutAtlas app** should be in the final guide without explicit user approval and app link
- **Every venue must be individually flagged** with a direct OutAtlas app link
- **Corporate pride-washing companies are excluded** by default
- **Copy+paste text must be readable** — if not, the process stops for clarification
- **User approval is required at every step** before proceeding
- **App links are embedded in the guide text** so readers can discover venues in OutAtlas

---

## Brand Voice & Tone

- Conversational, friend-like, warm
- Informative without being overwhelming
- Celebratory of LGBTQ+ culture and community
- Practical and budget-conscious
- Inclusive and welcoming
- Authentic commitment to LGBTQ+ values (no corporate speak)

---

## Resources

- **OutAtlas app** — Primary venue database and verification source
- **Unsplash, Pexels, Pixabay** — Free image sourcing
- **Equaldex.com** — LGBTQ+ legal status research
- **Tourism boards** — Geographic research
- **LGBTQ+ travel guides** — Community insights
- **Weather services** — Climate and packing data
