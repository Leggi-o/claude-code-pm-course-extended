# Spec Template

## Feature Summary

*(Expand when the feature has more clarity)*

A brief, high-level description of the feature's purpose, value, and core functionality

---

## Problem Definition

- **Summary:** Define the problem or opportunity you are addressing
- **Who is affected:** User types or segments impacted by this issue
- **Impact:** Describe the business effect (e.g., users can't create goals in different accounts, which limits their ability to track their savings)
- **Source:** Customer feedback / Loss analysis / Competitor analysis / Reported bug (including the customer who raised it) - Add links to the supporting evidence (request, quotes, call summary)

---

## Supporting Data

Power BI metrics or trends / Customer's metrics / usage data - Provide the available data that supports the issue (churn, low registration, etc.)

---

## Customer Feedback

Insights from 2–3 customer conversations or usability sessions:

- **Customer name:** Bank's name
- **Key pain points:** Main user challenges or frustrations related to this flow - what prevents users from reaching their goal efficiently
- **Business Impact:** (Time, effort, frustration, churn risk, etc.)

---

## Market Research

- Briefly summarize competitors and industry insights
- Include screenshots showing how others address this problem

*{Images}*

---

## Proposed Solution

- **Type of work:** New feature / Feature enhancement
- **Link to parent feature:** In case of enhancement, link to the main feature's doc
- **Concept overview:** Describe the proposed idea in simple terms (new button, graph)
- **Dependencies:** (if relevant – waiting for a new model, client addition etc)
- **Out-of-Scope Decisions:** Ideas or elements considered but excluded from this scope (postponed to a later phase or ruled out) and why
- **Value:** Describe the value this feature is supposed to provide
- **Success Metrics:** Specify the success criteria and metrics that indicate whether the feature is performing well (Registration rate, engagement frequency, conversion rate, retention rate, etc.)

---

## UX

### UX Brief

- **Flow:** For new features - Describe the full flow the user needs to complete. Existing feature - Where the change/addition occurs in the user journey
- **Context:** modules, add-ons, and insights where this component is/will be embedded
- **Sketch (optional):** Simple, high-level basic sketch, only if needed (PowerPoint/Paint)
- **Success metrics:** What's the final goal of this component (e.g user should finish the flow and create a goal)

### UX Tasks

| Use Case | User Story (User Actions + Constraints) | Link |
|----------|----------------------------------------|------|
| Describe the high-level purpose of this flow or component.<br><br>Examples: "Editing a date field," "Selecting a savings amount," "Viewing transaction insights." | Describe what the user needs to do and how the system should behave:<br>• User actions & steps<br>• Required content (headline, button) - only the must-have elements<br>• Input constraints (max value, numeric rules)<br>• Format/standards required (US vs EU formatting)<br>• Edge cases and validations | Link to Monday ticket |

---

## Figma

*{Link to the feature's design in Figma once ready}*

---

## Development Requirements

### Feature Requirements

| User Story | Acceptance Criteria | Testing | Link |
|-----------|---------------------|---------|------|
| Describe the capability/Element that is part of the feature.<br><br>Example:<br>• User filters transactions by date range | Define the expected behavior, logic, and edge cases.<br><br>Example:<br>• When X happens, Y should be displayed<br>• Negative inputs are not valid<br>• Items should be ordered alphabetically | Define on top of the acceptance criteria any key considerations or testing notes for the QA team:<br>• Key behaviors to pay attention to<br>• Edge cases the AC doesn't explicitly cover<br>• Cross-feature dependencies<br><br>Example:<br>• Test a user with multi currency accounts (currency filter behavior)<br>• Test as user with less than 6 months of data | Link to the YT |

---

## Open Questions

Define questions that Product needs R&D/Data to answer and any internal Product questions that require clarification to complete the spec

---

## Risks

Outline any known product, technical, or delivery risks, such as data quality or availability issues, scalability concerns, or areas with higher uncertainty that may impact timelines or outcomes

---

## Limitations / Requirements

Describe relevant constraints such as version requirements (e.g., client V3), unsupported platforms or systems (e.g., mobile only), or known edge cases/requirements (e.g., goals require real-time transactions)
