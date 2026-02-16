# Level 2 Reference Guide: Advanced PM Work

**Status:** In Progress (Module 2.2 complete, Module 2.3 coming soon)
**Last Updated:** February 15, 2026
**Next Update:** After completing Module 2.3

---

## Table of Contents

1. [Level 2 Overview](#level-2-overview)
2. [Module 2.1: Write a PRD](#module-21-write-a-prd)
3. [Module 2.2: Analyze Data](#module-22-analyze-data)
4. [Module 2.3: Product Strategy](#module-23-product-strategy)
5. [Quick Reference: PM Workflows](#quick-reference-pm-workflows)
6. [Advanced Patterns](#advanced-patterns)
7. [Time-Saving Techniques](#time-saving-techniques)

---

## Level 2 Overview

### What You're Learning

Level 2 applies the Claude Code fundamentals from Level 1 to real Product Management workflows:

**Module 2.1: Write a PRD**
- Generate comprehensive Product Requirements Documents
- Transform research into structured specs
- Create user stories and acceptance criteria
- Build technical specifications with engineering input

**Module 2.2: Analyze Data**
- Process quantitative and qualitative data
- Generate insights from analytics
- Create data-driven recommendations
- Build executive dashboards and reports

**Module 2.3: Product Strategy**
- Develop product roadmaps
- Prioritize features and initiatives
- Create strategic frameworks (RICE, ICE, Value vs Effort)
- Build competitive positioning strategies

### Prerequisites

Before starting Level 2, you should have completed:
- ✅ Level 1 (Modules 1.1-1.7)
- ✅ Understanding of @ file references
- ✅ Familiarity with agents and sub-agents
- ✅ Knowledge of CLAUDE.md project memory
- ✅ Comfort with input modes (edit, auto-accept, plan)

### What Makes Level 2 Different

| Level 1 | Level 2 |
| --- | --- |
| Learning **mechanics** | Applying to **real PM work** |
| Individual skills | **End-to-end workflows** |
| Simple transformations | **Complex multi-step processes** |
| Generic examples | **Realistic scenarios** from TaskFlow |
| Building foundation | **Delivering outputs** you'd ship to stakeholders |

---

## Module 2.1: Write a PRD

### What You'll Learn

✅ Structure and components of a comprehensive PRD
✅ Transforming research into product requirements
✅ Creating user stories with acceptance criteria
✅ Building technical specifications
✅ Generating multiple PRD formats (1-pager, full spec, tech spec)
✅ Using sub-agents for multi-perspective reviews

### PRD Components Covered

**Core Sections:**
- Executive Summary
- Problem Statement
- Goals & Success Metrics
- User Personas & Use Cases
- User Stories
- Functional Requirements
- Technical Requirements
- Acceptance Criteria
- Timeline & Milestones
- Dependencies & Risks

**Advanced Sections:**
- Competitive Analysis
- Go-to-Market Strategy
- Analytics Plan
- Open Questions

### Key Workflows (Module 2.1)

**Coming soon after module completion**

---

## Module 2.2: Analyze Data

### What You'll Learn

✅ **Phase 1: Problem Discovery**
- Funnel analysis to identify critical drop-offs
- Survey data analysis and theme extraction
- Qualitative + quantitative data synthesis
- Creating problem analysis documents

✅ **Phase 2: Impact Estimation**
- Impact estimation framework: `Impact = Users Affected × Current Rate × Lift × Value per Action`
- Building ROI models with realistic assumptions
- Multi-scenario planning (pessimistic/realistic/optimistic)
- LTV calculations and revenue modeling

✅ **Phase 3: Experiment Analysis**
- A/B test result interpretation
- Statistical significance (p-values, confidence intervals)
- **Critical skill:** Segmentation analysis (never stop at topline!)
- Quality metrics vs quantity metrics
- Leading indicators and predictive metrics
- Creating experiment readout documents

### Key Workflows (Module 2.2)

**1. Problem Discovery Workflow**
```
Read funnel data → Identify drop-off points → Read qualitative data →
Extract themes → Synthesize insights → Create problem analysis doc
```

**2. Impact Estimation Workflow**
```
Define users affected → Calculate current baseline → Estimate lift →
Calculate value per action → Model scenarios → Build ROI model
```

**3. Experiment Analysis Workflow**
```
Analyze topline results → Segment by target customer →
Analyze quality metrics → Check leading indicators →
Make segment-specific recommendation
```

### Deliverables Created (Module 2.2)

**Example documents from TaskFlow activation case:**
- `activation-problem-analysis.md` - Problem validation with funnel + survey data
- `guided-onboarding-roi-scenarios.md` - Three-scenario business case
- `guided-onboarding-experiment-readout.md` - Full A/B test analysis with segment-specific recommendation

### Critical Lessons Learned

**🎯 Always Segment Before Deciding**
- Topline metrics can hide massive wins (or losses) in specific segments
- Example: +2.6pp topline hid +10.75pp lift for target segment
- Always analyze your target customer segment separately

**📊 Quality Metrics Matter as Much as Quantity**
- Don't just measure if users activate - measure how engaged they are
- Track retention, engagement, template usage, invites
- Quality metrics predict long-term value

**🔢 Multi-Scenario Planning Reduces Risk**
- Single-point estimates are dangerous (hide uncertainty)
- Three scenarios show range of outcomes (pessimistic/realistic/optimistic)
- Helps leadership understand risk/reward trade-offs

---

## Module 2.3: Product Strategy

### What You'll Learn

*Module content coming after Module 2.2 completion*

### Key Workflows (Module 2.3)

**Coming soon**

---

## Quick Reference: PM Workflows

### PRD Creation Workflow

**Coming soon after Module 2.1**

### Data Analysis Workflow

**End-to-End Data-Driven Decision Making**

**Step 1: Problem Discovery**
```bash
# Analyze quantitative data (funnels, metrics)
"Analyze @funnel-data.csv and identify where users drop off"

# Analyze qualitative data (surveys, feedback)
"Analyze @survey-responses.csv and extract the top themes"

# Synthesize insights
"Create a problem analysis document combining funnel data and survey insights"
```

**Step 2: Impact Estimation**
```bash
# Build impact model
"Using @impact-estimation-framework.md, estimate the ROI of solving this problem"

# Create scenarios
"Create three scenarios (pessimistic/realistic/optimistic) showing range of outcomes"
```

**Step 3: Experiment Analysis**
```bash
# Analyze results
"Analyze @experiment-results.csv and calculate activation lift"

# Segment by target customer
"Segment the results by company size - how does it perform for small teams vs enterprise?"

# Create readout
"Create an experiment readout document with segment-specific recommendation"
```

**Key Prompts for Data Analysis:**
- "What's the biggest drop-off in this funnel?"
- "Extract the top 3-5 themes from this survey data"
- "Build an ROI model using the impact estimation framework"
- "Create pessimistic, realistic, and optimistic scenarios"
- "Segment these A/B test results by [customer type]"
- "Is this result statistically significant?"

### Strategy Development Workflow

**Coming soon after Module 2.3**

---

## Advanced Patterns

### Pattern 1: Research → PRD Pipeline

**Coming soon**

### Pattern 2: Data → Insights → Strategy

**From Raw Data to Actionable Decisions**

**Step 1: Process Raw Data**
- Use Claude to analyze CSV files with thousands of rows
- Extract patterns from qualitative feedback (surveys, interviews)
- Calculate statistical significance and confidence intervals

**Step 2: Generate Insights**
- Identify the "so what?" - why does this data matter?
- Connect quantitative metrics to qualitative user pain points
- Segment by customer type to find hidden patterns

**Step 3: Build Business Case**
- Estimate impact using frameworks
- Model multiple scenarios to show risk/reward
- Calculate ROI with realistic assumptions

**Step 4: Make Recommendation**
- Clear decision based on data (ship/iterate/kill)
- Segment-specific rollout strategy if needed
- Define success metrics for monitoring

**Example: TaskFlow Activation Analysis**
- **Data:** Funnel shows 60% drop-off, survey shows "blank canvas" confusion
- **Insight:** Users need examples, not just empty projects
- **Business Case:** 28.3x ROI over 3 years (realistic scenario)
- **Recommendation:** Ship guided onboarding to small teams, exclude enterprise

### Pattern 3: Multi-Stakeholder Communication

**Coming soon**

---

## Time-Saving Techniques

### Technique 1: Parallel Research & Writing

**Coming soon**

### Technique 2: Template Reuse & Customization

**Coming soon**

### Technique 3: Sub-Agent Review Workflows

**Coming soon**

---

## Common PM Deliverables

### PRD Templates

**Location:** `lesson-modules/2-advanced-pm-work/2.1-write-prd/prd-templates/`

You have 4 different PRD templates to choose from, each with different strengths:

#### Quick Comparison Table

| Template | Complexity | Best For | Key Strength |
| --- | --- | --- | --- |
| **Lenny's (Original)** | ⭐ Minimal | Small features, experiments, startups | Speed - get ideas on paper fast |
| **Lenny's Enhanced** | ⭐⭐⭐ Moderate | AI features, complex products | AI-specific sections + monetization |
| **Carl's Template** | ⭐⭐⭐⭐ Comprehensive | Large features, stakeholder alignment | Problem/solution separation |
| **Tania's Spec Template** | ⭐⭐⭐⭐⭐ Very Detailed | FinTech, regulated industries, QA-heavy | Customer feedback + testing focus |

#### Template 1: Lenny's PRD Template (Original)

**Author:** Lenny Rachitsky
**File:** `Lennys-PRD-Template.md`

**Philosophy:** Answer 7 essential questions, nothing more. Optimized for speed and clarity.

**Sections:**
1. Description - What is it?
2. Problem - What problem is this solving?
3. Why - How do we know this is a real problem?
4. Success - How do we know if we've solved it?
5. Audience - Who are we building for?
6. What - What does this look like?
7. How - What is the experiment plan?
8. When - When does it ship?

**Use when:**
- ✅ Small feature or quick experiment
- ✅ Early-stage product or startup
- ✅ Need to move extremely fast
- ✅ Simple problem with clear solution
- ✅ Small team that doesn't need heavy process

**Skip when:**
- ❌ Need to align execs across departments
- ❌ Complex technical implementation
- ❌ AI/ML features with edge cases
- ❌ Regulated industry requiring detailed specs

---

#### Template 2: Lenny's PRD Template - Enhanced

**Author:** Lenny Rachitsky (enhanced version)
**File:** `Lennys-PRD-Template-Enhanced.md`

**Philosophy:** Lenny's minimalist spirit + sections for AI features, monetization, and cross-functional alignment.

**Additional sections beyond original:**
- 🤖 **AI Autonomy & Control** - What AI can/cannot do autonomously, edge cases, user control
- 💰 **Monetization & Business Case** - Pricing tier, revenue model, projected impact
- 📋 **Documentation & Workflow** - Links to Jira, Figma, related docs
- **Changelog** - Track how PRD evolves over time
- **V2 Roadmap Preview** - Future enhancements post-V1

**Use when:**
- ✅ AI-powered features (critical: need autonomy boundaries)
- ✅ Need explicit monetization strategy
- ✅ Integration with Jira/agile workflow
- ✅ Want structured changelog tracking
- ✅ Building for multiple personas with different needs

**Skip when:**
- ❌ Want absolute minimalism (use original Lenny's)
- ❌ No AI components and simple monetization
- ❌ Pre-product-market-fit exploration

---

#### Template 3: Carl's PRD Template

**Author:** Carl (source unknown, popular in tech)
**File:** `Carls-PRD-Template.md`

**Philosophy:** Separate problem alignment from solution alignment. Ensure everyone agrees on the WHY before discussing the HOW.

**Structure:**

**Part 1: Problem Alignment**
- Problem & Opportunity
- High Level Approach
- Narrative (optional customer stories)
- Goals (measurable + immeasurable)
- Non-goals (explicit exclusions)

**Part 2: Solution Alignment**
- Key Features (plan of record + future considerations)
- Key Flows (end-to-end experience)
- Key Logic (rules, edge cases, non-functional requirements)

**Part 3: Development and Launch Planning**
- Key Milestones
- Operational Checklist

**Use when:**
- ✅ Large, complex features
- ✅ Need to align multiple stakeholders (exec, eng, design, sales)
- ✅ Problem space is ambiguous or contested
- ✅ Solution requires significant eng investment
- ✅ Want to separate "what to build" from "how to build it"

**Skip when:**
- ❌ Small, obvious feature
- ❌ Need to move extremely fast
- ❌ Single-person project with no stakeholder alignment needed

---

#### Template 4: Tania's Spec Template

**Author:** Tania (FinTech/Banking context)
**File:** `Tanias-Spec-Template.md`

**Philosophy:** Comprehensive spec optimized for regulated industries, customer-driven development, and QA-heavy workflows.

**Unique sections:**
- **Supporting Data** - Power BI metrics, customer metrics, usage data
- **Customer Feedback** - Structured 2-3 customer conversations with business impact
- **Market Research** - Competitor screenshots and industry insights
- **UX Brief** - Separate from development (Flow, Context, Sketch, Success metrics)
- **UX Tasks Table** - Use Case | User Story | Link to Monday ticket
- **Development Requirements Table** - User Story | Acceptance Criteria | Testing | Link
  - **Testing column** - QA testing notes separate from acceptance criteria
- **Open Questions** - Product needs R&D/Data to answer
- **Risks** - Product, technical, delivery risks
- **Limitations / Requirements** - Version requirements, platform constraints

**Use when:**
- ✅ FinTech, banking, healthcare, or regulated industries
- ✅ Heavy customer co-development (working directly with 2-3 banks/clients)
- ✅ Need explicit testing guidance for QA team
- ✅ Multiple constraints (version requirements, platform limitations)
- ✅ Need to link every requirement to tickets (Monday, Jira, etc.)
- ✅ Require separate UX and development sections

**Skip when:**
- ❌ Consumer product without regulatory requirements
- ❌ Fast-moving startup environment
- ❌ Don't have customer conversations to structure
- ❌ Testing is handled by engineering, not separate QA

---

#### Choosing the Right Template

**Start here:**

1. **Is this an AI feature?** → Use **Lenny's Enhanced** for AI autonomy sections
2. **Do you work in FinTech/regulated industry?** → Use **Tania's Spec Template**
3. **Is problem alignment critical?** → Use **Carl's Template** to separate problem/solution
4. **Do you need speed above all?** → Use **Lenny's Original**

**Mix and match:**
- You can combine sections from different templates
- Start with a base template and add sections you need
- Example: Carl's structure + Tania's testing column + Lenny's AI sections

**Pro tip:**
- For your first PRD, use Lenny's Original to get comfortable
- As projects get more complex, migrate to Carl's or Enhanced versions
- Keep a "house template" for your team and customize it over time

---

#### Template Comparison: What's Different?

**Customer Evidence:**
- **Tania's:** Most structured (2-3 customer conversations with business impact)
- **Carl's:** Incorporated into Problem & Opportunity section
- **Lenny's (both):** "Why" section with evidence bullets

**Testing & QA:**
- **Tania's:** Separate Testing column in requirements table (unique!)
- **Carl's:** Key Logic section includes edge cases
- **Lenny's (both):** Minimal - assumes eng/design handle edge cases

**AI Features:**
- **Lenny's Enhanced:** Dedicated AI Autonomy & Control section (unique!)
- **Other templates:** Would need to add AI sections manually

**Stakeholder Alignment:**
- **Carl's:** Best - separates problem vs solution alignment explicitly
- **Tania's:** Strong - structured customer feedback section
- **Lenny's:** Minimal - assumes small team with tight alignment

**Monetization:**
- **Lenny's Enhanced:** Explicit business case section (unique!)
- **Carl's:** Goals section can include revenue goals
- **Tania's:** Business Impact mentioned but not explicit ROI section

---

**All templates available at:**
```
/Users/lironavineri/Documents/claude-code-course/lesson-modules/2-advanced-pm-work/2.1-write-prd/prd-templates/
```

### Data Reports

**Problem Analysis Template**
```markdown
# [Feature/Metric] Problem Analysis

## Executive Summary
- Current state (metrics)
- Problem identified (data-backed)
- Proposed solution

## Quantitative Evidence
- Funnel analysis showing drop-offs
- Time-series showing trends
- Segmentation showing who's affected most

## Qualitative Evidence
- Survey themes with representative quotes
- User feedback synthesis
- Feature requests

## Root Cause Analysis
- Why is this happening?
- Supporting evidence

## Proposed Solution
- What we'll build
- Expected outcomes
- Success metrics
```

**ROI Scenario Analysis Template**
```markdown
# [Feature] ROI Scenario Analysis

## Investment
- Cost breakdown
- Timeline

## Assumptions to Vary
- Adoption rate
- Impact magnitude
- Secondary effects

## Scenario 1: Pessimistic (20th percentile)
- Assumptions, impact, revenue, ROI

## Scenario 2: Realistic (50th percentile)
- Assumptions, impact, revenue, ROI

## Scenario 3: Optimistic (80th percentile)
- Assumptions, impact, revenue, ROI

## Risk-Adjusted Expected Value
- Weighted average across scenarios

## Recommendation
- Ship/iterate/kill decision with reasoning
```

**Experiment Readout Template**
```markdown
# [Feature] Experiment Readout

## Topline Results
- Control vs treatment metrics
- Statistical significance

## Segmentation Analysis
- Results by target customer segment
- Why segments differ

## Quality Metrics
- Retention, engagement, leading indicators

## Recommendation
- Ship/iterate/kill decision
- Segment-specific rollout if needed
- Monitoring plan
```

### Strategy Frameworks

**Coming soon after Module 2.3**

---

## Tips & Best Practices

### For Writing PRDs

**Coming soon after Module 2.1**

### For Data Analysis

**🎯 Always Segment Before Deciding**
- Never stop at topline metrics - they can hide massive wins or losses in specific segments
- Always analyze your target customer segment separately
- Example: +2.6pp topline can hide +10.75pp lift for small teams and -1.25pp for enterprise
- Different segments may need different solutions

**📊 Combine Quantitative + Qualitative Data**
- Quantitative (funnels, metrics) tells you WHAT is happening
- Qualitative (surveys, interviews) tells you WHY it's happening
- Best insights come from synthesizing both
- Example: Funnel shows 60% drop-off (WHAT) + Survey shows "blank canvas confusion" (WHY)

**🔢 Use Multi-Scenario Planning**
- Single-point estimates hide uncertainty and create false precision
- Three scenarios (pessimistic/realistic/optimistic) show range of outcomes
- Helps leadership understand risk/reward trade-offs
- Even pessimistic scenario should justify investment if project is worth doing

**📈 Track Quality Metrics, Not Just Quantity**
- Don't just measure if users activate - measure how engaged they are
- Quality metrics: retention, engagement, feature adoption, invites
- Leading indicators predict long-term success
- Example: Activated users who use templates → higher long-term retention

**⚠️ ROI Calculation Complexity:**
- When calculating multi-year ROI for recurring improvements (e.g., +X users/month), be careful about timeframes
- LTV (Lifetime Value) is collected over 24 months, not immediately
- Year 1 cash collected ≠ Year 1 ARR ≠ Total LTV created in Year 1
- For +455 users/month improvement:
  - Year 1: Add 5,460 total users, but revenue is triangular (Month 1 = 455 users paying, Month 12 = 5,460 users paying)
  - 3-Year: Add 16,380 total users over 36 months (455 × 36)
  - Need to clarify: cash collected vs. LTV created vs. ARR impact

**🔍 Look for Segmentation Patterns**
- Segment by: company size, user role, industry, geography, acquisition channel
- Ask: "Does this feature work better for certain customer types?"
- Ship features to segments where they work, exclude segments where they don't
- One size does NOT fit all

### For Strategy Work

**Coming soon after Module 2.3**

---

## Level 2 Progress Tracker

| Module | Status | Key Deliverable |
| --- | --- | --- |
| 2.1: Write a PRD | 🔄 In Progress | Product Requirements Document |
| 2.2: Analyze Data | ✅ Complete | Problem Analysis, ROI Scenarios, Experiment Readout |
| 2.3: Product Strategy | ⏳ Not Started | Strategic Roadmap |

---

## What's Next

After completing Level 2, you'll move on to:

**Level 3: Specialized PM Skills**
- 3.1: User Research Analysis
- 3.2: Competitive Intelligence
- 3.3: Stakeholder Management

---

## Glossary (Level 2 Additions)

**PRD (Product Requirements Document):** Comprehensive document defining what will be built, why, and how success will be measured.

**Acceptance Criteria:** Specific, testable conditions that must be met for a feature to be considered complete.

**User Story:** Description of a feature from the end-user perspective, typically following the format: "As a [persona], I want [goal] so that [benefit]."

**RICE Scoring:** Prioritization framework using Reach, Impact, Confidence, and Effort.

**Success Metrics:** Quantifiable measures used to determine if a product or feature achieved its goals.

**Funnel Analysis:** Method of tracking user progression through sequential steps to identify where users drop off.

**Segmentation:** Dividing users into groups (by company size, role, behavior, etc.) to analyze patterns and tailor solutions.

**LTV (Lifetime Value):** Total revenue expected from a customer over their entire relationship with the product.

**Activation Rate:** Percentage of new users who complete a key action that indicates they've experienced product value.

**Leading Indicators:** Early metrics that predict future success (e.g., template usage predicts retention).

**Statistical Significance (p-value):** Probability that observed results occurred by chance. p<0.05 typically means result is significant.

**A/B Test:** Experiment comparing two versions (control vs treatment) to measure impact of a change.

---

## Resources

**Course Materials Location:**
```
/Users/lironavineri/Documents/claude-code-course/
```

**Level 2 Folders:**
- `lesson-modules/2-advanced-pm-work/` - Interactive modules
- `outputs/level-2/` - Your PRDs, analyses, and strategy docs

**Key Reference Files:**
- Level 1 Reference Guide (fundamentals)
- TaskFlow company context (`company-context/`)
- Communication styles library

---

**Last Updated:** February 15, 2026
**Modules Covered:** Level 1 complete, Module 2.2 complete
**Next Update:** After Module 2.3 completion

**Questions?** Ask Claude anytime during the course!
