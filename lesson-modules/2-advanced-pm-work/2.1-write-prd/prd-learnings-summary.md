# PRD Development Learnings & Insights

**Date:** Session learnings from Module 2.1
**Context:** AI Voice Task Creation feature for TaskFlow
**Questions Asked:** 2 critical product questions that revealed gaps in typical PRD templates

---

## Question 1: Detailed Design & Edge Cases

### The Question

> "Who does the detailed design, i.e. how many categories are we going to have on launch or is it completely AI discretion on how and which categories to create which might lead to a user having too many categories. Where are edge cases managed?"

### Why This Question Matters

This question revealed a critical gap in the PRD: **AI features need MORE product thinking, not less.** The original PRD said "Auto-categorizes based on keywords and user's historical patterns" but left ambiguous:
- Can AI create new categories autonomously?
- What happens when AI is uncertain?
- How does user maintain control?
- What are the boundaries of AI autonomy?

These are **strategic product decisions**, not just implementation details.

### The Answer: Three-Layer Documentation Approach

**Layer 1: PRD (Strategic Level)** - PM owns
- **WHAT** is the categorization philosophy?
  - Example: "Use existing categories only" vs. "AI can create new categories"
- **WHY** this approach?
  - Example: "Prevents category explosion, respects user's existing taxonomy, maintains user control"
- **SUCCESS** criteria
  - Example: "70% of voice tasks auto-categorized correctly"

**Layer 2: Product Spec (Tactical Level)** - PM + Designer create
- Detailed UI flows for all edge cases
- Wireframes showing what happens when AI is uncertain
- User controls: Can user override? Give feedback?
- Information hierarchy: Where does category appear in confirmation screen?

**Layer 3: Engineering Spec (Implementation Level)** - Engineering creates
- Exact ML model or rule-based logic
- Confidence score thresholds (e.g., ">70% confidence required")
- Performance requirements (e.g., "<500ms response time")
- Data models, APIs, storage

### What Should Be Added to PRDs for AI Features

**Section: "Key Product Decisions - AI Autonomy & Control"**

Should address:

1. **AI Autonomy Boundaries**
   - ✅ What AI CAN do autonomously
     - Example: "Auto-fill existing fields, suggest from existing categories"
   - ❌ What AI CANNOT do without user approval
     - Example: "Create new categories, assign to people, set priorities above 'High'"

2. **Uncertainty Handling**
   - What happens when AI confidence is low?
   - Default philosophy: transparent + user control vs. guess wrong
   - Example: "When confidence <70%, leave field blank rather than guess incorrectly"

3. **User Control Mechanisms**
   - Can users override AI decisions?
   - Can users provide feedback to improve AI?
   - How do users correct mistakes?

4. **Edge Case Philosophy**
   - Example for categorization:
     - New user with no categories → task uncategorized, prompt to create categories
     - Ambiguous task → uncategorized, no guess
     - Multiple possible categories → AI picks highest confidence, shows alternatives in UI

### Example Addition to PRD

```markdown
## AI Categorization Logic

**V1 Approach: Use Existing Categories Only**
- AI can ONLY assign tasks to categories the user has already created
- Does not create new categories autonomously
- If no clear match, task is left uncategorized (user can manually categorize later)
- Confidence threshold: >70% confidence required to auto-assign category

**Why this approach:**
- Prevents category explosion (100s of AI-invented categories)
- Respects user's existing taxonomy
- User maintains control over information architecture
- Reduces AI trust issues

**Edge Cases:**
- New user with no categories → task created uncategorized, prompt to create categories
- Ambiguous task ("work on the thing") → uncategorized, no guess
- Multiple possible categories → AI picks highest confidence, shows alternative in UI

**Success Metric:**
- 70% of voice-created tasks correctly auto-categorized
- <5% of users report "too many categories" in feedback
```

---

## Question 2: PRD Placement in Jira Hierarchy

### The Question

> "In the context of Jira would you say the Epic level should hold the PRD while the stories the tactical level Product spec?"

### Why This Question Matters

This shows understanding that **PRDs need to be actionable documents** that teams actually use, not just artifacts that sit in a folder. Where you put documentation affects:
- Who reads it
- How it's used during development
- How decisions get referenced
- How updates are communicated

### The Answer: Yes, Standard Hierarchy

**Epic Level (Strategic)** - PM owns
- **Attach:** Full PRD document
- **Epic Description:** 2-3 sentence summary of problem and solution
- **Business value:** Why building, revenue impact, strategic fit
- **Success metrics:** How we'll measure success
- **Timeline:** Target dates and milestones
- **Linkable:** Execs, sales, marketing can read Epic + PRD without wading through stories

**Story Level (Tactical)** - PM + Designer + Eng collaborate
- **Product Spec** (for design/UX stories): Detailed flows, wireframes, edge cases, user controls
- **Engineering Spec** (for technical stories): Architecture, API choices, data models, performance requirements
- **Acceptance Criteria:** Specific, testable conditions for "done"
- **Dependencies:** What must complete first

**Task Level (Implementation)** - Eng/Design execute
- Granular work items
- No additional docs - just code/designs

### Practical Example for Voice Feature

