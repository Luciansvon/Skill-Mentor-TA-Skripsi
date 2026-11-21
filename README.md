# TA Modular Mentor

A modular, adaptive, and deliberately critical AI mentor for writing an Indonesian undergraduate thesis (**Tugas Akhir / TA / skripsi**). It helps a student go from "I have no idea where to start" to a defense-ready draft — without locking onto a single title, object, or method before the student has actually decided.

The skill itself is written in Indonesian, because that is the language of the thesis, the supervisor conversations, and the defense simulation it is built for.

## What it does

- **Triage when stuck.** Turns a messy brain dump into a current position, the real blocker, and one small action that can be done away from the chat in about 15 minutes.
- **Explores topics without forcing a decision.** Tests title candidates against data availability, remaining time, field access, and the student's study level and discipline.
- **Writes and audits Chapters 1–5.** Keeps the problem statement, objectives, methods, instruments, and final output aligned 1:1; builds the Chapter 2 literature matrix and gap; paraphrases original academic prose suitable for similarity checks (Turnitin).
- **Designs field instruments.** Interview guides, observation sheets, document checklists, and expert validation forms — each tied to data that is actually analyzed, with an operational Plan B when field data is incomplete.
- **Audits methodology.** Adapts to the chosen approach (quantitative, qualitative, descriptive, case study, FMEA, SQC, system design, or others), and rejects vague normative recommendations in favor of specific, measurable ones.
- **Prepares supervisor meetings.** Compresses progress into three verified points plus two sharp decision questions before the meeting; breaks raw supervisor revision notes into prioritized actions afterward.
- **Runs a red-team defense simulation.** Four Indonesian examiner archetypes, with separate behavior for text chat and Gemini Live, plus slide/speech preparation and an evidence-based evaluation report.

## Core principles

1. **No yes-man, evidence required.** Wrong or unsupported claims are corrected, never agreed with. Every correction cites a verifiable source — textbook, industry standard/ISO, regulation, or journal. If no reliable reference exists, the skill says so instead of inventing a citation. Claim labels adapt to the phase: a lighter tone during early exploration; strict `[TERVERIFIKASI]`, `[ASUMSI - BUTUH BUKTI]`, and `[KELIRU / PERLU KOREKSI]` labels during draft audits and defense practice.
2. **Modular, never committed to one title.** Topics, titles, research objects, and methods stay adjustable slots until the student finalizes them explicitly.
3. **Answer calibrator.** For long-winded or circular explanations, it runs a three-step calibration: short diagnosis → calibrated answer (one-sentence core, supporting evidence, scope link) → substance check. Held back during free-form early brainstorming unless requested.
4. **Centralized context.** Checks the `Tugas Akhir` folder and the `00 - TA Master Hub` document in Google Drive as the single source of truth, and uses native Google Docs features (tabs, `@` smart chips, comments/suggesting, named version history) to sync progress. Sensitive personal data (full name, student ID, contact details, confidential company data) is kept out of that hub and left in official cover/draft documents only.

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
| 1 — Exploration, Construction, Literature & Writing | Feasibility gate, title construction, Chapter 2 matrix, Chapters 1–5 |
| 2 — Instruments & Field Strategy | Data collection tools aligned to the research questions, with Plan B |
| 3 — Methodology & Analysis Audit | Logic-chain, indicators, subjectivity risk, validation, usable recommendations |
| 4 — Presentation & Defense Simulation | 8–10 slide skeleton, speaker script, four examiner archetypes, evaluation report |
| 5 — Supervision & Revision Breakdown | Pre-meeting briefing and post-meeting prioritized revision list |

The student can switch modules at any point.

## Repository structure

```text
.
├── SKILL.md                                  # Skill definition, core rules, and modules
├── LICENSE                                   # MIT License
└── references/
    ├── evidence-and-calibration.md           # Claim labels, anti-hallucination rules, 3-step calibrator
    ├── modular-workflow.md                   # Module 0–5 protocols, blueprint, Drive/Docs conventions
    └── defense-simulator.md                  # Slide prep, examiner archetypes, chat vs Live behavior
```

`SKILL.md` holds the always-active rules and module routing. The files in `references/` are the detailed protocols to read when a module is activated.

## Installation

Copy this repository — or just `SKILL.md` and the `references/` folder together — into the skills directory of an AI agent that supports `SKILL.md`-style skills. For example, with Claude Code:

```bash
git clone https://github.com/Luciansvon/Skill-Mentor-TA-Skripsi.git \
  .claude/skills/ta-modular-mentor
```

Keep `SKILL.md` at the root of the skill folder and keep `references/` beside it; the skill loads those reference files by relative path.

## Usage

The skill activates when the user works on a thesis-related task. Example prompts:

- "I'm stuck, I have a pile of notes and no title. Help me start."
- "Audit my Chapter 3 method — is the data chain actually valid?"
- "Turn these journal findings into a Chapter 2 gap matrix."
- "Break my supervisor's revision notes into a prioritized action list."
- "Simulate my proposal defense with a methodology-focused examiner, in chat."

It works in text chat and in voice sessions such as Gemini Live; the defense simulator changes its formatting and role-switching cues to suit the medium.

## Author

Bima Chakti Adi Surya — [GitHub](https://github.com/LuciansVon)

## License

[MIT](LICENSE) © 2026 Bima Chakti Adi Surya
