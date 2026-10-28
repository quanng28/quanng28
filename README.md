## Who am I

I'm a second-year computer science student at Drexel University. I came to software from economics: in high school I started [EconLearner](https://econ-learner.net), an economics site that grew to more than 400,000 readers. I learn best with a real problem in front of me.

My first substantial software project was [HaneiRoom](https://www.haneiroom.com/), an AR furniture app. I started before I understood everything it would take to build it; working through the mistakes taught me how to keep learning while making something useful. I've kept that approach through [Hanei AI](https://tryhanei.app/), [GitWhy](https://gitwhy.dev), and [WhySpec](https://github.com/gitwhy-cli/whyspec). Right now I'm building [Scoot](https://github.com/quanng28/scoot) for stroke rehab and looking for the next problem worth building a startup around.

More at [quanng.me](https://quanng.me).

## What I've been building

### [Scoot](https://github.com/quanng28/scoot)

A camera-based web app for reviewing stroke-rehab exercises, built with a teammate.

**Problem:** After a stroke, much of rehab happens at home, where a clinician can't see how each exercise was done. A report that gets it wrong can hide a risky movement.

**Goal:** Give clinicians an accurate picture of each session without watching video, in a report that never says more than the measurements show.

**What I built:** On-device MediaPipe pose tracking that measures joint angles, torso lean, and movement; a repetition counter that ignores jitter and held poses and records why unreliable attempts were excluded; and Gemini reports built only from those measurements, never video or identifying data, then checked against them. Covered by 753 Vitest tests. Not in production yet.

### [GitWhy](https://gitwhy.dev)

Managing context when engineering teams coordinate with AI coding agents.

**Problem:** A commit shows what changed. When an agent wrote the change, the reasons usually stay in a chat nobody opens again.

**Goal:** Make the reason behind an AI-written change as easy to find as the diff.

**What I built:** A Go CLI and MCP server that let agents save their reasoning linked to Git commits, PostgreSQL workspace sync, and a GitHub App that posts that reasoning on pull requests. The first version saved full transcripts; testers wouldn't read them, so I replaced them with short structured notes that are 12–60x smaller.

**What happened:** Engineers at Meta, LinkedIn, Coinbase, NVIDIA, and ByteRover tested it, but it wasn't a problem they needed solved yet, and the timing was early. I stopped pursuing it as a startup; it's still online.

### [WhySpec](https://github.com/gitwhy-cli/whyspec)

Open-source spec-driven development for AI coding agents, grown out of GitWhy.

**Problem:** Spec-driven tools have an agent write a plan before it codes. Once the code exists, nobody checks which planned decisions held up and which changed.

**Goal:** Show the gap between what was planned and what was actually built.

**What I built:** A TypeScript CLI, published on npm, where the agent writes a spec before coding (intent, approach, open decisions, tasks) and records what it actually decided afterward, including anything unplanned. WhySpec lines the two up. Works with Claude Code, Cursor, Codex, and agents that use AGENTS.md.

### [Hanei AI](https://tryhanei.app/)

A furniture-sourcing and client-approval platform shaped by conversations with more than 50 U.S. interior designers.

**Problem:** Designers told us sourcing means running the same searches across catalogs again and again to match a style and a budget, then chasing client approvals separately.

**Goal:** Turn a design brief into a ranked shortlist that fits the style and budget, with client approval in the same place.

**What I built:** A Gemini function-calling agent that picks which searches to run and when to stop, with Zod-validated output. After runaway tool calls, slow serial searches, and duplicates, it now runs SerpAPI searches in parallel, deduplicates, and ranks by style and budget. I measured changes with an LLM judge on a fixed set of 50+ cases, calibrated against my own labels.

### [HaneiRoom](https://www.haneiroom.com/)

An iOS app for previewing furniture in your room with AR. Shipped on the App Store.

**Problem:** Product photos make it hard to judge how furniture will fit in a real room.

**Goal:** Let people see several pieces together in their own space before they buy.

**What I built:** I led a team of three and interviewed more than 20 college students. Multi-object placement with SwiftUI, ARKit, and RealityKit, plus disk caching, shared thumbnails, and cloned entities to fix slow repeated downloads and memory problems.

### [EconLearner](https://econ-learner.net)

An economics site I started in high school, written to explain economics clearly. With a remote team of five, I grew it to more than 400,000 readers and 1 million pageviews across 30+ countries, in nine languages.

## What I'm exploring

Alongside my software projects, I'm exploring electronics and robotics, starting with the fundamentals. I'm curious about how code interacts with sensors, motors, and the constraints of physical systems.

[LinkedIn](https://www.linkedin.com/in/quan-nguyen-321b4726a/) · [Email](mailto:qmn29@drexel.edu)
