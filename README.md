# HPF OS & NOVA

> A local-first work environment with a voice assistant that reformulates the app's own data.

**AI-powered software ecosystem** · In daily use · Software & Artificial Intelligence  
**Source code** · proprietary and private: this repository is documentation only.

![NOVA orb, listening state · design mockup](assets/nova-orb-mockup.png)

## My role

Software architecture and development.  
The project started from organising studies, clinical work and design production in one place.

## The problem

Studies, clinical work, laboratory production, finances and projects lived in a patchwork of spreadsheets, scripts and separate tools.  
There was no single place to answer the question: what should I do now?  

## The solution

One desktop environment that turns tasks, agenda, exams and production into clear priorities, with NOVA, a voice assistant that never sees patient names.

## Key features

- Dashboard of priorities drawn from tasks, alerts, exams and invoices.
- Tasks and agenda synchronised with standard calendars.
- Revision planner across upcoming exams, with load limits per day.
- Laboratory production follow-up.
- A CAD mode that frees resources during design work.
- NOVA: local speech recognition and synthesis, optional wake word, animated orb.
- NOVA actions are bounded: open a screen, add a task or a reminder; anything else is only proposed for confirmation.

## Screenshots

All screenshots use demonstration or synthetic data.

![NOVA orb, listening state · design mockup](assets/nova-orb-mockup.png)
<sub>NOVA orb, listening state · design mockup</sub>

## Technologies

Electron · Node.js · SQLite · Python · faster-whisper · Kokoro · Piper · Anthropic Claude API

## Architecture (simplified)

![Simplified architecture of HPF OS & NOVA](assets/architecture.svg)

- Only scrubbed text reaches the language model; figures come from the app and are never computed by the model.
- Separate Python voice process with size-capped inputs and logs that record durations, never content.
- Prompt caching and a spending cap on model calls.

## Development status

- In daily use since November 2026 as the author's own workstation environment.
- NOVA voice in service since mid-November 2026; some optimisations are still under evaluation.
- Personal tool: screenshots of the live app would show personal data, so only a design mockup is shown.

## Privacy and code availability

- Local database, local speech recognition and synthesis, local wake word.
- Patient names are replaced by codes and long account numbers are stripped before any model call.
- No payment and no deletion can be triggered by the assistant.
- The source code of HPF OS & NOVA is proprietary and kept in a private repository.
- This repository contains documentation and demonstration screenshots only: no source code, configuration, data or history from the private project.
- Demonstrations can be arranged on request.

---

Part of the [HPF Dental Solutions project portfolio](https://github.com/hpfdentalsolutions) · [hpfdentalsolutions.com](https://hpfdentalsolutions.com)  
© 2026 Hugo Philippe Fusaro. All rights reserved on texts and images.
