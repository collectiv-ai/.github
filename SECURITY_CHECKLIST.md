# CollectiVAI – Security Checklist

This checklist summarizes the core security practices for the CollectiVAI GitHub
ecosystem (`collectiv-ai`). It is meant as a living document – update and tick
items as the project evolves.

---

## 1. GitHub organisation & account

- [ ] **2FA enabled** for the `collectiv-ai` owner account (and all future collaborators).
- [ ] **Recovery methods** (email, recovery codes, hardware key) stored safely and offline.
- [ ] **Security & analysis** features enabled organisation-wide:
  - [ ] Dependency graph for all repositories
  - [ ] Dependabot alerts
  - [ ] Dependabot security updates
  - [ ] Grouped security updates
  - [ ] Secret scanning for all repositories
  - [ ] Push protection for all repositories
  - [ ] Private vulnerability reporting for new public repositories
- [ ] **Org members & collaborators** reviewed regularly (least privilege).
- [ ] **SSH keys / PATs** (if used) reviewed and rotated regularly.

---

## 2. All repositories (baseline)

Applies to every public repo under `collectiv-ai` (App, Router, Chain, Website,
Business, Branding, Sponsors, About-Founder, …).

- [ ] No `.env` or other secret files committed (API keys, private keys, seeds).
- [ ] `.gitignore` configured to exclude:
  - [ ] `.env`
  - [ ] local build artefacts
  - [ ] editor / IDE metadata
- [ ] Each repository has a clear **README** describing:
  - [ ] Scope and intended use (prototype / production / research).
  - [ ] Security assumptions (no secrets, no financial guarantees, etc.).
- [ ] A **LICENSE** file is present, or the README explicitly states:
  - [ ] that the code is “All rights reserved” / reference code only, **or**
  - [ ] which open-source license applies (MIT, Apache-2.0, …).
- [ ] No credentials or endpoints that expose private infrastructure:
  - [ ] No VPN endpoints
  - [ ] No private IPs or internal hostnames that should remain hidden
- [ ] All third-party dependencies are kept reasonably up-to-date (Dependabot).

---

## 3. Backend – `collectiv-ai-router`

FastAPI multi-provider AI router.

- [ ] **No real API keys** in the repository:
  - [ ] `.env` never committed
  - [ ] `.env.example` contains only example variable names, no real values.
- [ ] `SECURITY_NOTES.md` present and up-to-date:
  - [ ] Explains secret handling (keys only in hosting platform)
  - [ ] Mentions logging limitations and data protection
  - [ ] Recommends rate limiting, request size limits, anomaly detection
- [ ] **CORS** configuration:
  - [ ] `ROUTER_ALLOWED_ORIGINS` restricted to real frontends in production
  - [ ] No `*` in production deployments
- [ ] **Custom provider**:
  - [ ] If not used, `custom_provider.py` clearly returns an error (“not configured”).
  - [ ] If used, target backend is authenticated and trusted.
- [ ] **Error handling**:
  - [ ] No full prompts / PII logged in plain text
  - [ ] Upstream errors mapped to safe HTTP status codes
- [ ] **Transport security**:
  - [ ] Production deployments only exposed over HTTPS (via Cloudflare / reverse proxy).
  - [ ] No direct exposure of test instances with real keys to the public internet.

---

## 4. Client app – `collectiv-ai-app`

SwiftUI client for iOS / iPadOS / macOS.

- [ ] The app **never stores provider API keys** on device.
- [ ] Backend URL(s) are configurable and point to the router / trusted endpoints only.
- [ ] Any **Developer / Debug modes**:
  - [ ] Do not show real secrets
  - [ ] Clearly marked as “Developer only / not for production”
- [ ] Sensitive logs (prompts, user data) are disabled or minimised in release builds.
- [ ] Any future analytics / telemetry:
  - [ ] Are opt-in
  - [ ] Are documented in README / website
  - [ ] Avoid storing unnecessary personal data.

---

## 5. App-Chain – `collectiv-ai-app-chain`

Cosmos-based governance chain.

- [ ] README clearly states:
  - [ ] Chain is **not a financial product** and not for speculation.
  - [ ] Devnets/testnets must not be used to store assets with real-world value.
- [ ] No **private validator keys**, mnemonics or wallet seeds in:
  - [ ] `networks/`
  - [ ] `scripts/`
  - [ ] any example configs
- [ ] Example scripts use **throwaway keys** and are clearly labelled as such.
- [ ] Governance / proposal modules:
  - [ ] Validated inputs (no unbounded strings where not needed)
  - [ ] Safe default parameters in genesis examples.
- [ ] Security policy:
  - [ ] README or SECURITY file explains how to report vulnerabilities privately.

---

## 6. Website & docs – `collectiv-ai.github.io` and business/branding repos

- [ ] No contact forms or data-collecting scripts without a privacy notice.
- [ ] No hard-coded secrets or untrusted third-party scripts.
- [ ] External embeds (analytics, fonts, widgets) reviewed for privacy impact.
- [ ] Business & strategy docs clearly separate:
  - [ ] public / non-confidential parts (in repo)
  - [ ] internal documents (kept off GitHub).

---

## 7. Personal / lab scripts – `collectiv-ai-about-founder`

- [ ] All shell scripts carry a clear header warning, e.g.:
  - `# For personal lab use – do not run blindly on production systems.`
- [ ] Scripts do **not** contain:
  - [ ] hard-coded passwords
  - [ ] wallet seeds / mnemonics
  - [ ] private IPs that should not be public.
- [ ] Example output or screenshots do not reveal secrets or private identifiers.

---

## 8. Operational practices

- [ ] API keys for AI providers (OpenAI, Gemini, Mistral, etc.):
  - [ ] Stored only in secret managers / env variables in hosting platforms.
  - [ ] Rotated regularly and after any suspected leak.
- [ ] Access to production infrastructure (routers / nodes) protected by:
  - [ ] strong SSH keys or secure VPN
  - [ ] limited to trusted devices.
- [ ] Regular **security review cadence**:
  - [ ] Quarterly review of GitHub Security Alerts (Dependabot, secret scanning)
  - [ ] Review of open issues labelled `security`.
- [ ] Backups:
  - [ ] Critical configuration and documentation backed up securely
  - [ ] Wallets / keys (if any) backed up offline and encrypted.

---

## 9. Version & history

- [ ] This checklist is reviewed and updated at least twice a year.
- [ ] Old branches and unused repositories are archived or deleted to reduce attack surface.

---

> **Note:** This document is intentionally high-level and non-confidential.  
> It can be shared with partners, sponsors and auditors as part of the  
> CollectiVAI security story.
