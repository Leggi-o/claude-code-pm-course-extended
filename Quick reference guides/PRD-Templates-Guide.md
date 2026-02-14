# PRD Template Comparison & Usage Guide

**Quick reference for choosing between Carl's and Lenny's PRD templates**

---

## Template Overview

### **Carl's PRD Template** - Comprehensive & Structured

**Best for:**
- ✅ Large, complex features (multi-sprint projects)
- ✅ Cross-functional initiatives requiring extensive alignment
- ✅ Enterprise features with compliance/security considerations
- ✅ Projects where you need to document edge cases and detailed logic
- ✅ Teams that prefer detailed requirements and acceptance criteria
- ✅ When stakeholders need comprehensive documentation
- ✅ Features with significant technical complexity

**Characteristics:**
- 📄 Multi-page, detailed structure
- 🎯 Deep problem exploration with evidence and customer insights
- 🔄 Alternatives analysis ("What did we consider?")
- ✏️ Key flows, key logic, acceptance criteria
- 📊 Built-in operational checklist and milestones
- 🚧 Clear goals AND non-goals (boundary setting)

**Structure:**
1. **Problem Alignment**
   - Problem & Opportunity (with evidence, customer insights, urgency)
   - High Level Approach (alternatives considered)
   - Narrative (customer stories and use cases)
   - Goals (measurable + immeasurable + guardrails)
   - Non-goals (explicit boundaries)

2. **Solution Alignment**
   - Key Features (plan of record + future considerations)
   - Key Flows (end-to-end experience)
   - Key Logic (rules, edge cases, non-functional requirements)

3. **Development & Launch Planning**
   - Key Milestones
   - Operational Checklist

**Example use cases:**
- TaskFlow's notification redesign (complex system change)
- Mobile app launch (multi-platform, many features)
- Enterprise SSO integration (compliance, security)
- Template library system (new core feature)

---

### **Lenny's PRD Template** - Lean & Fast

**Best for:**
- ✅ Small to medium features (1-2 sprint projects)
- ✅ Experiments and A/B tests
- ✅ Rapid prototyping and iteration
- ✅ Startups or fast-moving teams
- ✅ When you need stakeholder buy-in quickly
- ✅ Features where the solution approach is fairly clear
- ✅ Internal tools or quick improvements

**Characteristics:**
- 📝 One-page, 7-section format
- ⚡ Quick to write and read (15-30 minutes)
- 🎯 Focuses on essentials: Problem, Why, Success, How
- 🧪 Built-in experiment thinking ("How do we test this?")
- 🚀 Great for getting started fast

**Structure:**
1. **Description:** What is it?
2. **Problem:** What problem is this solving?
3. **Why:** How do we know this is a real problem and worth solving?
4. **Success:** How do we know if we've solved this problem?
5. **Audience:** Who are we building for?
6. **What:** Roughly, what does this look like in the product?
7. **How:** What is the experiment plan?
8. **When:** When does it ship and what are the milestones?

**Example use cases:**
- Dark mode toggle (clear problem, clear solution)
- Adding a keyboard shortcut
- Small UX improvements
- Quick bug fixes with context
- Internal tooling features

---

## Quick Decision Matrix

| Factor | Carl's Template | Lenny's Template |
|--------|-----------------|------------------|
| **Project Size** | Large (3+ sprints) | Small-Medium (1-2 sprints) |
| **Team Size** | Cross-functional (5+ people) | Small team (2-4 people) |
| **Complexity** | High technical complexity | Straightforward implementation |
| **Documentation Need** | Comprehensive records needed | Quick alignment needed |
| **Timeline Pressure** | Multi-month project | Ship fast, iterate |
| **Risk Level** | High risk/impact | Low-medium risk |
| **Experiment-First?** | Build right the first time | Test and learn |
| **Writing Time** | 2-4 hours | 15-30 minutes |
| **Reading Time** | 20-30 minutes | 5 minutes |

---

## Pro Tips

### **Start with Lenny's, graduate to Carl's:**
- Use Lenny's template for initial exploration and alignment
- Once approved, expand into Carl's template for implementation details
- Best of both worlds: fast approval + detailed execution

