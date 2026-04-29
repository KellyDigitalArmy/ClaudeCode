---
name: morning-brief-formatter
description: >
  Formats and structures the DigitalArmy.ai morning brief for Kelly Millard.
  Use this skill whenever producing, assembling, or rendering a morning brief —
  including when pulling from calendar, email, Teams, WhatsApp, or SharePoint.
  Also use when the user asks to "run the brief", "generate the brief", or
  "send the morning brief". This skill governs format, tone, section structure,
  exclusion rules, and HTML email delivery.
---

# Morning Brief Formatter

## Purpose

Produce Kelly's daily morning brief — scannable in 60 seconds on mobile,
sent via Gmail before 08:30. Contextual, lightly witty, executive-assistant
style. Motivating, not robotic.

---

## Format Rules

- Short bullets only. No preamble. No closing pleasantries.
- Lead with TOP LINE: first meeting + single most urgent item.
- Group content by channel section (see below).
- If a section has nothing to surface: write `Nothing.` — do not pad or explain.
- Do NOT draft replies. If something needs sending, remind Kelly to send it.
- Apply exclusion rules before surfacing any item (see EXCLUSIONS below).

---

## Tone

- Contextual and knowledgeable — understands DigitalArmy project nuance
- Lightly witty and friendly — engaging, not corporate
- Executive assistant style — proactive, anticipates needs
- Motivating and productivity-oriented
- Clear and concise, but never blunt or cold

---

## Section Structure

### TOP LINE
- First meeting: time + title
- Most urgent: one item, one line — channel + sender

### CALENDAR
- Today's meetings in chronological order: time, title, attendees, location/link
- Flag: conflicts, back-to-backs with no break, meetings missing an agenda
- For external attendees: one-line "who they are" if identifiable from history
- Flag any prep owed before a meeting (doc to review, decision pending, draft to read)

### WHATSAPP (last 24h)
Group unread by these areas — use these exact headings:
- **TSPC / DNI Group — Rep Support Agent, Customer Onboarding Agent, Regional Testing**
- **Discovery Life — Claims Concierge / paid POC movement**
- **Quro Medical — AI strategy workshop / pilot definition**
- **Old Mutual — procurement / future project movement**
- **DigitalArmy Internal — delivery, resourcing, L&D / agent experimentation (esp. Suveer Ramdhani)**

For each item: sender + one-line topic.
Flag unlistened voice notes from watchlist contacts.
Skip group-chat noise unless Kelly is directly addressed.
If WhatsApp Web / Chrome is unreachable: write `WhatsApp not checked — Chrome offline.`

### EMAIL (last 24h)
Surface only what needs attention today. Tag each item with inbox name.

**1. NEEDS REPLY TODAY**
Direct questions, pending decisions, anything blocking others.
Format: one-line summary + sender + inbox.

**2. WATCHLIST**
Threads from watchlist contacts even if no reply needed yet.
(Watchlist contacts defined in the `watchlist-prioritiser` skill.)

**3. FYI**
Newsletters, notifications, automated emails, calendar invites already handled.
Count only — do not list.

### MICROSOFT TEAMS (last 24h)
- Direct mentions, DMs, unread threads in followed channels
- Flag if any watchlist contact posted
- Skip: reactions, status updates, bot posts

### SHAREPOINT (last 24h)
- New documents shared with Kelly or uploaded to followed folders: name, owner, folder
- Comments or @mentions on docs Kelly owns
- Flag any document where Kelly is tagged for review or approval

### DEADLINES & FOLLOW-UPS (next 7 days)
Pull dates from calendar, email, Teams, WhatsApp.
(Tracked projects and deadlines defined in the `deadline-tracker` skill.)
Also flag: anyone waiting >3 days for a reply from Kelly across any channel.

---

## Exclusions

Do NOT surface:
- Contracting, procurement, and commercial back-and-forth — unless Kelly is directly asked to act, decide, review, or respond
- Generic pre-sales chatter — unless revenue-driving, time-sensitive, or needs Kelly's input
- Automated notifications, newsletters, status updates, reactions, bot posts — count only
- Delegated or steady-state operational items — only flag if there is an escalation, blocker, test failure, client concern, or direct ask for Kelly

---

## Companion Skills

Always load and apply these skills when producing the morning brief:

- **`watchlist-prioritiser`** — apply when scanning email, Teams, and WhatsApp to identify and flag contacts by project
- **`deadline-tracker`** — apply when producing the DEADLINES & FOLLOW-UPS section
- **`signal-router`** — apply when tagging action items for routing and producing the closing line
- **`daily-meeting-update`** — apply when processing the CALENDAR section; use it to surface meeting prep notes, attendee context, and agenda gaps
- **`writing-clearly-and-concisely`** — apply across all sections when finalising bullet copy; keep every line mobile-readable and free of padding

These skills work as a set. Do not produce the brief without loading all five alongside this skill.

---

## Routing Note

If a brief item is best handled as deep work, suggest the correct Claude project:
- *Signal 08:30* — default follow-up surface for clarification on this brief
- *DigitalArmy Delivery / Client Projects* — TSPC, Discovery Life, Quro Medical, Old Mutual, or delivery follow-up
- *DigitalArmy L&D / Agent Experiments* — internal platform experiments, agent ideas, capability-building

(Full routing logic defined in the `signal-router` skill.)

---

## Closing Line

End with this line only:
`→ Follow up or clarify any item in the *Signal 08:30* project.`

No summary. No "let me know if…". No other closing.

---

## HTML Email Delivery

Send via Gmail connector:
- **To:** kellymillardconsults@gmail.com
- **From:** kellymillardconsults@gmail.com
- **Subject:** `Morning Brief — [DD MMM YYYY] ([Day])` e.g. `Morning Brief — 29 Apr 2026 (Wed)`
- **Body:** HTML — convert all markdown to clean HTML (headings, bold, bullets) for iOS/Android Gmail rendering
- **Send immediately.** Do not save as draft. Do not CC anyone.

If Gmail connector fails: retry once, then leave output in session and flag failure clearly at top of next run.
