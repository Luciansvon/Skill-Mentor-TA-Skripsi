# TA Modular Mentor

A modular, adaptive, and deliberately critical AI mentor for writing an Indonesian academic thesis (**KTI / TA D3, Skripsi / TA D4 & S1 including Creative/Design TA, and S2 Master's Thesis**). It helps a student go from "I have no idea where to start" to a defense-ready draft — across campuses, disciplines, and writing tools — without locking onto a single title, object, or method before the student has actually decided.

The skill itself is written in Indonesian for mentoring, while academic drafts and text audits automatically adapt to the manuscript language (**Indonesian** per EYD V/KBBI or **academic English**, including bilingual abstracts and international programs).

## What it does

- **Gentle onboarding & triage when stuck.** Greets new users with a compact 6-entry-point menu instead of immediate interrogation, and turns a messy brain dump into a current position, the real blocker, and one concrete 15-minute action away from the chat.
- **Explores topics across all disciplines.** Tests title candidates against four research tracks (field/institution, human respondents, experiment/design, secondary/literature/legal data), data availability, remaining time, and study level.
- **Writes and audits Chapters 1–5.** Enforces full traceability across research questions, objectives, methods, and discussion; builds the Chapter 2 literature matrix and gap; guides original literature synthesis (Turnitin similarity-check friendly, always with mandatory citations); and audits Chapter 4 discussion against Chapter 2 theory.
- **Designs data instruments with a Plan B.** Interview/FGD guides, questionnaires, observation sheets, testing protocols, and secondary data checklists — paired with operational fallback plans and chat data anonymization reminders.
- **Audits methodology & recommendations.** Adapts across qualitative, quantitative/experimental, legal/SLR, IT/system/design R&D, and risk/decision approaches, rejecting vague normative recommendations in favor of concrete, measurable artifacts.
- **Prepares supervisor meetings.** Compresses progress into three verified points plus two sharp decision questions before the meeting; breaks raw supervisor revision notes into prioritized actions afterward.
- **Runs a red-team defense simulation.** Pre-flight checks thesis inputs before Question 1, enforces strict 1-examiner-per-turn pacing across four Indonesian examiner archetypes, supports text chat and Voice Mode (such as Gemini Live or similar voice tools), enforces leak-free *Real Exam Mode* with `pause`/`selesai` controls, and closes with an evidence-based evaluation report.

## Core principles

1. **Campus guidelines first & academic integrity (Anti-Ghostwriting).** The student's official campus thesis guideline always takes highest priority over default chapter structures or citation styles. The mentor outlines, audits logic, polishes student drafts, and gives at most one sample paragraph — it refuses to fabricate data or ghostwrite an entire chapter from scratch.
2. **No yes-man, evidence required.** Wrong or unsupported claims are corrected with verifiable sources — never invented citations. Presentation adapts by phase: a lighter tone during early exploration; strict `[TERVERIFIKASI]`, `[ASUMSI - BUTUH BUKTI]`, and `[KELIRU / PERLU KOREKSI]` labels during draft audits and defense evaluation (explicitly suspended during active *Real Exam Mode* turns until the final report).
3. **Modular, never committed to one title.** Topics, titles, research objects, and methods stay adjustable slots until the student finalizes them explicitly.
4. **Answer calibrator.** For long-winded or circular explanations during strict audit phases, it runs a three-step calibration: short diagnosis → calibrated answer (one-sentence core, supporting evidence, scope link) → substance check. Held back during early brainstorming and active *Real Exam Mode* turns.
5. **Cross-platform documentation & privacy.** Works seamlessly with MS Word, LaTeX/Overleaf, Notion, or plain chat via copy-pasteable Blueprint summary blocks, with optional Google Drive / Docs (`00 - TA Master Hub`) sync only when Drive access is enabled and active. Reminds users to anonymize sensitive names (institutions, patients, students, informants) before pasting raw data into chat.

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
| 3 — Methodology, Chapter 4 & Recommendation Audit | Cross-discipline method audit, 4-step Chapter 4 discussion check, concrete recommendations |
| 4 — Presentation & Defense Simulation | 8–10 slide skeleton, speaker script, pre-flight check, 4 examiner archetypes, leak-free Real Exam / Coaching Mode |
| 5 — Supervision & Revision Breakdown | Pre-meeting briefing and post-meeting prioritized revision list |

The student can switch modules at any point.

## Repository structure

```text
.
├── SKILL.md                                  # Lean routing brain, core rules, and negative triggers
├── LICENSE                                   # MIT License
└── references/
    ├── evidence-and-calibration.md           # Claim labels, Real Exam override, anti-hallucination, 3-step calibrator
    ├── modular-workflow.md                   # Module 0–5 protocols, 4-track gate, Ch. 4 audit, local/Drive fallback
    └── defense-simulator.md                  # Slide prep, pre-flight check, examiner archetypes, chat vs Voice Mode
```

`SKILL.md` holds the always-active core rules and module routing. The files in `references/` act as the single source of truth for detailed operational protocols loaded on demand.

## Installation

Copy this repository — or just `SKILL.md` and the `references/` folder together — into the skills directory of an AI agent that supports `SKILL.md`-style skills. For example, with Claude Code:

```bash
git clone https://github.com/Luciansvon/Skill-Mentor-TA-Skripsi.git \
  .claude/skills/ta-modular-mentor
```

Keep `SKILL.md` at the root of the skill folder and keep `references/` beside it; the skill loads those reference files by relative path.

## Usage

The skill activates when the user works on a thesis-related task (and explicitly avoids triggering on short coursework, business slides, or non-academic projects). Example prompts:

- "Halo, kamu bisa bantu apa buat skripsiku?"
- "I'm stuck, I have a pile of notes and no title. Help me start."
- "Audit my Chapter 4 discussion — is it connected enough to Chapter 2?"
- "Turn these journal findings into a Chapter 2 gap matrix."
- "Break my supervisor's revision notes into a prioritized action list."
- "Simulate my defense with a panel of 3 examiners in Real Exam Mode."

It works in text chat and in voice sessions (such as Gemini Live or similar voice tools); the defense simulator changes its formatting and verbal cues to suit the medium.

## Author

Bima Chakti Adi Surya — [GitHub](https://github.com/Luciansvon)

## License

[MIT](LICENSE) © 2026 Bima Chakti Adi Surya
