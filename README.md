<!-- Showcase repository: the product is real and in use, its source code is private. -->

<a href="https://bym.agentbuff.id"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg"><img src="assets/banner-light.svg" width="100%" alt="Buff Your Money. A personal and family finance app that your AI agent fills in from a chat message."></picture></a>

<p align="center"><a href="https://bym.agentbuff.id"><b>Open bym.agentbuff.id</b></a> · <a href="https://github.com/nugrahalabib">More of my work</a> · <a href="https://nugrahalabib.com">nugrahalabib.com</a> · <a href="mailto:nugrahalabib@gmail.com">Email</a></p>

## Overview

Buff Your Money is a web and phone app for personal and family finances. It is sold on the AgentBuff marketplace and connects to the user's own AI agent over MCP.

People stop tracking money because typing every expense is tedious. Here the user writes "lunch 35k with GoPay" to the agent in WhatsApp or Telegram, and the app records it.

There is no LLM inside the app. The agent does the language work. The app does parsing and money math deterministically, so a number is the same every time.

| | |
| --- | --- |
| **Status** | Live at [bym.agentbuff.id](https://bym.agentbuff.id) |
| **Role** | Designed and built by Nugraha Labib Mujaddid as a first-party app on the AgentBuff marketplace. |
| **Period** | Since Sep 2026 |
| **Source** | Private. This repository presents the product; the code is not published. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/features-dark.svg"><img src="assets/features-light.svg" width="100%" alt="What Buff Your Money does: Quick entry by chat, Budgets and goals, Debts and zakat, Tax asset list, Financial independence, Statement import, Family members, Undoable agent actions."></picture>

<details>
<summary>Features as text</summary>

- **Quick entry by chat.** A deterministic parser reads amounts, dates and context from a short sentence and files the transaction.
- **Budgets and goals.** Monthly budgets, savings goals and a safe-to-spend figure until the next payday.
- **Debts and zakat.** Plan how to pay off debts, and calculate zakat from your own records.
- **Tax asset list.** Gather the assets and income figures needed for an annual tax return in one list.
- **Financial independence.** Simulate financial independence targets, including a Monte Carlo run on your own numbers.
- **Statement import.** Import bank statements from PDF and spreadsheet files, plus portfolio files, instead of typing them.
- **Family members.** Invite family members into a shared book, each with their own login.
- **Undoable agent actions.** Every action by the agent is logged, and the user can undo recent ones.

</details>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg"><img src="assets/architecture-light.svg" width="100%" alt="How Buff Your Money is built. Docker Compose on a VPS with three database roles, a worker, backup before every deploy and a restore drill."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg"><img src="assets/stack-light.svg" width="100%" alt="Buff Your Money stack: Frontend Next.js 16, React 19, Tailwind 4, TanStack Query; Backend Next.js server, MCP server, pg-boss queue; Data PostgreSQL 16, Drizzle ORM, decimal.js; AI None inside the app, MCP for the user's agent; Ops Docker Compose, GitHub Actions CI, Vitest, Playwright."></picture>

## Engineering highlights

- Money is stored in minor units and calculated with a decimal library, never with floats.
- Row-level security and separate database roles for migration, app and worker.
- A deploy backs up first, then counts rows, and fails if any table shrinks.
- The app ships with a data protection impact assessment and an account deletion workflow.

## Screens

<img src="assets/screens/screen-1.jpg" width="100%" alt="Landing page">

<sub>Landing page</sub>

---

<sub>Built by [Nugraha Labib Mujaddid](https://github.com/nugrahalabib). This page describes a private codebase; questions about the product or a demo are welcome at [nugrahalabib@gmail.com](mailto:nugrahalabib@gmail.com).</sub>