### **Mix and match:**
- Use Carl's Problem Alignment + Lenny's concise format
- Add Carl's "Non-Goals" section to Lenny's template
- Adapt to your team's needs

### **For TaskFlow specifically:**

| Feature | Recommended Template | Why |
|---------|---------------------|-----|
| **Dark Mode** | Lenny's | Straightforward feature, experiment with rollout |
| **Template Library** | Carl's | Complex system, multiple considerations, edge cases |
| **Notification Redesign** | Carl's | Multi-component, technical architecture, system change |
| **Add keyboard shortcut** | Lenny's | Simple, quick win, clear implementation |
| **Interactive Onboarding Tour** | Lenny's → Carl's | Start lean, expand if needed |
| **Mobile App Launch** | Carl's | Multi-platform, many features, high complexity |
| **Enterprise SSO** | Carl's | Security, compliance, detailed requirements |

---

## Common Mistakes to Avoid

### ❌ Using Carl's when Lenny's would work
- **Problem:** Over-documentation for simple features
- **Impact:** Slows down shipping, creates maintenance burden
- **Fix:** Ask "Does this really need 10 pages of documentation?"

### ❌ Using Lenny's for complex projects
- **Problem:** Under-specification leads to confusion and rework
- **Impact:** Engineers unclear on requirements, design misaligned
- **Fix:** Expand to Carl's template when complexity emerges

### ❌ Never documenting non-goals
- **Problem:** Scope creep, team confusion about boundaries
- **Impact:** Features balloon, timelines slip
- **Fix:** Always include non-goals, even in Lenny's template

### ❌ Writing PRDs in isolation
- **Problem:** Solution doesn't match technical constraints or design vision
- **Impact:** Major rework after "alignment"
- **Fix:** Collaborate with design and engineering throughout

---

## When to Skip a PRD Entirely

Sometimes you don't need a PRD at all:

- **Bug fixes** - Use a ticket with repro steps and expected behavior
- **Copy changes** - Just make the change and document in commit
- **Refactoring** - Technical spec is better than PRD
- **Prototype/spike** - Just build and show, document learnings after
- **Trivial features** - Quick Slack message + screenshot is enough

**Rule of thumb:** If you can explain it fully in < 5 minutes and everyone agrees immediately, you probably don't need a PRD.

---

## PRD Templates in Claude Code

### Creating PRDs with Claude Code

Both templates work great with Claude Code:

**Quick workflow:**
1. Reference template: `@Carls-PRD-Template.md` or `@Lennys-PRD-Template.md`
2. Provide context: `@user-research-synthesis.md` or `@product-sync-notes.md`
3. Ask Claude to draft the PRD using the template structure

**Example prompts:**
- "Using @Carls-PRD-Template.md, draft a PRD for the notification redesign based on @user-research-synthesis.md and @product-sync-notes.md"
- "Create a lean PRD using @Lennys-PRD-Template.md for adding dark mode to TaskFlow"

**Pro tip:** Let Claude draft the initial version, then refine collaboratively. PRDs are living documents!

---

## Template Evolution

### When to update your templates

**Add sections when you notice patterns:**
- Repeated questions from engineers? Add FAQ section
- Security concerns keep coming up? Add security checklist
- Accessibility often overlooked? Add accessibility requirements

**Remove sections that don't add value:**
- Nobody reads the appendix? Delete it
- Milestones tracked elsewhere? Link instead of duplicating

**Adapt to your team:**
- If design owns flows, don't duplicate in PRD - link instead
- If engineering prefers acceptance criteria, expand Key Logic section
- If leadership wants metrics, add success metrics dashboard

---

## Related Resources

- **Original Templates:**
  - Carl's: `lesson-modules/2-advanced-pm-work/2.1-write-prd/prd-templates/Carls-PRD-Template.md`
  - Lenny's: `lesson-modules/2-advanced-pm-work/2.1-write-prd/prd-templates/Lennys-PRD-Template.md`

- **Module 2.1:** Write a PRD (full interactive lesson on PRD writing)
- **Level-1-Reference-Guide.md:** Fundamentals of Claude Code workflows
- **Solutions-Research.md:** Design pattern research examples

---

**Last Updated:** February 2026
**Maintained as part of:** Claude Code PM Course Extended
