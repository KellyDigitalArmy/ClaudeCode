---
name: signal-router
description: >
  Routes action items, follow-ups, and deep work tasks to the correct
  Claude project for Kelly Millard at DigitalArmy.ai. Use this skill
  when concluding the morning brief, when the user asks "where should I
  handle this", or when any task needs routing to the right working context.
  Always use alongside morning-brief-formatter when producing the brief.
---

# Signal Router

## Purpose

Every actionable item surfaced in the morning brief (or in any working session)
should be routed to the correct Claude project. This keeps Kelly's working
contexts clean, prevents context-switching, and ensures deep work lands in
the right place.

---

## The Three Projects

### Signal 08:30
**Default surface for the morning brief itself.**
Use for:
- Clarifying any item from today's brief
- Quick follow-up questions on brief content
- Short decisions that don't need a full project context
- Anything that doesn't clearly belong to Delivery or L&D

### DigitalArmy Delivery / Client Projects
**All active client delivery work.**
Use for:
- TSPC Rep Support Agent — any delivery, integration, pilot, or testing work
- TSPC Customer Onboarding Agent — design, build, compliance, pilot readiness
- Discovery Life Claims Concierge — POC scoping, prototype refinement, stakeholder follow-up
- Quro Medical — workshop prep, pilot definition, proposal work
- Old Mutual — procurement follow-up, project scoping, stakeholder engagement
- Any other billable client delivery task

### DigitalArmy L&D / Agent Experiments
**Internal capability building and experimentation.**
Use for:
- Webchat Sales Concierge (MS Copilot)
- MCP Build — Go-live PM Agent
- OpenClaw Project
- Google Cloud Agent Platform
- IT Ops / Coding Agent SDLC
- OpenAI Agents SDK exploration
- Any internal agent experiment, prototype, or skills development work
- Reading, videos, and L&D content flagged by Suveer or the team

---

## Routing Logic

When tagging a brief item for routing, apply this order:

1. **Is it about an active client or billable delivery?**
   → *DigitalArmy Delivery / Client Projects*

2. **Is it an internal experiment, platform build, or L&D item?**
   → *DigitalArmy L&D / Agent Experiments*

3. **Is it a quick clarification or follow-up on today's brief?**
   → *Signal 08:30*

4. **Unclear or spans multiple contexts?**
   → *Signal 08:30* by default; note the ambiguity

---

## Output Format

When routing in the morning brief, append a single line after the item:
`→ Handle in: [Project Name]`

At the end of the brief, always close with:
`→ Follow up or clarify any item in the *Signal 08:30* project.`

No other closing text.
