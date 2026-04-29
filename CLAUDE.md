# CLAUDE.md — DigitalArmy.ai

## About This Repository

This is the Claude Code workspace for Kelly (Technical Junior Founding Partner, DigitalArmy.ai). All work produced here supports the design, development, and delivery of agentic AI solutions for South African enterprise clients.

---

## About DigitalArmy.ai

DigitalArmy.ai is a fully-managed AI implementation partner that builds custom autonomous AI Agents — referred to as **Digital Employees** — for South African businesses. We are not a reseller. We design, build, integrate, and support end-to-end agentic solutions.

**Core mission:** Bridge the GenAI divide for South African businesses by automating the "Human Bridge" — the armies of people currently hired to read unstructured data, interpret communications, and manually translate the real world into machine-readable formats.

**Our 10:20:70 rule:** Successful AI projects are 10% AI, 20% people, and 70% data. The AI is the engine, people are the architects, and data is the fuel.

**Key differentiators:**
- Fix-First methodology — we optimise the process before we automate it
- End-to-end partner: strategy, build, integration, and ongoing support
- Deep technical integration and custom API expertise
- Local trust: VAT-compliant, B-BBEE compliant, South African-first
- Proven track record: Cell C, Discovery Life, Sanlam, Momentum, FlySafair, Blu Label, TSPC/The Prepaid Company, and others

---

## The Team

**Kelly** — Technical Junior Founding Partner
- Focus: Production and delivery
- Responsible for: agent development, technical architecture, integration, deployment, and ongoing optimisation
- This Claude Code workspace is Kelly's primary development environment

**Suveer Ramdhani** — Senior Partner
- Focus: Commercial, Business Development, and Strategy
- Responsible for: client relationships, proposals, roadmaps, and growth

---

## Our Methodology: The Fix-First Framework

All client engagements follow this 5-step approach:

1. **Map Your Disasters or Opportunities** (1–2 weeks) — identify the worst process or biggest missed opportunity; document every step and complexity
2. **Fix It Manually First** (2–4 weeks) — streamline the process before adding technology; cut unnecessary steps and approvals
3. **Then Add AI** (4–6 weeks) — only automate excellence; if the manual process works, AI makes it exceptional
4. **Measure What Matters** (ongoing) — focus on business outcomes with clear, measurable goals
5. **Kill It If It's Not Working** (iterative) — ruthlessly focused on value; revert to simpler solutions if AI doesn't deliver

---

## Our Products: Digital Employee Types

We build agents across five optimisation categories:

**1. Operational Efficiency & Automation**
- Automated invoice processing, report generation, internal knowledge base assistants, supply chain optimisation

**2. Customer Engagement & Experience**
- Customer service drafting assistants, proactive customer support, journey mapping and friction insights

**3. Revenue Growth & Sales Automation**
- Upsell campaigns, deal engines, leads generation, end-to-end sales copilots

**4. Strategic Intelligence & Innovation**
- Financial forecasting, product ideation, hyper-personalised marketing

**5. Workforce Productivity & Enablement**
- Legal document generation, AI recruitment agents

---

## Active Projects

### TSPC (The Prepaid Company) — Agentic Transformation
- **Rep Assistant:** Proven prototype, approved for pilot. Scope: coaching, allocation explanation, extra stock decisioning, escalation, policy support inside SimTrack. Currently in production deployment phase.
- **Customer Support Agent:** Merchant-facing digital assistant embedded in the RICA mobile app (WhatsApp secondary). Scope: merchant onboarding, FAQ support, CVM lifecycle messaging, loyalty and gamification. Customer onboarding confirmed as prototype baseline.
- **Architecture principles:** Behaviour improvement, merchant-safe data only, simplicity for low-literacy users, positive reinforcement, strict governance, phased value delivery

### Discovery Life — Digital Claims Coordinator (Demo/POC)
- Agentic AI for severe illness claims, replacing paper-era forms and call centres
- Key capabilities: plain-language policy Q&A (RAG over Life Plan Guide), real-time pathology report parsing (ICD-10, TNM staging, diagnosis date extraction), claim record creation, live claim status tracking
- Design principles: zero redundant data capture, compassionate member experience, human-in-the-loop by design
- Governance: POPIA, FAIS, FSCA Explainable AI compliance built in
- Six-layer architecture: channels → reasoning engine → action library → enterprise systems → knowledge intelligence → governance

---

## Past Clients & Reference Deployments

### Cell C — AI Collections Agent
- Autonomous agent engaging customers via WhatsApp after failed payments
- Handled hundreds of thousands of cases monthly without human input
- Capabilities: multi-language support, payment gateway, document validation, escalation to Forensics/Finance/Customer Care, data capture to BI
- Reference use case: high-volume autonomous collections at scale

### BackaBuddy — AI Deployment
- Past client and reference deployment
- Use as a proof point in relevant pitches and proposals

---

## Technical Context

**Primary platforms and tools Kelly works with:**
- Claude Code (this workspace) for agent development and automation
- Agentic AI built on Claude (Anthropic) models
- WhatsApp Business API as primary customer-facing channel
- RPA for backend system integration (Apollo, SimTrack)
- RAG (Retrieval-Augmented Generation) for knowledge-grounded responses
- API-first integration design

**Agent architecture pattern:**
- Interaction channels (WhatsApp, web, email, voice, in-app)
- Reasoning engine (Claude)
- Action library (custom tools/functions per use case)
- Enterprise data & system integration
- Knowledge intelligence layer (RAG)
- Governance & human oversight (HITL, audit logging, escalation triggers)

---

## How Claude Should Work in This Workspace

- Always approach problems through the **Fix-First lens** — understand the process before automating it
- Write code and agents that are **production-ready**: error handling, logging, escalation paths, and audit trails matter
- Default to **South African context** — ZAR currency, POPIA compliance considerations, B-BBEE awareness, local enterprise client landscape
- When building agent prompts, write with **empathy and clarity** — many end users are second-language English speakers or in emotionally sensitive situations (e.g., claims)
- Favour **modular, phased delivery** — scope each capability tightly, prove it, then expand
- **Governance is not an afterthought** — every agent needs defined escalation triggers, human oversight points, and a clear audit trail

---

## Active Skills

Refer to `.claude/skills/` for the current skill stack. Skills should be applied based on their trigger conditions — Claude will load them automatically when relevant.

---

## Notes

- Kelly's GitHub: KellyDigitalArmy
- Repo: ClaudeCode
- This file should be updated as new projects are onboarded and the tech stack evolves
