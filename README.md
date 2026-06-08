# AI Use Cases for Digital Centers — Interactive Presentation

An interactive, single-file HTML presentation designed for the project **“AI Use Case Design and High-Level Prototype for Digital Centers of the Future, UNDP Bangladesh.”** It translates the *Detailed Use-Case Design Document* into a stakeholder-friendly slide deck: every AI use case is told as a user story around one Digital Center entrepreneur, paired with a reference architecture and a human-in-the-loop checkpoint, plus a fully interactive Bangla app preview.

---

## Overview

The deck is built to help a mixed audience — a2i, LGD, UNDP, field supervisors, and entrepreneurs — quickly understand *what* each AI use case does, *how* the system is wired, and *where the human stays in control*. It deliberately avoids "black box" framing: every AI moment answers five accountability questions, and every architecture diagram shows an explicit human approval step.

- **Format:** one self-contained `undp-ai-usecases.html` file — no build step, no server, no dependencies to install.
- **Audience:** government, development-partner, and field stakeholders (English) plus rural citizens/entrepreneurs (Bangla preview).
- **Design language:** warm mocha/cream "card" aesthetic, editorial typography, calm and professional.

---

## How to view

1. Download `undp-ai-usecases.html`.
2. Open it in any modern web browser (Chrome, Edge, Firefox, Safari).
3. Present in full screen (`F11` on Windows/Linux, `⌃⌘F` on macOS).

An internet connection is recommended on first load so the Google Fonts (Fraunces, Hanken Grotesk, Hind Siliguri for Bangla) can download; everything else runs locally.

### Navigation

- **Arrow keys** `←` / `→` (or `Space`) move between slides.
- **`Home` / `End`** jump to the first / last slide.
- **On-screen arrows** (bottom-right) and the **progress dots** (bottom-center) also navigate.
- **Swipe** left/right on touch devices.

---

## What's inside (15 slides)

1. **Cover** — project title, framing, and the architect credit.
2. **The protagonist** — a day-in-the-life of one Union Digital Center entrepreneur and the four pain points the AI addresses.
3. **The design principle** — the five accountability questions and the governance-language rule.
4. **Citizen experience (Bangla, interactive)** — a phone mockup that plays a real Bangla AI conversation; tap any of the 11 use-case tiles to preview that use case's own scenario.
5–12. **Eight detailed use cases** — each with a Bangla user story, an English AI-augmentation / human-control split, an "AI-in-action" label, and an animated reference-architecture diagram behind the text.
13. **Three further use cases** — summarized for later phases.
14. **Prototype roadmap** — the recommended priority order.
15. **Closing.**

### The eleven AI use cases

1. Assisted KYC, CRM & Document Vault
2. Service Status & Payment Tracking
3. Service Knowledge & Communication Assistant *(prototype priority ①)*
4. Predictive Demand & Queue Optimization
5. Early-Warning Dashboard for Center Performance
6. Center Maturity Classification
7. Citizen Feedback & Integrity Analysis *(prototype priority ②)*
8. Anomaly Monitoring for Sensitive Services
9. Business Sustainability Advisory
10. Personalized Financial Inclusion Recommender
11. Offline & Low-Connectivity Support

---

## Key features

- **User-story framing in Bangla.** Each use-case narrative is written in plain Bangla for the target community; the technical AI-augmentation and human-control lists remain in English for implementation clarity.
- **Reference architectures.** Every use case has a generated system diagram — *Inputs → AI Engine modules → Data & Governance stores → Human-in-the-loop checkpoint → Output* — with animated data-flow and a pulsing core, sitting on the same card surface as the text (no overlap).
- **Interactive Bangla app preview.** A phone mockup auto-plays a typed conversation (typing indicator, message bubbles, document/fee/status/alert cards, the human-confirm note). A picker lets the audience switch between all 11 scenarios; the in-app role badge updates to নাগরিক / উদ্যোক্তা / সুপারভাইজার as appropriate.
- **Human-in-the-loop throughout.** Governance language is enforced (e.g., "possible anomaly," "requires review," never "fraud confirmed"); sensitive credentials are explicitly never stored.
- **Self-contained & offline-friendly.** Pure HTML/CSS/vanilla JS with inline SVG and SMIL animation. No frameworks, no bundlers.

---

## Customization

Everything lives in the single HTML file.

- **Colors & theme:** edit the CSS variables in the `:root` block (`--bg`, `--card`, `--accent`, `--sage`, etc.).
- **Architecture diagrams:** edit the `ARCH` object in the first `<script>`. Each use case has `core`, `modules`, `inputs`, `stores`, `human`, and `output` fields; the diagram is drawn from these by `buildArch()`.
- **Bangla app scenarios:** edit the `SC` object in the second `<script>`. Each scenario is an array of steps (`user`, `ai`, `typing`, `note`) with `bn` (Bangla), optional `en` (English gloss), and optional `card` (HTML for a document/fee/alert card).
- **Use-case story text:** the Bangla user story lives in each slide's `.story2` block (`.q` quote + `.scene` narrative).
- **Slides:** add or remove `<section class="slide">` blocks; navigation, progress bar, and dots update automatically.

---

## Technical notes

- **Stack:** HTML5, CSS3 (custom properties, grid, keyframe animation), vanilla JavaScript, inline SVG + SMIL (`animateMotion`).
- **Fonts:** Fraunces (display), Hanken Grotesk (body), Hind Siliguri (Bangla) via Google Fonts.
- **No browser storage** is used; all state is in-memory for the session.
- Tested against the document content as of the 2026 design phase.

---

## Credits

**Designed & Architected by**

**Jahidul Arafat** — PhD Candidate, Auburn University (AU), USA
- Presidential & Woltosz Graduate Research Fellow
- Principal Strategist — Enterprise Architecture & Global Expansion, OrangeBD
- Lead Avatar Technology Developer, thinkingautomata.ai, USA

Prepared in the context of UNDP Bangladesh's Digital Centers of the Future initiative, in collaboration with a2i, and prototyped by OrangeBD.

---

## Confidentiality

This material is intended for information-sharing with a2i and UNDP Bangladesh. Please treat it accordingly and do not redistribute without authorization.
