# Lenny's PRD Template - Enhanced for AI Features

*Enhanced version of [Lenny Rachitsky's PRD template](https://www.lennyrachitsky.com/) with additional sections for AI-powered features, edge case handling, and modern product development workflows.*

---

# [Project Title]

**One-sentence description:**
[What is this in 10 words or less?]

**Type:** [New Feature / Enhancement / Experiment / Infrastructure]
**Target Launch:** [Quarter/Month]
**Tier:** [Which pricing tier gets this? All / Pro / Enterprise]

---

## Description: What is it?

[2-3 sentences describing what you're building from the user's perspective]

**Core experience:**
[Describe the user journey in one sentence: User does X → System does Y → User achieves Z]

---

## Problem: What problem is this solving?

**Primary problem:**
[1-2 sentences describing the core user pain point]

**Evidence:**
- [Quantitative data: survey results, usage stats, churn reasons]
- [Qualitative data: user quotes, support tickets, sales feedback]
- [User quote example: "I can't do X because Y"]

**Secondary problems (if applicable):**
[Additional pain points this solves]

---

## Why: How do we know this is a real problem and worth solving?

**User evidence:**
- [% of users affected or requesting this]
- [Qualitative feedback themes]
- [Behavioral data showing the pain point]

**Business impact:**
- [Revenue opportunity or risk]
- [Strategic importance]
- [Competitive pressure]

**Why now?**
[What makes this urgent? Market timing? Competitive threat? Customer churn?]

---

## Success: How do we know if we've solved this problem?

**Primary success metrics:**
1. [Metric 1 with target: e.g., "Increase weekly active users by 25%"]
2. [Metric 2: e.g., "50% of users try feature within 30 days"]
3. [Metric 3: e.g., "Reduce churn by 0.5 percentage points"]

**Secondary metrics:**
- [Supporting metrics that indicate progress]
- [Quality metrics: e.g., "Error rate <5%"]

**For AI features, also include:**
- **AI quality metrics:** [e.g., "Accuracy >80%", "User override rate <15%"]
- **Trust metrics:** [e.g., "User satisfaction with AI >8/10"]

**Business metrics:**
- [Revenue impact: conversion, expansion, retention]
- [Cost savings or efficiency gains]

**Qualitative success signals:**
- [User testimonials themes]
- [Reduced support tickets about X]
- [Mentioned in win/loss sales analysis]

**Failure criteria:**
[What would make you consider this a failure? Be specific.]

---

## Audience: Who are we building for?

**Primary persona(s):**

**[Persona Name]** ([X%] of user base)
- [Key characteristic 1]
- [Key characteristic 2]
- [Job-to-be-Done: what are they hiring this feature to do?]
- [Current workaround or pain]

**[Persona Name 2]** ([X%] of user base)
[Repeat above]

**Not building for (V1):**
- [Users or use cases explicitly out of scope]

---

## What: Roughly, what does this look like in the product?

**Core user flow:**

1. **[Step 1]:** [What user does]
   - [What happens in the system]
   - [What user sees/experiences]

2. **[Step 2]:** [Continue the flow]

3. **[Step 3]:** [How it ends]

**Key features (V1):**
- [Feature 1 with brief description]
- [Feature 2]
- [Feature 3]

**What's NOT included in V1:**
- [Explicitly call out what's being deferred to V2]
- [Why: helps prevent scope creep and sets expectations]

---

## 🤖 AI Autonomy & Control *(For AI Features Only)*

*Include this section for any feature with AI/ML components*

**What AI can do autonomously:**
- ✅ [Example: "Auto-categorize using existing user categories"]
- ✅ [Example: "Suggest priorities based on keywords"]
- ✅ [Example: "Extract due dates from natural language"]

**What AI cannot do without user approval:**
- ❌ [Example: "Create new categories"]
- ❌ [Example: "Assign tasks to team members"]
- ❌ [Example: "Delete or archive items"]

**Handling uncertainty:**
- [Philosophy: What happens when AI confidence is low?]
- [Example: "If confidence <70%, leave field blank rather than guess incorrectly"]
- [How is confidence communicated to users?]

**User control mechanisms:**
- [How can users override AI decisions?]
- [How can users provide feedback to improve AI?]
- [Can users disable AI features?]

**Key edge cases:**
- [Edge case 1 and how it's handled]
- [Edge case 2 and how it's handled]
- [Philosophy: default to transparency and user control]

---

## How: What is the experiment plan?

**Launch strategy:**
[Beta → Gradual rollout → General availability? Or different approach?]

**Phase 1: [Name]** ([Timeline])
- [What happens in this phase]
- [Success criteria to proceed]

**Phase 2: [Name]** ([Timeline])
- [What happens in this phase]
- [Success criteria to proceed]

**Phase 3: General Availability** ([Timeline])
- [Full launch details]

**Key experiment questions:**
1. [Question 1 you're trying to answer with data]
2. [Question 2]
3. [Question 3]

**Success criteria to proceed:**
- [Specific metrics or signals needed to move forward]
- [What would make you stop or pivot?]

---

## When: When does it ship and what are the milestones?

**Target Launch:** [Date or Quarter]

**Key milestones:**

| Milestone | Date | Owner | Status |
|-----------|------|-------|--------|
| Design complete | [Date] | [Name] | 🔵 Not started |
| Eng complete | [Date] | [Name] | 🔵 Not started |
| Beta launch | [Date] | [Name] | 🔵 Not started |
| GA launch | [Date] | [Name] | 🔵 Not started |

**Dependencies:**
- [What needs to happen first? External dependencies?]
- [What could block or delay this?]

**Risks:**
- **[Risk 1]** → Mitigation: [How you'll address it]
- **[Risk 2]** → Mitigation: [How you'll address it]

---

## 💰 Monetization & Business Case *(Optional but Recommended)*

**Pricing tier:** [Which tier gets this feature?]

**Revenue model:**
- [How does this drive revenue? Conversion? Expansion? Retention?]
- [Expected impact: e.g., "15% of Starter users upgrade to Pro within 90 days"]

**Projected impact:**
- [Revenue impact in Year 1: $XXk ARR]
- [Cost to build: $XXk]
- [ROI: positive in Month X]

**How this supports company goals:**
- [Link to OKRs or strategic initiatives]
- [Why this is the right thing to build NOW]

---

## 📋 Documentation & Workflow *(Optional but Useful)*

**Where this lives:**
- **Jira Epic:** [Link to epic]
- **Design:** [Link to Figma/design files]
- **Specs:** [Links to detailed Product Specs or Eng Specs]

**Related documents:**
- [User research reports]
- [Competitive analysis]
- [Technical architecture docs]

**Changelog:**
[Track major changes to this PRD]

| Date | Change | Author |
|------|--------|--------|
| [Date] | [What changed and why] | [Name] |

---

## 🔮 V2 Roadmap Preview *(Optional)*

**Future enhancements (post-V1):**
- [Feature idea 1 that builds on V1]
- [Feature idea 2]
- [Why these are V2, not V1]

---

## Appendix: Open Questions & Decisions Needed

**Open questions:**
- [ ] [Question 1 that needs answering before proceeding]
- [ ] [Question 2]

**Decisions needed:**
- [ ] [Decision 1 with options and recommendation]
- [ ] [Decision 2]

**Assumptions:**
- [Key assumption 1 that could change]
- [Key assumption 2]

---

## Key Differences from Original Lenny's Template

**Added sections:**
1. **🤖 AI Autonomy & Control** - Critical for AI features to define boundaries and edge cases
2. **💰 Monetization & Business Case** - Makes business impact explicit
3. **📋 Documentation & Workflow** - Links PRD to actual development (Jira, specs)
4. **Changelog** - Tracks how PRD evolves over time
5. **Enhanced Success section** - Separates user metrics, AI metrics, and business metrics

**Enhanced existing sections:**
- **Audience** - Added "Job-to-be-Done" framing
- **What** - Added explicit "What's NOT in V1" to prevent scope creep
- **Success** - Added failure criteria and qualitative signals

**Philosophy:**
- Original template is great for early-stage, fast-moving features
- Enhanced version adds rigor for AI features, complex products, and cross-functional alignment
- Still maintains Lenny's minimalist spirit - only add sections you need

---

## When to Use Original vs. Enhanced Template

**Use Original Lenny's Template when:**
- ✅ Small feature or experiment
- ✅ Early-stage product or startup
- ✅ Want to move extremely fast
- ✅ No AI/ML components
- ✅ Simple monetization model

**Use Enhanced Template when:**
- ✅ AI-powered features (need autonomy & edge case sections)
- ✅ Enterprise or complex products
- ✅ Need to align exec, eng, design, sales
- ✅ Explicit monetization strategy required
- ✅ Integration with Jira/agile workflow

**Best practice:** Start with original template, add enhanced sections only as needed.

---

*Template credit: Original by [Lenny Rachitsky](https://www.lennyrachitsky.com/). Enhanced by [Your Name] based on learnings from AI feature development.*
