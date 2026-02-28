---

## Date: 2025-11-06 — 2026-02-28
Tags: #Random #Engineering #Principles #Career

# Random Knowledge

A curated collection of engineering principles, mental models, career insights, and practical notes gathered over time.

---

## Table of Contents

- [Engineering Principles](#engineering-principles)
- [Mental Models & Systems Thinking](#mental-models--systems-thinking)
- [Frontend Engineering](#frontend-engineering)
- [Backend Engineering](#backend-engineering)
- [Software Architecture & Decision Records](#software-architecture--decision-records)
- [AI-Assisted Development](#ai-assisted-development)
- [Career & Leadership](#career--leadership)
- [Communication & Storytelling](#communication--storytelling)
- [Learning Techniques](#learning-techniques)
- [Design & UI/UX](#design--uiux)
- [Infrastructure & DevOps](#infrastructure--devops)
- [Useful Git Commands](#useful-git-commands)
- [Quotes](#quotes)
- [Color Palette](#color-palette)
- [References](#references)

---

## Engineering Principles

Ten core concepts every developer should internalize:

1. **Composition over Inheritance** — favor combining small, focused pieces over deep class hierarchies.
2. **YAGNI (You Aren't Gonna Need It)** — don't build what you don't need yet.
3. **Principle of Least Privilege** — don't expose data unnecessarily; don't give functions access to everything.
4. **Make Illegal States Unrepresentable** — design types and data structures so invalid states can't exist.
5. **Code for Humans** — readability and clarity over cleverness.
6. **Embrace Immutability** — copy data or create new instances instead of mutating in place.
7. **Think in Pipelines** — `Input -> Transform -> Output -> Transform -> Output`
8. **Understand the Cost of Abstraction** — every layer adds complexity; justify it.
9. **Accept That Refactoring Is Not Optional** — code rots; refactoring is maintenance, not rework.
10. **Your Code Will Change — Build for Now** — stop future-proofing; embrace simplicity.

Additional principles:

- **DSA** — keep it simple, predictable, and stable.
- **Configs & Secrets** — write functional code, define configuration categories, choose where secrets live, and create example configs. Small steps save hours of refactoring later.
- **Essential vs. Derived State** — distinguish between source-of-truth state and state that can be computed from it.
- **State vs. Events** — understand when to model something as persistent state versus a transient event.
- Write tests, not theories. Simplicity is king.

---

## Mental Models & Systems Thinking

> *"All programs are just data transformations."* — Mike Acton

**The Universal System Model:**

```
Input -> Process/Transformation -> Output
```

Everything is a state machine. Your code is a liability. Think in systems.

**Measuring System Thinking:**

- What is the real goal?
- Who is affected if this breaks?
- What is the definition of success?
- What changes if we do this?

**Data Flow Principles:**

- Data goes **DOWN** via props
- Events go **UP** via functions
- Track the state; make it small and isolated
- Don't modify data — copy or create new (immutability)

**Pointers & Variables:**

- Pointers = addresses in memory
- Variables = labels for memory locations
- Pass by value vs. pass by reference
- Everything is data: what data do I have? Code like it's obvious.

---

## Frontend Engineering

**Core Concepts:** Components, State, Props, Lifecycle

The frontend engineering lifecycle spans three phases — **Build**, **Deployment**, and **Runtime** — each with distinct concerns:

Frontend Engineering Lifecycle

*Figure: The frontend lifecycle from build through deployment to runtime, covering SSR, bundling, caching, state management, error handling, accessibility, and more.*

**JavaScript Event Loop:**

- **Heap** — memory allocation
- **Call Stack** — execution context
- **libuv** — async I/O (Node.js)
- **Task Queue** — macrotasks (setTimeout, I/O)
- **Microtask Queue** — promises, queueMicrotask

---

## Backend Engineering

**Core Concepts:** Routes, Controllers, Services, Models

**Key Infrastructure Patterns:**


| Pattern           | Purpose                                      |
| ----------------- | -------------------------------------------- |
| **Reverse Proxy** | Forwards client requests to backend servers  |
| **Load Balancer** | Distributes requests across multiple servers |
| **API Gateway**   | Manages, routes, and secures API traffic     |


**GraphQL / DataLoader** — batch and cache database requests to avoid N+1 query problems.

---

## Software Architecture & Decision Records

Recording architectural decisions is a critical engineering habit. The format doesn't matter — the habit of recording does.

Recording Decisions — ADR Example

*Figure: An Architecture Decision Record (ADR) captures what you chose, why, and what you considered. From "Learn Out Loud: From Prototype to Production" with Alan Knox.*

ADR Workflow in Cursor

*Figure: Using AI to generate and manage ADRs directly in the IDE — surfacing decisions before deployment.*

### The Full Methodology

The same three steps work at every stage of the software lifecycle — from Idea through Design, Architecture, Plan, Build, Deploy, Operate, and Evolve:

The Full Methodology

*Figure: At every stage, the same habit: (1) Surface the decisions being made, (2) Explore options and understand tradeoffs, (3) Decide consciously and record your reasoning.*

### What to Do Next

AI-Assisted Decision Making

*Figure: Actionable next steps — ask your AI to audit your code, pick the scariest answer and explore it, record what you decide, and repeat from the start.*

### ADR Workflow (Practical Example)

**Step 1 — Surface decisions before deploying:**

> *"I'm ready to deploy this project in production. Study my project and suggest decisions that we should make before deploying. Create a list of decisions in `/docs/decisions` and for each decision add an ADR file so that we can track the decision-making later."*

**Step 2 — Evaluate each decision:**

> *"Check the updated ADRs. For each decision, recommend the best and simplest option, then suggest the 2nd best. Explain why you came up with the decision, list strengths, weaknesses, and tradeoffs. Finally, tell me your assumptions."*

### Contingency for Architectural Integrity

- Own it
- Explain it
- Stand by it

---

## AI-Assisted Development

### How Cursor Works

Cursor's Composer agent receives a query and uses a set of tools to accomplish tasks autonomously:

How Cursor Works

*Figure: The Cursor agent flow — User query is processed by the Composer agent, which selects from tools: Read File, Edit File, Codebase Search, Collect Lints, and Terminal Command.*

### Workflow Modes


| Mode          | Purpose                                   |
| ------------- | ----------------------------------------- |
| **Research**  | Gather context and understand the problem |
| **Plan**      | Design the approach and surface decisions |
| **Implement** | Execute the plan with the agent           |


Equivalent in Cursor: **Ask -> Plan -> Agent**

**Sub-agents** guide the main agent by handling specialized sub-tasks.

### You Are the Driver When Using AI

1. **Surface decisions** — what choices need to be made?
2. **Understand tradeoffs** — what are the pros and cons?
3. **Make choices** — decide consciously and record reasoning.

### Recommended AI Model Usage


| Model         | Best For            |
| ------------- | ------------------- |
| Opus          | Coding (most tasks) |
| GPT-5.3 Codex | Debugging           |
| Gemini Pro 3  | UI/UX               |
| Composer 2    | Testing             |


### Key Documents


| Document                                | Owner                        |
| --------------------------------------- | ---------------------------- |
| **PRD** (Product Requirements Document) | Product Owner / Team         |
| **Decision Record** (ADR)               | Architect / Engineering Team |


---

## Career & Leadership

### Demonstrating Impact

Frame your work in terms of business outcomes:

- **Revenue** — how does it drive income?
- **Risk** — what risk does it mitigate?
- **Cost** — what cost does it reduce?
- **TTM (Time to Market)** — how does it accelerate delivery?

**Impact Formula:**

- What I did
- What outcome it produced
- What problem it avoided

**Example:** *"Improved login latency by 25%."*

### Business Acumen for Engineers

- What business problem does it solve?
- Understand the industry and business constraints
- Discuss the advantage of the investment
- Solve the business problem that matters today
- Understand the business context

### Impact Language


| Category             | Description                          |
| -------------------- | ------------------------------------ |
| Reduced Exposure     | Decreased risk or attack surface     |
| Increased Efficiency | Faster, cheaper, or more automated   |
| Strategic Enablement | Unlocked new capabilities or markets |
| Risk Mitigation      | Prevented potential failures         |


### Leadership Without a Title

- **Skill = Execution** — deliver results consistently
- **Authority = Trust** — earned through reliability
- Write decision docs
- Record tech talks
- Lead without a role

**Meetings:** Name them *"Recap and Next Steps"* — always end with clarity.

**Architecture:** Components -> Modules (think in composable units)

---

## Communication & Storytelling

### The BPAS Framework


| Step             | Description                       |
| ---------------- | --------------------------------- |
| **B** — Big Idea | Lead with the core insight        |
| **P** — Problem  | Define the pain point             |
| **A** — Amplify  | Show the consequences of inaction |
| **S** — Solution | Present your approach             |


### Narrative Structure

**Hook -> Tension -> Climax -> Resolution**

### How to Whiteboard

- **What** — define the concept
- **Why** — explain the motivation
- **How** — walk through the mechanics

**Goal:** Understand by breaking down. Answer any questions.

### How to Create a Mind Map

1. Start with ideas
2. Create frameworks to support them
3. Say it out loud

Break down the problem into its most basic components. Organize main ideas in a structured way: **What -> Why -> How**.

---

## Learning Techniques

### The Feynman Technique (First Principles)

1. **Choose a Concept & Study** — select a topic, research it, and write down everything you know on a blank sheet of paper.
2. **Teach It Simply** — explain the topic as if teaching a child, using simple, non-technical language.
3. **Identify Gaps & Review** — note areas where you struggled, then return to source materials to fill those gaps.
4. **Simplify & Use Analogies** — create a final, concise narrative or analogy that makes the concept intuitive.

### Train of Thought & Belief Systems

Your mental frameworks shape how you approach problems. Be intentional about the beliefs and thought patterns you adopt — they become your default problem-solving toolkit.

---

## Design & UI/UX

### Four Rules for Effective Landing Pages

1. Users must know what you do within **3 seconds**
2. Avoid AI slop — no generic purple gradients, abstract glows, or stock imagery
3. **Show, don't tell** — demonstrate value, skip the fluff
4. Clear hierarchy and CTAs > aesthetics

### Color Palette

Color Palette


| Swatch      | Hex Code  |
| ----------- | --------- |
| Blue        | `#7FB3E1` |
| Purple      | `#CB96E2` |
| Teal        | `#75E0D9` |
| Accent Blue | `#68B8FF` |


---

## Infrastructure & DevOps

### Web Standards Bodies

- **HTTP Working Group (HTTPWG)** — develops and maintains the HTTP protocol specifications
- **Internet Engineering Task Force (IETF)** — develops and promotes internet standards

---

## Useful Git Commands

```bash
# Revert a specific commit without editing the message
git revert 2c0ae1a --no-edit

# View the last 5 commits in one-line format
git log --oneline -5

# Show files changed in a specific commit
git show 2c0ae1a --stat

# Check the latest commit on origin/main
git log origin/main -1 --format="%H %s"

# Trigger CI/CD with an empty commit
git commit --allow-empty -m "chore: trigger CI/CD workflow"
```

---

## Quotes

> *"Don't compare yourself to others. Compare yourself to who you were yesterday."*
> — Jordan Peterson

> *"I don't wish for an easy life. I wish for the strength to handle a difficult life."*
> — Bruce Lee

---

## References

### Videos


| Topic                           | Link                                                   |
| ------------------------------- | ------------------------------------------------------ |
| Software Engineering Principles | [YouTube](https://www.youtube.com/watch?v=sWDJB_7PvpY) |
| 10 Concepts for Developers      | [YouTube](https://www.youtube.com/watch?v=_qS11aeMn1U) |
| Engineering Career Growth       | [YouTube](https://www.youtube.com/watch?v=pbiXEGnFzoY) |
| Green Software                  | [YouTube](https://www.youtube.com/shorts/6du8CImc5Ik)  |
| Modern Web Vitals               | [YouTube](https://www.youtube.com/watch?v=xYoTbKJGSLE) |
| Confidence                      | [YouTube](https://www.youtube.com/watch?v=jiJ-wZch_vQ) |
| Communication                   | [YouTube](https://www.youtube.com/watch?v=btWlBHE0pe4) |
| Systems Thinking                | [YouTube](https://www.youtube.com/watch?v=Q_sjBeCDNV0) |
| Systems Thinking (ST)           | [YouTube](https://www.youtube.com/watch?v=ECT9UizeneM) |
| Architecture Decisions          | [YouTube](https://www.youtube.com/watch?v=DQH0g3nKkU4) |
| Decision Records                | [YouTube](https://www.youtube.com/watch?v=-FilDF45U1s) |
| AI Agents                       | [YouTube](https://www.youtube.com/watch?v=g24tJk8Flsk) |


### Key Figures

- **Matt Huang** — technology and venture capital
- **Mike Acton** — data-oriented design, "All programs are just data transformations"
- **Alan Knox** — "Learn Out Loud: From Prototype to Production"

---

*Last updated: 2026-02-28*