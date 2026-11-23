# TA Modular Mentor

A modular, adaptive, and deliberately critical AI mentor for writing an Indonesian academic thesis (**KTI / TA D3, Skripsi / TA D4 & S1 including Creative/Design TA, and S2 Master's Thesis**). It helps a student go from "I have no idea where to start" to a defense-ready draft — across campuses, disciplines, and writing tools — without locking onto a single title, object, or method before the student has actually decided.

The skill itself is written in Indonesian for mentoring, while academic drafts and text audits automatically adapt to the manuscript language (**Indonesian** per EYD V/KBBI or **academic English**, including bilingual abstracts and international programs).

## What it does

- **Gentle onboarding & triage when stuck.** Greets new users with a compact 6-entry-point menu instead of immediate interrogation, and turns a messy brain dump into a current position, the real blocker, and one concrete 15-minute action away from the chat.
- **Adaptive pedagogy & tiered visual explainer.** Reads the user's thinking flow and academic literacy naturally from conversation (without questionnaires), bridges everyday analogies to formal academic phrasing for beginners while staying sharp for advanced S2 users, switches angles instead of repeating the same words when confused, and scales visual explanations across 4 honest tiers (interactive diagrams -> images/Mermaid -> clean text schematics -> spoken spatial analogies in Voice Mode).
- **Trigger-driven automatic learning memory.** Automatically updates a privacy-safe learning profile whenever one of 5 conversation triggers fires (proven learning style, detected/upgraded language tier, thinking pattern/cognitive load, direct user correction, or discipline/direction shift) using native agent memory/local files, optional Google Drive tab, or a copy-pasteable Memory Card fallback — suspended during *Real Exam Mode*.
- **Explores topics across all disciplines.** Tests title candidates against four research tracks (field/institution, human respondents, experiment/design, secondary/literature/legal data), data availability, remaining time, and study level.
- **Writes and audits Chapters 1–5 & Abstract.** Enforces full traceability across research questions, objectives, methods, and discussion; builds the Chapter 2 literature matrix and gap; guides original literature synthesis (Turnitin similarity-check friendly, always with mandatory citations); and audits Chapter 4 discussion, Chapter 5 conclusions/limitations, and abstracts.
- **Designs data instruments with a Plan B.** Interview/FGD guides, questionnaires, observation sheets, testing protocols, and secondary data checklists — paired with operational fallback plans and chat data anonymization reminders.
- **Audits methodology & recommendations.** Adapts across qualitative, quantitative/experimental, legal/SLR, IT/system and structured Creative/Design TA workflows, and risk/decision approaches, rejecting vague normative recommendations in favor of concrete, measurable artifacts.
- **Prepares supervisor meetings.** Compresses progress into three verified points plus two sharp decision questions before the meeting; breaks raw supervisor revision notes into prioritized actions afterward.
- **Runs a red-team defense simulation.** Pre-flight checks thesis inputs before Question 1, enforces strict 1-examiner-per-turn pacing across four Indonesian examiner archetypes, supports text chat and Voice Mode (such as Gemini Live or similar voice tools), enforces leak-free *Real Exam Mode* with `pause`/`selesai` controls, and closes with an evidence-based evaluation report.

## Core principles

1. **Campus guidelines first & academic integrity (Anti-Ghostwriting).** The student's official campus thesis guideline always takes highest priority over default chapter structures or citation styles. The mentor outlines, audits logic, polishes student drafts, and gives at most one sample paragraph — it refuses to fabricate data or ghostwrite an entire chapter from scratch.
2. **User-adaptive pedagogy, tiered visuals, & trigger-driven memory.** Calibrates language level, real-world analogies, and 4-tier visual explainers to how the user actually thinks and what the host app supports (never fabricating image URLs), and updates a privacy-safe learning profile automatically on conversation triggers (held back during active *Real Exam Mode* turns).
3. **No yes-man, evidence required.** Wrong or unsupported claims are corrected with verifiable sources — never invented citations. Presentation adapts by phase and user profile: accessible reasoning paired with strict `[TERVERIFIKASI]`, `[ASUMSI - BUTUH BUKTI]`, and `[KELIRU / PERLU KOREKSI]` labels during draft audits and defense evaluation (explicitly suspended during active *Real Exam Mode* turns until the final report).
4. **Modular, never committed to one title.** Topics, titles, research objects, and methods stay adjustable slots until the student finalizes them explicitly.
5. **Answer calibrator.** For long-winded or circular explanations during strict audit phases, it runs a three-step calibration: short diagnosis → calibrated answer (one-sentence core, supporting evidence, scope link) → substance check. Held back during early brainstorming and active *Real Exam Mode* turns.
6. **Cross-platform documentation & privacy.** Works seamlessly with MS Word, LaTeX/Overleaf, Notion, or plain chat via copy-pasteable Blueprint summary blocks and Learning Memory Cards, with optional Google Drive / Docs (`00 - TA Master Hub`) sync only when Drive access is enabled and active. Reminds users to anonymize sensitive names (institutions, patients, students, informants) before pasting raw data into chat, and keeps personal identifiers out of automatic memory.

## Attribution

On the first activation of the skill in each session, the agent opens with exactly one line:

```text
TA Modular Mentor aktif — by Bima Chakti Adi Surya.
```

The same line is used when the skill is introduced at installation time. It is not repeated on later turns in the same session. The author is also recorded in the `description` and `metadata.author` fields of `SKILL.md`, in the license, and in this file.

## Modules

| Module | Purpose |
| --- | --- |
| 0 — Triage & Anti-Stuck | Unblock the student; end with one concrete 15-minute action |
| 1 — Exploration, Construction, Literature & Writing | 4-track feasibility gate, title construction, Chapter 2 matrix & original synthesis, full-traceability audit |
| 2 — Instruments & Data Collection Strategy | Research-track aligned tools with operational Plan B and anonymization reminders |
| 3 — Methodology, Chapter 4–5, Abstract & Recommendation Audit | Cross-discipline & Creative/Design method audit, Ch. 4 discussion & Ch. 5/Abstract checks, concrete recommendations |
| 4 — Presentation & Defense Simulation | 8–10 slide skeleton, speaker script, pre-flight check, 4 examiner archetypes, leak-free Real Exam / Coaching Mode |
| 5 — Supervision & Revision Breakdown | Pre-meeting briefing and post-meeting prioritized revision list |

The student can switch modules at any point.

## Repository structure

```text
.
├── SKILL.md                                  # Lean routing brain, 7 core rules, and negative triggers
├── README.md                                 # Project overview and installation guide
├── LICENSE                                   # MIT License
└── references/
    ├── adaptive-pedagogy.md                  # 3-tier language ladder, 4-tier visual explainer, trigger-driven auto-memory
    ├── evidence-and-calibration.md           # Claim labels, Real Exam override, anti-hallucination, 3-step calibrator
    ├── modular-workflow.md                   # Module 0–5 protocols, Ch. 5 & Abstract checks, Creative/Design flow, local/Drive fallback
    ├── defense-simulator.md                  # Slide prep, pre-flight check, examiner archetypes, chat vs Voice Mode
    └── verification-scenarios.md             # 6 behavioral & pressure test scenarios for auditing skill changes
```

`SKILL.md` holds the always-active core rules and module routing. The files in `references/` act as the single source of truth for detailed operational protocols loaded on demand.

## Compatible AI Platforms & Recommended Setup

| Use Case | Recommended AI | Why It Fits |
| --- | --- | --- |
| **Voice Defense Simulation (Two-Way Spoken Practice)** | **Google Gemini (Gemini Live)**, **ChatGPT (Voice Mode / Advanced Voice)**, and **Claude (Voice Mode)** | Low-latency, interruptible spoken dialogue ideal for practicing against Indonesian examiner archetypes; the skill automatically drops tables/markdown and switches to concise spoken cues (Visual Tier 4). |
| **Interactive Diagrams & Visual Explanations (Visual Tiers 1–2)** | **Claude (Artifacts)**, **Google Gemini (Canvas & image generation)**, and **ChatGPT (Canvas & image generation)** | Renders clickable/interactive diagrams, Mermaid flowcharts, or concept illustrations side-by-side with mentoring. |
| **Full Native `SKILL.md` Loading & Local Auto-Memory (Layer 1)** | **Claude Code**, **Google Antigravity**, **Gemini CLI**, **OpenAI Codex CLI**, **Cursor**, **GitHub Copilot (VS Code)**, and **Windsurf** | Natively loads `SKILL.md` + on-demand `references/` and updates a local learning profile file automatically on triggers. |
| **Optional Google Drive / Docs Sync (`00 - TA Master Hub`)** | **Google Gemini (Google Workspace / Drive enabled)** and Drive-connected agents (e.g., **Google Antigravity** or **Claude** with Google Drive integration) | Reads and updates `00 - TA Master Hub` including the **Profil & Gaya Belajar** tab without manual copy-paste. |
| **Plain Web Chat / No-Install Workflow** | Any standard chat app (**ChatGPT**, **Gemini**, **Claude**, etc.) | Works fully via copy-pasteable Blueprint blocks, Learning Memory Cards, and clean text schematics. |

## Installation

### Option A — Native `SKILL.md` Agents

Copy this repository — or `SKILL.md` and the `references/` folder together — into a directory named `ta-modular-mentor` inside the skills directory of an AI agent that supports `SKILL.md`-style skills. For example:

```bash
git clone https://github.com/Luciansvon/Skill-Mentor-TA-Skripsi.git \
  .claude/skills/ta-modular-mentor
```

If you install manually (e.g., via ZIP download) or target a cross-runtime directory such as `.agents/skills/ta-modular-mentor`, rename the folder to `ta-modular-mentor` so it matches the `name: ta-modular-mentor` field in `SKILL.md`, and keep `references/` right beside `SKILL.md` because relative paths load from there.

### Option B — Chat & Voice Apps (Gemini Live, ChatGPT Voice, Claude Web/Mobile)

If you prefer a regular chat or voice app without installing local agent tools:

- **ChatGPT & Claude:** Upload `SKILL.md` and the `references/` files into a **Project** (or paste `SKILL.md`, `references/defense-simulator.md`, and a short summary of your Title, Research Questions, and Method at the start of a chat), then turn on **Voice Mode** in that conversation to run a spoken defense simulation.
- **Google Gemini & Gemini Live:** Load the instructions via **Gemini Gems / Skills**, or prime a regular chat with `SKILL.md`, `references/defense-simulator.md`, and your thesis summary before switching to **Gemini Live** *(note: direct Gem or Skill support inside Live voice sessions can vary depending on account rollout, so priming a regular chat first is the most reliable path)*.

## Usage

The skill activates when the user works on a thesis-related task (and explicitly avoids triggering on short coursework, business slides, or non-academic projects). Example prompts:

- "Halo, kamu bisa bantu apa buat skripsiku?"
- "Aku benar-benar nggak paham bahasa formal penelitian kayak rumusan masalah sama triangulasi, tolong jelasin pakai bahasa biasa buat TA desain furnitur."
- "Aku lebih cepat paham kalau lihat bagan. Gambarkan diagram alur nyambungnya Bab 1 sampai Bab 4."
- "I'm stuck, I have a pile of notes and no title. Help me start."
- "Audit my Chapter 4 discussion — is it connected enough to Chapter 2?"
- "Turn these journal findings into a Chapter 2 gap matrix."
- "Break my supervisor's revision notes into a prioritized action list."
- "Simulate my defense with a panel of 3 examiners in Real Exam Mode."

It works in text chat and in voice sessions (such as Gemini Live or similar voice tools); both the adaptive visual explainer and the defense simulator automatically switch to concise, symbol-free spoken explanations in Voice Mode.

## Author

Bima Chakti Adi Surya — [GitHub](https://github.com/Luciansvon)

## License

[MIT](LICENSE) © 2026 Bima Chakti Adi Surya
