---
name: deadline-tracker
description: >
  Tracks delivery milestones, deadlines, and momentum across all active
  DigitalArmy.ai projects for Kelly Millard. Use this skill when scanning
  for upcoming deadlines, flagging stalled work, or producing the
  DEADLINES & FOLLOW-UPS section of the morning brief. Also use when the
  user asks "what's due this week", "anything stalled", or "where are we
  on [project]".
---

# Deadline Tracker

## Purpose

Surface upcoming deadlines, flag stalled momentum, and track open items
across all active DigitalArmy delivery and internal projects. Look ahead
7 days by default. Pull dates from calendar, email, Teams, and WhatsApp.

---

## Active Project Tracks

### TSPC — Rep Support Agent
Watch for:
- Regional testing progress and feedback
- Blockers or escalations from the Rep pilot group
- Data integrity issues
- API fallback issues
- Lifecycle logic changes
- Governance or performance-management updates
- Go/No-Go confirmation for staged rollout

### TSPC — Customer Onboarding Agent
Watch for:
- Onboarding flow design decisions
- RICA App / WhatsApp channel validation outcomes
- Routing rules and exception handling decisions
- Compliance sign-off items
- Pilot readiness milestones
- SteerCo approval or sign-off requests

### Discovery Life — Claims Concierge
Watch for:
- Movement toward paid POC (any stakeholder signal)
- Scope of work requests or document sharing
- Costing or commercial discussions that need Kelly's input
- Stakeholder feedback on the prototype demo
- ROI framing or business case requests
- Approval requests or next-step asks from Alan Meechan, Darryn Botha, Sylvia Steyn

### Quro Medical — AI Strategy Workshop
Watch for:
- Pilot definition progress
- Executive-team follow-up items
- Proposal requests
- Concrete next-step asks from Joost Pielage

### Old Mutual — Future Project / Procurement
Watch for:
- Procurement process movement
- Stakeholder engagement activity
- Transition signals toward an active project
- Any ask from Chris Basson, Donavan Van Der Ross, Vaniel Ramdhani

### DigitalArmy L&D / Agent Experimentation Track
Watch for movement on these internal initiatives:
- Webchat Sales Concierge (MS Copilot)
- MCP Build — Go-live PM Agent
- OpenClaw Project
- Google Cloud Agent Platform
- IT Ops / Coding Agent SDLC
- OpenAI Agents SDK exploration

**Stall rule:** Flag any initiative in this track with no visible activity
for 14 days or more.

---

## Flagging Rules

- Surface all items with a deadline or milestone in the next **7 days**
- Flag any item that appears **blocked or stalled** — no movement, missing
  decision, waiting on external party
- Flag **anyone waiting more than 3 days for a reply from Kelly** across
  any channel — check email, Teams, and WhatsApp
- For L&D / experiments: flag no-movement items at **14 days**
- Prioritise active billable delivery (TSPC, Discovery) over pipeline
  (Quro, Old Mutual) in ordering

---

## Output Format

For each item:
- Project name
- What's due or what's stalled
- Source (calendar / email / Teams / WhatsApp)
- Days until deadline or days since last movement
- Any action Kelly needs to take
