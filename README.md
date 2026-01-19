# sales-rep-reallocation-internship-project
Documentation-only internship project detailing the design and reasoning behind a sales rep reallocation and scenario versioning tool built at LINEN.Cloud. Covers problem context, user workflows, system architecture, versioning strategy, and product decisions, with visuals and high-level explanations while respecting code confidentiality.

# Sales Rep Reallocation & Scenario Versioning  
**Internship Case Study (Documentation Only)**

## Overview
During my **Summer 2025 internship at LINEN.Cloud**, an AI-driven sales operations platform, I worked on a cross-functional team focused on solving a common but high-impact challenge in sales organizations: **how to reallocate accounts when sales coverage changes** due to rep turnover, territory shifts, or capacity imbalances.

LINEN.Cloud is a no-code platform that automates sales planning by organizing team hierarchies, territories, and performance goals in one place. It integrates directly with systems like Salesforce to ensure accounts are assigned correctly and commissions are calculated accurately. Our goal was to extend this foundation with a tool that allowed sales operations teams to make reassignment decisions **quickly, safely, and with confidence**.

> **Confidentiality Note:** This repository contains **documentation only**. The original source code, data, and internal logic are proprietary to LINEN.Cloud and are not included here.

---

## The Problem
When a sales rep leaves or coverage changes, account reallocation is rarely straightforward. Sales operations teams must balance multiple constraints at once, including:

- A rep’s industry knowledge or specialization  
- Reasonable account load and capacity  
- Geographic or territory alignment  
- Historical performance and experience  

Without the right tooling, these decisions are often manual, difficult to validate, and hard to reverse. Teams needed a way to **experiment with reassignment scenarios**, understand tradeoffs, and avoid accidentally overwriting critical data.

---

## Users & Use Cases
**Primary users:** Sales Operations and Revenue Operations managers  

**Key needs:**
- Quickly test “what-if” reassignment scenarios  
- Combine algorithm-generated recommendations with manual judgment  
- Track how decisions change over time  
- Compare scenarios before committing to one  
- Maintain transparency and trust in the data  

---

## My Role & Ownership
I contributed as a **Data Analyst Intern with a strong product focus**, working closely with engineers and product stakeholders. My work centered on the **scenario management and versioning experience**, with ownership over:

- Designing **versioned scenario workflows** so each reassignment state could be saved, revisited, and compared  
- Defining data structures that paired each scenario with **metadata and edit history** to preserve context and decision rationale  
- Supporting **safe experimentation**, allowing users to test changes without risking the original dataset  
- Helping design and implement a **Streamlit UI** that surfaced scenario branching and version lineage in a clear, intuitive way  
- Translating complex backend concepts into workflows that aligned with how sales operations teams actually think and work  

---

## Solution Summary
The resulting tool enabled users to move beyond one-off edits and instead work iteratively:

- Users could generate or manually adjust rep assignments  
- Each reassignment state was saved as a **distinct scenario**  
- Scenarios included structured metadata (assumptions, notes, timestamps) and a history of changes  
- Users could compare versions to understand **what changed and why** before finalizing decisions  

This approach balanced analytical rigor with usability, giving users confidence to explore options without fear of losing work or context.

---

## How It Works (High Level)
At a conceptual level, the workflow followed this pattern:

1. Load an initial account-to-rep dataset  
2. Apply reassignment logic (algorithmic suggestions and/or manual edits)  
3. Save each state as a versioned scenario, including:
   - Current assignment data  
   - A history of edits  
   - Descriptive metadata for context  
4. Compare scenarios to evaluate differences and select a final outcome  

Each scenario existed independently, making it easy to trace decision evolution and roll back when needed.

---

## Key Design Decisions
- **Versioned scenarios over overwrites:** Preserved trust and reduced risk  
- **Metadata-first approach:** Ensured decisions weren’t separated from their reasoning  
- **User-centered controls:** Supported both automation and hands-on adjustment  
- **Transparency over abstraction:** Made system behavior visible instead of “black-box”  

---

## Impact
While exact metrics are confidential, this workflow helped:

- Reduce friction in reassignment planning  
- Improve clarity during review and approval conversations  
- Make scenario comparison faster for non-technical stakeholders  
- Support more thoughtful, defensible sales coverage decisions  

---

## Tools & Skills Demonstrated
- Product-minded data analysis  
- Streamlit (UI design & interaction patterns)  
- Scenario versioning concepts  
- Data modeling with CSV-based workflows  
- Cross-functional collaboration  
- User-centered design and technical documentation  

---

## What I’d Improve Next
- A clearer tree-based visualization of scenario lineage  
- Automated validation checks (capacity thresholds, territory conflicts)  
- Richer comparison summaries highlighting risk and coverage gaps  
