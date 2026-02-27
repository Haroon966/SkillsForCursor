---
name: manager
description: Apply on every user prompt to triage the task and decide which specialized skills to invoke. Use for any user request—coding, planning, or questions—so the manager can route to frontend-dev, backend-dev, database-dev, or data-engineer as needed. Also use when the user asks about planning, scope, prioritization, tickets, estimation, roadmap, process, or workflow.
---

# Manager (Router + Planning + Process)

Run this skill on **every user message** to triage the request, then delegate to the right role skill(s). When the user asks for planning or process, apply the planning guidance below as well.

## Always Run First

On each user prompt:

1. **Assess** the request: what is the user trying to do or learn?
2. **Route** using the table below to choose which skill(s) apply.
3. **Apply** the chosen skill(s): read and follow their SKILL.md guidance when answering.
4. If **none** clearly fit, answer using general best practices and say which skill is closest for follow-up.

## Routing (Task → Skill)

| User need / topic | Skill to apply |
|-------------------|----------------|
| React, UI components, hooks, client state, styling, React Router, frontend data fetching, frontend testing | **frontend-dev** |
| Django, views, DRF, APIs, auth, middleware, settings, commands, deployment | **backend-dev** |
| Schema design, migrations, data modeling, ORM, indexes, app database structure | **database-dev** |
| SQL, data analysis, tables/datasets, local or online DBs, ETL scripts, reporting, data profiling | **data-engineer** |
| Full-stack (e.g. feature touching React and Django) | **frontend-dev** + **backend-dev** (and others if relevant) |

- **frontend-dev**: React, UI components, hooks, client state, styling, React Router, frontend data fetching, frontend testing.
- **backend-dev**: Django, views, DRF, APIs, auth, middleware, settings, commands, deployment.
- **database-dev**: Schema design, migrations, data modeling, ORM, indexes, app database structure.
- **data-engineer**: SQL, data analysis, tables/datasets, local or online DBs, ETL scripts, reporting, data profiling.

Invoke **all** skills that apply (e.g. frontend + backend for a full-stack task).

## After Routing

- Read the relevant skill file(s) (e.g. `.cursor/skills/frontend-dev/SKILL.md`) and follow their instructions when answering.
- If the request is ambiguous, you may invoke the most likely skill(s) and mention others if the user clarifies.

## Planning and Process (When User Asks)

When the user asks about planning, scope, process, or workflow:

- **Deliverables**: Break work into clear deliverables; suggest acceptance criteria; flag scope creep or missing steps.
- **Formats**: Use ticket/issue templates, short roadmap or milestone lists, checklist-style summaries where helpful.
- **Process**: Code review flow; when to document decisions (e.g. short ADRs); lightweight rituals.
- **Tone**: Structured and outcome-focused. Do not prescribe specific tools (e.g. Jira vs Linear); stay tool-agnostic unless the project already uses one.
