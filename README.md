# StudyMatch

A mobile-first prototype that connects Hong Kong secondary school students with compatible study partners. Built for the **HK Junior Achievement Business Startup Competition**.

> Find your person. Ace your exams.

## What it is

StudyMatch is a Tinder-style swipe interface for HKDSE candidates (S4–S6) to find study partners by subject, school level, study style, and availability. Profiles are **text-only** — no photos — keeping the focus on academic compatibility and protecting minors from inappropriate content.

## Live prototype

Open [StudyMatch.html](StudyMatch.html) directly in any modern browser. No build step, no install — it loads React, ReactDOM and Babel from CDN and renders a fully interactive iPhone-frame mockup.

## Screens

| # | Screen | What it does |
|---|---|---|
| 1 | Onboarding | Logo, value props, school email gate (`.edu.hk`) |
| 2 | Profile Setup | Name, school, year, subjects, style, availability |
| 3 | Home | Browse / Create quick actions, recent matches, stats |
| 4 | Browse | Drag-to-swipe card deck with CONNECT / PASS overlays |
| 5 | Create Card | Live preview, bio, subjects, study style, location |
| 6 | Match | Confetti reveal, dual avatars, Start Chatting CTA |
| 7 | Chat | Threaded messaging, Book-a-session banner |
| 8 | Schedule | Date / time / location picker, confirmation state |
| 9 | Profile | Editable bio, stats, settings, sign out |

## Key features

- **Verified students only** — `.edu.hk` school email gate (Phase 1), school roster integration (Phase 2)
- **No photos** — eliminates appearance-based harassment and removes an entire category of moderation risk
- **Two-layer content moderation** — automated keyword + toxicity API filtering, plus human review queue
- **Bilingual UI** — toggle between English and 繁體中文 from the status bar
- **Smart matching** — algorithm scores subject overlap, availability, and study-style compatibility
- **PDPO-compliant by design** — parental consent flow, data minimisation, right to erasure

## Stack (prototype)

- Single-file HTML + React 18 (loaded from unpkg)
- Babel Standalone for in-browser JSX
- DM Sans (Google Fonts)
- Pure inline styles — no CSS framework

## Stack (production plan)

- **Frontend:** Flutter (iOS + Android, single codebase)
- **Backend:** Firebase (Auth, Firestore, Cloud Functions)
- **Chat:** Stream Chat API
- **Moderation:** Google Perspective API + custom Cantonese/English blocklist

## Target market

- ~50,000 HKDSE candidates per year
- Pilot: 3–5 schools, ~3,000 students
- Expansion: Macau, Taiwan, other exam-driven education markets

## Roadmap

- **Q1 2027** Research, user interviews, Figma v1
- **Q2 2027** MVP — text profiles, swipe UI, school email verification, Layer 1 moderation
- **Q3 2027** Pilot with 1 school, 200 beta users, human review queue
- **Q4 2027** Open launch, premium subscription, school licensing

## Repo contents

```
StudyMatch.html              Standalone interactive prototype
README.md                    This file
```

## License

Prototype submitted for the HK Junior Achievement Business Startup Competition. All rights reserved by the team.