```
Epic: "Mobile Voice Task Creation"
├── PRD: ai-chat-todo-prd-final.md
├── Description: "Enable mobile users to create tasks via voice..."
├── Labels: mobile, ai, q1-priority
│
├─── Story 1: "Design voice capture and confirmation flow"
│    ├── Product Spec: Figma + edge case doc
│    │   - What if no internet connection?
│    │   - What does confirmation screen look like?
│    │   - How does user edit AI tasks?
│    ├── Acceptance Criteria:
│    │   ✅ Wireframes approved
│    │   ✅ 10 edge cases documented
│    │   ✅ Accessibility requirements met
│
├─── Story 2: "Implement AI categorization logic"
│    ├── Engineering Spec:
│    │   - Use existing categories only
│    │   - Confidence threshold >70%
│    │   - Vector similarity matching
│    ├── Acceptance Criteria:
│    │   ✅ 75% accuracy on test dataset
│    │   ✅ <500ms categorization time
│    │   ✅ Handles new user edge case
│
└─── Story 3: "Build voice capture (iOS)"
     ├── Engineering Spec: API selection, architecture
     └── Tasks: Research APIs, implement, test
```

### Why This Works

1. **PRD at Epic level** = Single source of truth for "why" and "what"
2. **Specs at Story level** = Detailed "how" that can be reviewed independently
3. **Stories reference PRD** = "Per PRD section 'Monetization', this is Pro-tier only"
4. **Clear ownership** = PM owns Epic/PRD, Designer owns Product Spec, Eng owns Eng Spec
5. **Right level of detail** = Execs read Epic, team members read relevant Stories

---

## Key Learnings Summary

### 1. AI Features Need Explicit Product Decisions

**Traditional feature PRDs can be vague about implementation** because designers and engineers figure out details.

**AI feature PRDs MUST be explicit** because AI autonomy affects:
- User trust
- Product complexity
- Edge case handling
- Long-term information architecture

**Add to every AI feature PRD:**
- AI autonomy boundaries (what can/can't AI do?)
- Uncertainty handling (what happens when AI doesn't know?)
- User control mechanisms (how can users override/correct?)
- Edge case philosophy (default to transparency vs. guessing)

### 2. Edge Cases Are Strategic Decisions, Not Implementation Details

**Wrong mindset:** "Engineering will figure out edge cases during implementation"

**Right mindset:** "PM defines edge case PHILOSOPHY, engineering implements it"

Example:
- **Philosophy (PRD level):** "When uncertain, default to user control rather than guessing wrong"
- **Implementation (Eng level):** "If confidence <70%, set field to null and display 'Unable to detect, please specify'"

### 3. Documentation Lives at Three Levels

| Level | Owner | Document Type | Purpose |
|-------|-------|---------------|---------|
| **Strategic** | PM | PRD | Why we're building, what success looks like |
| **Tactical** | PM + Designer + Eng | Product Spec, Eng Spec | How it works in detail, edge cases, flows |
| **Implementation** | Eng + Designer | Code, Designs | The actual built thing |

**Mistake:** Putting implementation details in PRD (too long, changes frequently)
**Mistake:** Not putting strategic decisions in PRD (team doesn't understand constraints)

### 4. PRDs Should Be Living Documents in Your Workflow

**PRDs aren't write-once artifacts** - they're referenced throughout development:
- Attached to Epic in Jira
- Linked from Stories when making decisions
- Updated when assumptions change (with changelog)
- Shared with stakeholders to communicate status

**If your PRD lives in Google Docs and nobody looks at it after kickoff, something is wrong.**

### 5. Template Matters - Standard Templates Miss AI-Specific Needs

**Lenny's PRD Template is great for traditional features** but lacks:
- AI autonomy and control decisions
- Edge case handling philosophy
- Success metrics specific to AI quality
- User trust considerations

**Conclusion:** Need an enhanced template for AI features (see next section)

---

## Recommendations for Refining PRDs

### For the Voice Feature PRD Specifically

**Add these sections to `ai-chat-todo-prd-final.md`:**

1. **"Key Product Decisions - AI Autonomy & Control"** (new section)
   - What AI can/cannot do autonomously
   - Categorization logic (existing categories only)
   - Edge case handling philosophy

2. **Enhanced Success Metrics** (update existing section)
   - Add: "AI categorization accuracy >70%"
   - Add: "<5% of users report 'too many categories'"
   - Add: "User override rate <15% (shows AI getting it right)"

3. **"Documentation Hierarchy"** (new appendix section)
   - Epic: This PRD
   - Stories: Product Specs for design, Eng Specs for technical
   - Link to Jira Epic: [URL]

### For Future AI Feature PRDs

**Always include:**
- AI autonomy boundaries section
- Edge case philosophy (not just edge case list)
- AI quality metrics (accuracy, confidence, override rate)
- User control mechanisms
- Trust-building considerations (transparency, explainability)

---

## Next Steps

1. **Update `ai-chat-todo-prd-final.md`** with "Key Product Decisions" section
2. **Create enhanced Lenny's template** for AI features (see `Lennys-PRD-Template-Enhanced.md`)
3. **When creating Jira Epic**, attach PRD and write 2-3 sentence description
4. **During story creation**, reference PRD sections for decisions ("Per PRD, we're using existing categories only")
5. **Track learnings** - after shipping, document what worked and what should change in template

---

## Reflection: What Made This PRD Process Successful

**✅ What worked:**
- Starting with Socratic questions to clarify thinking
- Generating 3 strategic approaches to compare
- Getting multi-angle feedback (eng, exec, UX) before socializing
- Iteratively refining based on feedback

**⚠️ What gaps emerged:**
- AI autonomy decisions weren't explicit initially
- Edge case philosophy was missing
- Didn't think about Jira workflow integration upfront

**💡 Key insight:**
AI features require PMs to be MORE opinionated and explicit, not less. Traditional features can rely on designer/eng judgment for many details. AI features need PM to define the boundaries, philosophy, and user control mechanisms upfront - otherwise team will make inconsistent decisions that erode user trust.

---

**This document captures key learnings from the PRD development process that should inform future PRD writing, especially for AI-powered features.**
