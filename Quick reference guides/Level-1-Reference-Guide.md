# Level 1 Reference Guide: Claude Code Fundamentals

**Status:** In Progress (Modules 1.1-1.5 Complete)
**Last Updated:** February 14, 2026
**Next Update:** After completing Modules 1.6-1.7

---

## Table of Contents

1. [Course Overview](#course-overview)
2. [Module 1.1: Welcome](#module-11-welcome)
3. [Module 1.2: Visualizing Files](#module-12-visualizing-files)
4. [Module 1.3: First Tasks](#module-13-first-tasks)
5. [Module 1.4: Agents](#module-14-agents)
6. [Module 1.5: Custom Sub-Agents](#module-15-custom-sub-agents)
7. [Quick Reference: Commands & Patterns](#quick-reference-commands--patterns)
8. [Common Workflows](#common-workflows)
9. [Tips & Best Practices](#tips--best-practices)

---

## Course Overview

### What You're Learning

Claude Code is a powerful AI tool for Product Managers that can save you **10-20 hours per week** through:
- Automated meeting note processing
- User research synthesis
- Multi-format communication generation
- Parallel task execution
- Custom workflow automation

### Course Structure

**Level 1: Fundamentals**
- 1.1: Welcome (TaskFlow intro, course structure)
- 1.2: Visualizing Files (visual workspace setup)
- 1.3: First Tasks (file operations, analysis, communication)
- 1.4: Agents (parallel processing)
- 1.5: Custom Sub-Agents (specialized assistants) ⬅️ YOU ARE HERE
- 1.6: Project Memory (CLAUDE.md files)
- 1.7: Navigation (keyboard shortcuts, efficiency)

**Level 2: Advanced PM Work**
- 2.1: Write a PRD
- 2.2: Analyze Data
- 2.3: Product Strategy

### The Fictional Company: TaskFlow

Throughout this course, you work as a Senior PM at TaskFlow:
- **What it is:** Project management SaaS (Asana meets Jira for remote teams)
- **Stage:** Series B, $20M raised, 50 employees
- **Your role:** Senior PM (activation & onboarding)
- **Current metrics:** $2.5M ARR, 10,000 active users
- **Your goal:** Increase activation from 45% → 60%

**Key personas:**
- **Sarah (Enterprise Admin)** - Needs SSO, security, audit logs
- **Mike (IC Engineer)** - Wants speed, keyboard shortcuts, GitHub integration
- **Alex (Team Lead)** - Needs team visibility, workload balance, reporting

---

## Module 1.1: Welcome

### What You Learned

✅ TaskFlow company overview and your role
✅ Course structure (interactive modules + reference guides)
✅ How to use slash commands to navigate modules
✅ That you communicate with Claude in plain English (no coding required)

### Key Commands

| Command | What It Does |
| --- | --- |
| `/start-1-1` | Start Module 1.1 (Welcome) |
| `/start-1-2` | Start Module 1.2 (Visualizing Files) |
| `/start-X-Y` | Start any module (replace X and Y with module numbers) |

### Key Concepts

**Interactive Learning:** You learn by doing actual PM work with real files and exercises, not just reading documentation.

**TaskFlow Context:** All exercises use realistic TaskFlow scenarios - meetings, user research, product decisions, etc.

---

## Module 1.2: Visualizing Files

### What You Learned

✅ Why visual workspace matters (not working "blind")
✅ How to choose and install a visual workspace tool
✅ Split-screen workflow (Terminal + Editor)
✅ Seeing files created/edited in real-time
✅ Understanding the .claude/ folder

### Visual Workspace Options

| Tool | Pros | Cons | Best For |
| --- | --- | --- | --- |
| **Nimbalyst** (Recommended) | Built for Claude Code, shows diffs, sees hidden folders | New tool to learn | Most users |
| **Obsidian** | Popular, great for markdown, familiar | Can't see .claude/ folder | Note-takers |
| **VS Code / Cursor** | Powerful, feature-rich | More complex | Developers |

### Split-Screen Workflow

```
+-----------------------------+-----------------------------+
|     Terminal (Left)         |     Editor (Right)          |
|     Claude Code             |     File Viewer             |
+-----------------------------+-----------------------------+
| > claude                    | Files:                      |
| User: Create a PRD...       |  - company-context/         |
| Claude: Creating PRD...     |  - lesson-modules/          |
|                             |  - your-work/               |
|                             | [File content shown here]   |
+-----------------------------+-----------------------------+
```

**Setup:**
1. Open Terminal with Claude Code (left half of screen)
2. Open your visual workspace (right half of screen)
3. Navigate to: `/Users/lironavineri/Documents/claude-code-course`
4. Watch files appear/update in real-time as Claude works

### Key Concepts

**Real-time visualization:** As Claude creates or edits files, you see the changes immediately in your editor.

**The .claude/ folder:** Contains custom commands and configurations. Nimbalyst can see it; Obsidian cannot (use Finder/Explorer instead).

---

## Module 1.3: First Tasks

### What You Learned

✅ Using @ to reference files
✅ Reading and analyzing file contents
✅ Transforming messy content into polished outputs
✅ Creating reusable communication styles
✅ Processing meeting notes into action items
✅ Synthesizing user research from multiple interviews
✅ Generating multi-format communications

### Core Pattern: @ File References

**Syntax:**
```
@filename.md          - Reference a file
@folder/             - Reference a folder
@path/to/file.md     - Full path (if needed)
```

**Examples:**
```
"Read @meeting-notes.md"
"Analyze all files in @user-interviews/"
"Summarize @product-sync-notes.md"
"Based on @communication-styles, transform @research.md"
```

**When to specify full path:**
- Multiple files with same name in different folders
- Ambiguous references
- Otherwise, just the filename usually works!

### Scenario 1: Meeting Notes Processing

**Problem:** Messy meeting notes from 3+ meetings, need action items before weekend
**Time:** 30-45 min manually → 2 min with Claude Code

**Command Pattern:**
```
"Organize the action items from @meeting-notes-raw.md by owner"
```

**What Claude does:**
1. Reads the messy meeting notes
2. Identifies all action items
3. Extracts owner, priority, due date
4. Creates formatted table
5. Organizes by owner

**Output:** Clean action item table with owners, priorities, due dates

### Scenario 2: User Research Synthesis

**Problem:** 8 interview transcripts (3-4 pages each), need to find patterns
**Time:** 2-3 hours manually → 5 min with Claude Code

**Command Pattern:**
```
"Analyze all the user interviews in @user-interviews and create a summary document highlighting overall findings and themes"
```

**What Claude does:**
1. Reads all 8 transcripts
2. Identifies common pain points (frequency count)
3. Extracts supporting quotes
4. Identifies feature requests
5. Creates comprehensive synthesis document

**Output:** Research synthesis with:
- Top pain points (ranked by frequency)
- Supporting user quotes
- Feature requests (prioritized)
- Recommended next steps
- Competitive intelligence

**Pro Tip:** You can customize the synthesis format by being more specific in your prompt!

### Scenario 3: Communication Transformation

**Problem:** Same information needs to reach 3 different audiences (team, execs, company)
**Time:** 30-45 min manually → 2 min with Claude Code

**The Pattern: Reusable Communication Styles**

1. **Create style templates once** (define format, tone, structure)
2. **Reference styles with @** when transforming content
3. **Get consistent output** every time

**Command Pattern:**
```
"Based on the communication styles in @communication-styles, create 3 messages about @user-research-synthesis.md and put them all together into a new document"
```

**What Claude does:**
1. Reads all communication style templates
2. Reads the source content (research synthesis)
3. Transforms content into each format:
  - Slack Update (casual, 2-4 lines, emojis)
  - Executive Email (strategic, 3 paragraphs, business impact)
  - Notion Doc (comprehensive, detailed, standalone)

**Output:** One document with 3 versions, each perfectly formatted for its audience

### Communication Style Examples

**Style 1: Slack Update**
- Length: 2-4 lines
- Tone: Casual, friendly
- Emojis: 1-2
- Focus: Quick team update

**Style 2: Executive Email**
- Length: 3 paragraphs
- Tone: Professional, strategic
- Structure: Findings → Impact → Next Steps
- Focus: Business outcomes, ROI

**Style 3: Notion Document**
- Length: As needed (300-600 words)
- Tone: Professional, detailed
- Structure: Summary, sections with headers, tables, callouts
- Focus: Comprehensive reference

**Common PM Styles to Create:**
1. Executive Briefing
2. User Story
3. Linear/Jira Issue
4. Weekly Update
5. Release Notes
6. PRD Section
7. Slack Announcement
8. Stakeholder Email

### Time Savings Summary (Module 1.3)

| Task | Manual Time | With Claude Code | Savings |
| --- | --- | --- | --- |
| Meeting processing | 30-45 min | 2 min | ~35 min |
| User research synthesis | 2-3 hours | 5 min | ~2.5 hours |
| Multi-format communications | 30-45 min | 2 min | ~35 min |
| **Weekly total (if done weekly)** | **3-4 hours** | **\~10 min** | **\~3.5 hours/week** |

---

## Module 1.4: Agents

### What You Learned

✅ Agents are independent Claude instances that work simultaneously
✅ Parallel processing: 10 tasks at once instead of 1 at a time
✅ When to use agents vs regular sequential work
✅ Batch processing pattern (10 meeting notes processed simultaneously)
✅ The math: 10 tasks × 5 min = 50 min sequential, or 5 min with 10 agents

### Key Concept: Agents vs Regular Claude

|  | Regular Claude | Agents |
| --- | --- | --- |
| **Tasks** | One at a time, sequential | Multiple at once, parallel |
| **Speed** | 1x | Nx (where N = number of agents) |
| **Best for** | Single tasks, iterative work | Batch processing, multi-source research |
| **Each agent** | — | Full Claude instance with all capabilities |

### When to Use Agents

✅ **USE agents for:**
- Batch processing (10 meeting notes, 20 interviews, 15 tickets)
- Multi-source research (5 competitors researched simultaneously)
- Different data types (interviews + surveys + tickets + sales notes)
- Any task that can be broken into independent parallel pieces

❌ **DON'T use agents for:**
- Single tasks (just ask Claude directly)
- Sequential work (Task 2 depends on Task 1's output)
- Simple quick tasks (overkill)
- Iterative conversations (strategy discussions, brainstorming)

### How to Decide: Agent Checklist

1. **Can this be broken into independent parallel tasks?** If yes → agents
2. **How many independent tasks?** That's how many agents you need
3. **Are tasks similar or different?** Similar = generic agents, Different = specialized agents
4. **Will outputs need combining?** If yes → plan a synthesis step

### Agent Patterns for PMs

**Pattern 1: Batch Processing (Same Task, Many Files)**
```
"Process all 10 meeting notes in parallel using agents.
Each agent should extract action items, decisions, and next steps."
```

**Pattern 2: Multi-Source Research (Different Sources, Same Topic)**
```
"Research our top 5 competitors in parallel.
Each agent should research one competitor's features, pricing, and positioning.
Then combine into a competitive landscape synthesis."
```

**Pattern 3: Specialized Agents (Different Tasks, Different Data)**
```
"Analyze these data sources with specialized agents:
- Agent 1 (Interview Analyst): Analyze user interviews
- Agent 2 (Survey Analyst): Analyze survey CSV data
- Agent 3 (Support Analyst): Review support tickets
- Agent 4 (Sales Analyst): Review sales notes
Then create a unified synthesis."
```

###    How to assign specialized agents to tasks                                                                
  **1. Just ask in plain English:**                                                     
  You describe what you want and I figure out the specializations. For example:       
  "Analyze my mobile app data:                                                      
- Analyze user interviews for pain points and quotes                            
- Analyze the survey CSV for percentages and segments                               
- Review support tickets for common scenarios                                       
- Review sales notes for lost revenue impact
  Then synthesize everything into one report."

  I'll spin up agents with the right "lens" for each data type based on your
  description.

  **2.** **Explicitly** **name** **the** **specializations:**
  You can be more specific about what each agent should focus on:
  "Use specialized agents:
- Interview Analyst: read user-interviews/, extract emotional pain points and direct
   quotes
- Survey Analyst: read survey.csv, calculate percentages by role
- Support Analyst: read support-tickets/, categorize by use case and severity
- Sales Analyst: read sales-notes.md, quantify revenue impact
  Then combine into a synthesis."

  **The** **key** **insight:** The specialization comes from the *instructions* you give, not from
  some technical configuration. You're telling each agent what to focus on, what lens
  to use, and what output to produce. The more specific your instructions, the more
  specialized the analysis.


### Agents vs Custom Sub-Agents (Preview)

|  | Agents (Module 1.4) | Custom Sub-Agents (Module 1.5) |
| --- | --- | --- |
| **Nature** | Ad-hoc, temporary | Pre-configured, permanent |
| **Created** | On the fly for parallel work | Once, reused many times |
| **Analogy** | Temp contractors | Permanent specialized team |
| **Best for** | Batch parallel tasks | Consistent specialized analysis |

### Time Savings (Module 1.4)

| Task | Sequential Time | With Agents | Savings |
| --- | --- | --- | --- |
| 10 meeting notes | 50 min | ~5 min | 10x faster |
| 5 competitor analyses | 2.5 hours | ~30 min | 5x faster |
| Multi-source research (4 sources) | 2 hours | ~30 min | 4x faster |

---

## Module 1.5: Custom Sub-Agents

### What You Learned

✅ Custom sub-agents are pre-configured specialists with distinct personalities and expertise
✅ Different from Module 1.4 - permanent team members vs temporary workers
✅ Three pre-built sub-agents: Engineer, Executive, User Researcher
✅ Call them explicitly ('Use the engineer subagent') or let Claude invoke them automatically
✅ Multiple sub-agents can review the same work from different perspectives
✅ Main Claude orchestrates: delegates to specialists, synthesizes results
✅ Sub-agents live in `.claude/agents/` folder (hidden folder)
✅ Each sub-agent has YAML frontmatter + system prompt
✅ 100+ pre-built agents available in community libraries

### Key Concept: Agents vs Sub-Agents

|  | Agents (Module 1.4) | Sub-Agents (Module 1.5) |
| --- | --- | --- |
| **Nature** | Ad-hoc, temporary | Pre-configured, permanent |
| **Created** | On the fly for parallel work | Once, reused many times |
| **Analogy** | Temp contractors | Permanent specialized team |
| **Capabilities** | Generic (any task) | Specialized (distinct personality & expertise) |
| **Best for** | Batch parallel tasks | Repeated specialized perspectives |
| **Use when** | You need parallel processing NOW | You need specialist input REPEATEDLY |

### Your Pre-Built Team

| Sub-Agent | Emoji | Color | Expertise |
| --- | --- | --- | --- |
| **Engineer** | (@_@) | Purple | Technical feasibility, architecture, implementation complexity |
| **Executive** | (ಠ_ಠ) | Blue | Strategic framing, stakeholder communication, business cases |
| **User Researcher** | (^◡^) | Green | Pain point synthesis, research analysis, user advocacy |

### How to Invoke Sub-Agents

**Two methods:**

1. **Explicit** - You request a specific sub-agent:
```
"Use the engineer subagent to review this spec"
"Have the executive subagent frame this for leadership"
"Ask the user researcher subagent to analyze these interviews"
```

2. **Automatic** - Claude uses them when appropriate based on their description. Just ask naturally and Claude will route to the right specialist.

**Multi-agent orchestration:**
```
"Have the Engineer, Executive, and User Researcher review
feature-spec.md and create a consolidated review"
```

### Sub-Agent File Structure

Each sub-agent is a `.md` file in `.claude/agents/` with two parts:

**Section 1: YAML Frontmatter** (between `---` markers)
- `name:` - Identifier (can include text face emoji for visual personality)
- `description:` - When and how this sub-agent should be invoked
- `tools:` (optional) - Which tools this agent can use
- `model:` (optional) - Which AI model to use (sonnet, opus, haiku, or inherit)
- `color:` (optional) - Visual identity color

**Section 2: System Prompt** (after the frontmatter)
- Who they are (background, experience, role)
- What they provide (specific capabilities)
- How they communicate (style, tone, approach)
- What value they give you as a PM
- Output structure they should follow

The YAML frontmatter tells Claude Code **WHEN** to use the sub-agent.
The system prompt tells the sub-agent **HOW** to behave.

### Example: Executive Sub-Agent File

```yaml
---
name: (ಠ_ಠ) executive
description: Strategic framing, executive communication, and stakeholder alignment.
tools: Read, Grep, Glob, Bash
model: inherit
color: blue
---

# (ಠ_ಠ) Executive - Strategic Communication Specialist

You are a seasoned executive (VP or C-level) with 15+ years of leadership...

## Your Role
- Strategic framing and business context
- Executive summary writing
- Stakeholder communication advice
...
```

### Community Libraries

You don't have to create sub-agents from scratch! 100+ pre-built sub-agents are available:

- **awesome-claude-agents:** Collection of 100+ pre-built agent personas
- **pm-agent-library:** Product Manager specific sub-agent templates

Just copy the `.md` files into your `.claude/agents/` folder and they're ready to use.

**Common pre-built sub-agents:**
- QA Tester, Data Analyst, Technical Writer
- Competitive Intelligence, Growth Strategist
- DevOps Engineer, Security Reviewer
- Content Strategist, Design Reviewer

---

## Quick Reference: Commands & Patterns

### File Operations

| What You Want | Command Pattern | Example |
| --- | --- | --- |
| Read a file | `@filename` | "Read @meeting-notes.md" |
| Read multiple files | `@file1, @file2` | "Compare @notes1.md and @notes2.md" |
| Read a folder | `@folder/` | "Analyze all files in @user-interviews/" |
| Extract info | "Extract [what] from @file" | "Extract action items from @meeting-notes.md" |
| Summarize | "Summarize @file" | "Summarize @product-sync-notes.md" |
| Organize | "Organize [what] by [criteria]" | "Organize action items by owner" |

### Analysis Operations

| What You Want | Command Pattern | Example |
| --- | --- | --- |
| Find patterns | "Analyze @files and identify patterns" | "Analyze @user-interviews/ and find common pain points" |
| Synthesize | "Create synthesis from @files" | "Synthesize findings from @research/" |
| Compare | "Compare @file1 and @file2" | "Compare @asana-research.md and @linear-research.md" |

### Transformation Operations

| What You Want | Command Pattern | Example |
| --- | --- | --- |
| Transform format | "Transform @file into [format]" | "Transform @research.md into Slack update" |
| Use styles | "Based on @styles, transform @content" | "Based on @communication-styles, transform @findings.md" |
| Multiple outputs | "Create [number] versions of @content" | "Create 3 versions: Slack, email, Notion doc" |

### Creation Operations

| What You Want | Command Pattern | Example |
| --- | --- | --- |
| Create document | "Create [doc type] from @source" | "Create PRD from @user-research.md" |
| Append to file | "Add [content] to @file" | "Add action items summary to @meeting-notes.md" |
| Create with style | "Create @file using @style" | "Create weekly update using @update-style.md" |

---

## Common Workflows

### Workflow 1: End-of-Day Meeting Processing

**Situation:** 5pm Friday, 3 meetings, messy notes, team needs action items

**Steps:**
1. Have Claude read your meeting notes: `@meeting-notes.md`
2. Extract action items: "Organize action items by owner"
3. Review the output in your editor
4. Share with team

**Time saved:** 40 minutes → 2 minutes

---

### Workflow 2: User Research → Insights → Communications

**Situation:** Completed 8 user interviews, need to present findings to multiple audiences

**Steps:**
1. Synthesize research:
```
   "Analyze all user interviews in @user-interviews/ and create a summary document"
```

2. Create multi-format communications:
```
   "Based on @communication-styles, create 3 messages about @synthesis.md"
```

3. Review outputs:
  - Slack update (for team)
  - Executive email (for leadership)
  - Notion doc (for company)

4. Send to appropriate audiences

**Time saved:** 3-4 hours → 10 minutes

---

### Workflow 3: Weekly Status Updates

**Situation:** Every Monday, need to send update to stakeholders in different formats

**Steps:**
1. Create a "Weekly Update" communication style (once)
2. Keep notes throughout the week in `@weekly-notes.md`
3. On Monday: "Transform @weekly-notes.md using @weekly-update-style.md"
4. Get formatted update ready to send

**Time saved:** 30 min/week → 2 min/week (26 hours/year!)

---

## Tips & Best Practices

### File References (@)

✅ **DO:**
- Start with just the filename: `@notes.md`
- Use folder references for bulk operations: `@interviews/`
- Be specific if ambiguous: `@project-a/notes.md`

❌ **DON'T:**
- Guess file paths - ask Claude to list files if unsure
- Reference files that don't exist (Claude will tell you)
- Forget the @ symbol (Claude won't know it's a file reference)

### Communication Styles

✅ **DO:**
- Create styles once, reuse forever
- Define format rules (length, tone, structure)
- Include examples in style templates
- Build a library over time

❌ **DON'T:**
- Recreate styles for each use
- Make styles too rigid (allow flexibility)
- Skip the example (shows Claude what "good" looks like)

### Prompting Best Practices

✅ **DO:**
- Be specific about what you want
- Reference source files with @
- Specify desired output format
- Ask for what you need ("create a summary with...")

❌ **DON'T:**
- Be too vague ("do something with this")
- Forget to specify where info comes from
- Assume Claude knows context (provide it!)

### Image Analysis: Prompts & Best Practices

**Two Ways to Work with Images:**

1. **Paste directly:** Press **Ctrl+V** (works on Mac too!) after copying/screenshotting
2. **Reference file:** Use `@path/to/image.png` to reference saved images

🚨 **CRITICAL:** On Mac, use **Ctrl+V** (NOT Command+V) to paste images!

**Generic vs Specific Prompts:**

| Your Prompt | What Claude Does |
| --- | --- |
| `"analyze @mockup.png"` | Comprehensive PM analysis (UX, accessibility, improvements, metrics) |
| `"analyze @mockup.png for accessibility issues only"` | Focused WCAG compliance check |
| `"analyze @mockup.png from a mobile UX perspective"` | Mobile-specific analysis (responsive, touch targets) |
| `"compare @our-design.png to Amazon's product page"` | Competitive UX comparison |

**Common Image Analysis Patterns:**

```
Design Review:
"Analyze @ui-mockup.png and provide UX feedback"
"Review @wireframe.png for missing elements"

Accessibility Audit:
"Check @design.png for WCAG 2.1 AA compliance"
"Identify color contrast issues in @mockup.png"

Competitive Analysis:
"Compare @our-ui.png to @competitor-screenshot.png"
"What can we learn from @amazon-product-page.png?"

Technical Feasibility:
"Analyze @mockup.png for front-end implementation challenges"
"Estimate complexity of building @design.png"

User Flow Analysis:
"Analyze @user-flow.png for friction points"
"Identify drop-off risks in @onboarding-flow.png"

Data Visualization:
"Is the data clear in @dashboard.png?"
"Improve the chart design in @analytics-screenshot.png"

Bug Documentation:
"Document the error shown in @bug-screenshot.png"
"What's wrong with @broken-ui.png?"
```

**Controlling the Output:**

**Specify perspective:**
```
"Analyze @mockup.png from Mike (IC Engineer persona)'s perspective"
"Review @design.png as a PM checking launch readiness"
"Evaluate @mockup.png as a front-end engineer estimating effort"
```

**Specify output format:**
```
"Create a prioritized list of top 5 UX issues from @mockup.png"
"Write a design review email based on @mockup.png"
"Generate Linear tickets for issues in @design.png"
"Create a table: Issue | Severity | Recommendation from @ui.png"
```

**Specify scope:**
```
"Focus only on above-the-fold content in @mockup.png"
"Analyze mobile experience only in @responsive-design.png"
"Find critical issues only (not nice-to-haves) in @mockup.png"
```

**Combine with other files:**
```
"Analyze @mockup.png against requirements in @prd.md"
"Compare @mockup.png to our design system in @design-guidelines.md"
"Check if @design.png addresses pain points from @user-research.md"
```

**What Claude Can Analyze:**
- 📱 Design mockups (Figma, Sketch, wireframes)
- 📊 Data visualizations and charts
- 🖼️ Competitor product screenshots
- 📸 Whiteboard photos from meetings
- 🎨 UI components and flows
- 📈 Analytics dashboards
- ❌ Error messages and bug screenshots
- 🎯 User journey maps
- 📋 Information architecture diagrams

**Pro Tips for Image Analysis:**

1. **Be specific about what you need:**
  - ❌ "What do you think?"
  - ✅ "Identify the top 3 UX issues preventing conversion"

2. **Provide context when helpful:**
  - "Analyze @mockup.png - this is for first-time users with no training"
  - "Review @design.png - our target is mobile-first millennials"

3. **Ask follow-up questions:**
  - First: "Analyze @mockup.png"
  - Then: "Focus on the checkout flow - what's causing friction?"
  - Then: "How would you fix issue #2?"

4. **Request specific deliverables:**
  - "Create a PRD based on @competitor-ui.png"
  - "Write user stories from @user-flow.png"
  - "Generate test cases from @mockup.png"

### General Tips

**Iteration is normal:**
- First output not perfect? Ask for revisions!
- "Make section 3 more technical"
- "Shorten the executive email to 2 paragraphs"
- "Add more specific examples"

**Build your toolkit:**
- Create communication styles for your common outputs
- Save example prompts that work well
- Build a library of reusable patterns

**Trust but verify:**
- Always review Claude's output in your editor
- Claude is powerful but not infallible
- You're the PM - make final decisions

---

## What's Next in Level 1

### Module 1.6: Project Memory (Coming Next)
Use CLAUDE.md files to give Claude persistent context:
- Project background
- Style guidelines
- Common workflows
- Team preferences

### Module 1.7: Navigation
Master keyboard shortcuts and efficiency tools:
- Quick navigation
- Search patterns
- Workflow optimization

---

## Quick Wins You Can Use Today

Even before completing Level 1, you can start using:

1. **@ file references** - Reference any file with @filename
2. **Meeting note processing** - Turn messy notes into action items
3. **Multi-format communications** - One source → multiple formats
4. **User research synthesis** - Analyze interviews quickly

**Try this today:**
Take your messiest meeting notes and ask:
```
"Organize the action items from @[your-notes-file] by owner and priority"
```

Watch the magic happen! ✨

---

## Glossary

**@ (at symbol):** File reference syntax. Use `@filename` to tell Claude which file to read/analyze/transform.

**Communication Style:** A reusable template that defines format, tone, and structure for a specific type of output (e.g., Slack update, executive email).

**Synthesis:** Combining multiple sources (like 8 interview transcripts) into a cohesive summary with patterns, insights, and recommendations.

**TaskFlow:** The fictional company you work for throughout this course. A project management SaaS for remote teams.

**Visual Workspace:** A tool (like Nimbalyst, Obsidian, or VS Code) that shows your files alongside Claude Code, so you can see changes in real-time.

**Module:** An interactive lesson taught by Claude. Each module covers a specific skill.

**Level:** A collection of related modules. Level 1 = Fundamentals, Level 2 = Advanced PM Work.

---

## Resources

**Course Materials Location:**
```
/Users/lironavineri/Documents/claude-code-course/
```

**Key Folders:**
- `lesson-modules/` - Interactive modules
- `company-context/` - TaskFlow background materials
- `Quick reference guides/` - Reference documents (like this one!)
- `.claude/` - Course commands and configurations

**Company Context Files:**
- `company-context/COMPANY.md` - TaskFlow overview
- `company-context/PRODUCT.md` - Product details
- `company-context/PERSONAS.md` - User personas
- `company-context/COMPETITIVE.md` - Competitive landscape

---

**Last Updated:** February 14, 2026
**Modules Covered:** 1.1, 1.2, 1.3, 1.4, 1.5
**Next Update:** After Module 1.6 (Project Memory)

**Questions?** Ask Claude anytime during the course!
