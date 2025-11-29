# Contributing to CollectiVAI

Thank you for your interest in contributing to **CollectiVAI – Democratic AI for Europe**. 💙💛

This document provides a common guideline for all repositories under  
the `collectiv-ai` organisation (app, chain, website, docs, scripts, etc.).

---

## 1. Project Overview

CollectiVAI is an independent, human-centred AI initiative focused on:

- **Democratic AI & civic tech** (CollectiVAI App & Chain)  
- **Ethical, privacy-respecting AI infrastructure**  
- **Local / hybrid AI setups** (macOS, Linux, nodes)  
- **Security & reliability** inspired by industrial environments  

You can read more in:

- Org README: https://github.com/collectiv-ai/.github  
- Website & whitepaper: https://github.com/collectiv-ai/collectiv-ai.github.io  

---

## 2. Ways to Contribute

There are many ways to help, even without writing code:

- 🐛 **Report bugs**  
- 💡 **Propose features or improvements**  
- 📚 **Improve documentation** (EN/DE)  
- 🧪 **Test the app or chain prototypes**  
- 🌐 **Help with translations** (starting with DE/EN)  
- 🛡 **Review security, privacy and reliability aspects**  
- 🧱 **Work on infrastructure scripts & tooling**

Small, focused contributions are very welcome.

---

## 3. Before You Start

1. **Read the README** of the repository you want to contribute to.  
2. Check **open issues** and **projects** for existing work:  
   - maybe your idea is already being discussed.  
3. For larger changes, please **open an issue first** to discuss the idea.  
4. Make sure you understand and accept the  
   **[Code of Conduct](https://github.com/collectiv-ai/.github/blob/main/CODE_OF_CONDUCT.md)**.

---

## 4. How to Propose Changes

### 4.1 Issues

Use GitHub issues to report bugs, request features or ask questions.

When creating an issue, please include:

- **Type**: bug / feature request / question / docs  
- **Context**: which repo, which version/branch  
- **Steps to reproduce** (for bugs)  
- **Expected behaviour**  
- **Actual behaviour**  
- **Environment** (OS, device, tools if relevant)

Clear issues make it much easier to respond and act.

### 4.2 Pull Requests

Standard PR workflow:

1. **Fork** the repository.  
2. **Create a feature branch** from `main` (or the default branch):  
   `feature/my-improvement` or `fix/issue-123`.  
3. Make your changes in small, logical commits.  
4. Run tests / linters if available (see repo README).  
5. Open a **Pull Request** against the repository’s default branch.  
6. Describe:
   - what you changed  
   - why you changed it  
   - how you tested it  

We may ask you for small adjustments before merging.

---

## 5. Code Style & Languages

Because CollectiVAI is multi-stack, style is **repo-specific**.  
General guidelines:

- Follow the **existing style** in the file or project.  
- For **Swift / SwiftUI** (CollectiVAI App):
  - use clear naming, small focused views and view models  
  - keep UI and logic separated as much as possible  
- For **Go / Cosmos SDK** (App-Chain):
  - follow standard Go formatting (`gofmt`) and idioms  
  - prefer explicit, readable code over clever tricks  
- For **Shell scripts**:
  - keep them safe, explicit, with clear `echo` logs  
  - avoid destructive commands without prompts

Documentation is usually in **English**, with **German** versions where relevant.

---

## 6. Security & Responsible Disclosure

CollectiVAI touches on **security, blockchain and infrastructure**.  

- Do **not** open public issues for critical security vulnerabilities.  
- Instead, please send an e-mail to:

  **security@collectivai.org** (if not available yet, use `info@collectivai.org`)

Include:

- affected repository / component  
- description of the issue  
- steps to reproduce  
- potential impact  

We will respond as soon as reasonably possible and coordinate a fix and disclosure.

---

## 7. AI & Ethics

CollectiVAI explicitly cares about **democratic, human-centred AI**:

- Please avoid contributions that primarily serve **surveillance, manipulation, exploitation or harm**.  
- Contributions should respect **privacy, consent and human rights** as far as technically feasible.  
- If you work on routing, logging or analytics, consider:
  - data minimisation  
  - transparency for the user  
  - options to opt out or delete data  

If you are unsure whether an idea fits the ethical scope, open an issue and ask.

---

## 8. Documentation & Translations

Clear documentation is a core part of the project.

- For every non-trivial change, update **README** or relevant docs.  
- Use **English** as the default technical language.  
- German translations are welcome in separate files (e.g. `README_DE.md`).  
- Keep translated content **aligned** with the English version (no marketing extras).

Diagrams, architecture overviews and examples are very welcome,  
especially for the app, chain and civic use cases.

---

## 9. Attribution & Licensing

Licences are defined **per repository** (see the `LICENSE` file).

By contributing code, docs or other content, you agree that:

- your contribution is compatible with the repository’s licence, and  
- you have the right to contribute it (no proprietary or secret material).

If you are contributing on behalf of an organisation,  
please make sure you are allowed to do so.

---

## 10. Getting Started (Practical Entry Points)

Some good starting points across the organisation:

- `collectiv-ai-app`  
  - improve README / add screenshots  
  - small SwiftUI refactors  
  - settings, accessibility, localisation (EN/DE)

- `collectiv-ai-app-chain`  
  - discuss / sketch governance modules  
  - help with basic Cosmos app scaffolding  
  - write docs for devnet/testnet setups

- `collectiv-ai.github.io`  
  - improve whitepaper formatting  
  - add use case examples (cities, universities, NGOs)  
  - fix typos or layout issues

- `collectiv-ai-business` & `collectiv-ai-sponsors`  
  - proofread docs  
  - suggest structure improvements  
  - add FAQs for partners / sponsors

---

## 11. A Note in German

> 🇩🇪 **Hinweis:**  
> Beiträge sind sehr willkommen – egal ob klein oder groß.  
> Du musst kein „Senior Developer“ sein, um mitzumachen.  
> Wichtig sind **Respekt, Offenheit und die Bereitschaft zu lernen**.  
> Wenn du unsicher bist, einfach ein Issue mit deiner Idee eröffnen –  
> dann schauen wir gemeinsam, ob und wie es ins Projekt passt.

---

Thank you for helping to build CollectiVAI –  
**Democratic AI for Europe, Made in Europe.**
