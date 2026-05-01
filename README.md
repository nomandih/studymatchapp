# StudyMatch

A mobile-first prototype that connects Hong Kong secondary school students with compatible study partners. Built for the **HK Junior Achievement Business Startup Competition**.

> Find your person. Ace your exams.

## What it is

StudyMatch is a Tinder-style swipe interface for HKDSE candidates (S4–S6) to find study partners by subject, **specific syllabus topic**, school level, study style, and availability. Profiles are **text-only** — no photos — keeping the focus on academic compatibility and protecting minors from inappropriate content.

A built-in **Pomodoro timer** keeps users locked in during a study session, and the timer keeps running as a floating widget even when they leave the Focus tab.

## Live prototype

**🔗 Try it now: [nomandih.github.io/studymatchapp](https://nomandih.github.io/studymatchapp/)**

Or open [StudyMatch.html](StudyMatch.html) directly in any modern browser. No build step, no install — it loads React, ReactDOM and Babel from CDN and renders a fully interactive iPhone-style mockup that auto-adapts to fullscreen on mobile widths.

## Screens

| # | Screen | What it does |
|---|---|---|
| 1 | Onboarding | Logo, value props, EN/中文 toggle, school email gate (`.edu.hk`) |
| 2 | Profile Setup | Name, school, year, subjects, study style, availability |
| 3 | Home | Browse / Create quick actions, recent matches, stats |
| 4 | Browse | Drag-to-swipe card deck with CONNECT / PASS overlays + topic filter sheet |
| 5 | Create Card | Live preview, bio, subjects with **per-subject topic drill-down**, study style, location |
| 6 | Match | Confetti reveal, dual avatars, Start Chatting CTA |
| 7 | Chat | Threaded messaging, Book-a-session banner |
| 8 | Schedule | Date / time / location picker, confirmation state |
| 9 | Profile | Editable bio, stats, language toggle, settings, sign out |
| 10 | Focus | Pomodoro timer with circular progress ring, work/break modes, persistent floating widget |

## Key features

- **Verified students only** — `.edu.hk` school email gate (Phase 1), school roster integration (Phase 2)
- **No photos** — eliminates appearance-based harassment and removes an entire category of moderation risk
- **Two-layer content moderation** — automated keyword + toxicity API filtering, plus human review queue
- **HKDSE syllabus-aware matching** — every subject (Physics, Chemistry, Biology, Maths with M1/M2, Economics, History, Chinese History, Geography, English, Chinese, Citizenship & Social Development, BAFS, ICT) breaks down to its official compulsory + elective topics. Pick *exactly* what you need help with — e.g. Geography C5 (Combating Famine) — and find a partner studying the same thing.
- **Topic-aware Browse filter** — slide-up sheet with collapsible subject accordions. Active filters highlight matching codes on each card with a glow.
- **Built-in Pomodoro timer** — 5th tab in the bottom nav. Customisable work / break durations (15/25/30/45/60 work, 5/10/15/20 break), session counter, mode auto-switching with toast notifications, and a floating timer pill that persists across all other tabs while running.
- **Bilingual UI (EN / 繁體中文)** — toggle exposed at registration and in profile settings; every label, syllabus topic name, school placeholder, and toast is fully translated.
- **PDPO-compliant by design** — parental consent flow, data minimisation, right to erasure

## Subject syllabus coverage

All 13 HKDSE subjects are wired with their official topic codes and bilingual names:

| Subject | Compulsory | Elective |
|---|---|---|
| Physics | C1–C5 | E1–E4 |
| Chemistry | C1–C11 | E1–E3 |
| Biology | C1–C4 | E1–E4 |
| Maths | C1–C4 | M1, M2 |
| Economics | C1–C10 | E1–E2 |
| History | C1–C3 | E1–E3 |
| Chinese History | C1–C2 | E1–E5 |
| Geography | C1–C7 | E1–E4 |
| English | P1–P5 (skill-based) | — |
| Chinese | P1–P5 (skill-based) | — |
| Citizenship & Social Dev | T1–T3 | — |
| BAFS | C1–C2 + strand | E1 |
| ICT | C1–C5 | E1–E3 |

## Stack (prototype)

- Single-file HTML + React 18 (loaded from unpkg)
- Babel Standalone for in-browser JSX
- DM Sans (Google Fonts)
- Pure inline styles — no CSS framework
- SVG-based circular progress ring for the Pomodoro timer

## Stack (production plan)

- **Frontend:** Flutter (iOS + Android, single codebase)
- **Backend:** Firebase (Auth, Firestore, Cloud Functions)
- **Chat:** Stream Chat API
- **Moderation:** Google Perspective API + custom Cantonese/English blocklist
- **Timer state:** background service for Pomodoro persistence + push notifications

## Target market

- ~50,000 HKDSE candidates per year
- Pilot: 3–5 schools, ~3,000 students
- Expansion: Macau, Taiwan, other exam-driven education markets

## Roadmap

- **Q1 2027** Research, user interviews, Figma v1
- **Q2 2027** MVP — text profiles, swipe UI with topic filter, school email verification, Layer 1 moderation, Pomodoro timer
- **Q3 2027** Pilot with 1 school, 200 beta users, human review queue
- **Q4 2027** Open launch, premium subscription, school licensing

## Repo contents

```
StudyMatch.html              Standalone interactive prototype
README.md                    This file
```

## License

Prototype submitted for the HK Junior Achievement Business Startup Competition. All rights reserved by the team.
