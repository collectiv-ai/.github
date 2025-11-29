# Contributing to CollectiVAI

Thank you for your interest in contributing to **CollectiVAI – Democratic AI for Europe** 💙💛  

This document explains **how to get involved**, how we work across the different
repositories, and what we ask from contributors.

---

## 1. Code of Conduct

By participating in CollectiVAI projects, you agree to follow the:

👉 [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md)

Please read it carefully. It reflects the project’s focus on  
**democracy, dignity, safety and public interest**.

---

## 2. Repositories Overview

The `collectiv-ai` organisation is split into multiple repositories, for clarity:

- **Organisation profile & meta**  
  - `.github` – organisation profile, Code of Conduct, contributing.

- **Core projects**
  - `collectiv-ai-app` – iOS / iPadOS / macOS client app (SwiftUI).  
  - `collectiv-ai-app-chain` – Cosmos-based governance and voting chain (pre-alpha).  
  - `collectiv-ai.github.io` – public website and documentation at [collectivai.org](https://collectivai.org).

- **Documentation & strategy**
  - `collectiv-ai-business` – business plan, funding logic, strategy & roadmap.  
  - `collectiv-ai-about-founder` – founder profile, lab description and portfolio (EN/DE).

- **Branding & partners**
  - `collectiv-ai-branding` – logos, colours, typography and visual identity.  
  - `collectiv-ai-sponsors` – information for sponsors, partners and institutions.

Each repo has its own **focus** and may include additional docs in a `docs/` folder.

---

## 3. Ways to Contribute

You don’t have to write code to contribute. Helpful contributions include:

- 🐞 **Bug reports** – clear descriptions, steps to reproduce, screenshots.  
- 💡 **Feature ideas** – suggestions that align with democratic, civic and public-interest use cases.  
- 📝 **Documentation improvements** – fixing typos, clarifying explanations, adding examples.  
- 🌍 **Translations & language polish** – especially English ↔ German.  
- 🧪 **Testing** – trying out prototypes and giving feedback on UX, clarity, accessibility.  
- 🛡 **Security / privacy reviews** – flagging risks, suggesting safer patterns.

---

## 4. How to Propose Changes

### 4.1. For small fixes (typos, small docs, tiny code changes)

1. **Fork** the repository you want to change.  
2. Create a branch, e.g. `fix/docs-typo` or `chore/update-readme`.  
3. Make your changes and commit with a clear message.  
4. Open a **Pull Request (PR)**:
   - describe _what_ you changed,
   - explain _why_ it improves things.

### 4.2. For larger features or architectural changes

1. First open an **issue** titled like:  
   `Proposal: Add X to Y (App / Chain / Website)`  
2. Describe:
   - the problem or use case,  
   - your proposed solution,  
   - why it fits the CollectiVAI vision (democratic AI, public interest, EU focus).  
3. Wait for initial feedback / alignment.  
4. Then implement in a feature branch and open a PR referencing the issue.

This helps keep the overall direction consistent and avoids wasted effort.

---

## 5. Coding & Style Guidelines

Because CollectiVAI spans multiple stacks, styles are kept *pragmatic*:

### 5.1. General

- Prefer **clear, explicit names** over clever abstractions.  
- Add short **comments** when something is non-obvious.  
- Keep the **user impact** in mind (citizens, experts, institutions).  
- Avoid adding heavy dependencies unless they clearly add value.

### 5.2. Swift / SwiftUI (App)

- Use Swift’s modern features where appropriate (e.g. `async/await`).  
- Group views into meaningful modules (e.g. `Chat`, `Contracts`, `Chain`, `Settings`).  
- Keep business logic in view models / managers rather than deep in views.

### 5.3. Go / Cosmos SDK (Chain)

- Follow the existing module structure under `app/` and `x/collectivai/`.  
- Add or update tests where possible, especially for governance logic.  
- Document new messages, params and state transitions in `docs/`.

### 5.4. Docs & Markdown

- Main language: **English**.  
- German sections are welcome, especially for public-facing docs.  
- Use headings, lists and short paragraphs for readability.

---

## 6. Security & Responsible Disclosure

If you believe you have found a **security issue**, privacy risk, or behaviour  
that could harm users or institutions:

- **Do not** open a public GitHub issue with full details.  
- Instead, contact **privately**:

  - ✉️ **info@collectivai.org**

Please include:

- which repo / component is affected,  
- how the issue could be exploited or misused,  
- any guidance on potential mitigation.

Security-related reports will be treated with **priority** and **confidentiality**.

---

## 7. Governance & Decision-Making

At this stage, CollectiVAI is a **founder-led** and **exploratory** project.

- The founder (and future core maintainers) have final say on:
  - project scope and roadmap,
  - acceptance of features and PRs,
  - alignment with **democratic, human-centred and European** values.

As the project matures, governance models may evolve towards more  
**participatory and transparent structures**, especially for:

- the Cosmos-based chain,  
- civic and institutional partnerships,  
- public funding and long-term sustainability.

---

## 8. Recognition & Attribution

Contributions may be recognised by:

- listing contributors in `README` or `CONTRIBUTORS` sections,  
- mentioning contributors in release notes,  
- highlighting community work in docs or on the website.

If you prefer **not** to be listed by name, please mention this in your PR or issue.

---

## 9. Thank you 💙💛

By contributing to CollectiVAI, you are helping to explore a different path for AI:

- more **democratic**,  
- more **transparent**,  
- more **human-centred**,  
- and rooted in **European values**.

Thank you for your time, your ideas and your care.
