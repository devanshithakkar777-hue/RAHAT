# RAHAT — Intelligent Relief Platform

**The Right Resource, To the Right Location, At the Right Time.**

Built by **Team SevaTech** for Smart India Hackathon 2026.

RAHAT is a government-verified disaster relief platform that connects citizens to itemized, authenticated relief needs and tracks every rupee and every relief item from pledge to delivery. It also opens up the *public funds* side of disaster relief — NDRF, SDRF, CSR, and PM CARES money — to the same level of citizen transparency applied to individual donations.

---

## Table of Contents

- [Problem Statement](#problem-statement)
- [Quick Start](#quick-start)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Data & Scope Notes](#data--scope-notes)
- [Roadmap](#roadmap)
- [Team](#team)

---

## Problem Statement

Disaster relief today is fragmented across two blind spots:

1. **Citizen donations** go into a generic pool with no visibility into what's actually needed, no proof of delivery, and frequent duplication of effort.
2. **Public/government funds** (NDRF, SDRF, CSR) are released with far less real-time scrutiny than they deserve — utilization certificates lag, and there's no easy way for a citizen or journalist to audit where the money went.

RAHAT addresses both sides with one ledger-based platform: verified need-matching for citizen contributions, and a hash-chained public funds ledger with anomaly detection and RTI tooling for government spend.

---

## Quick Start

RAHAT is a **single self-contained HTML file** — no server, no build step, no dependencies to install.

```bash
# Just open it in any browser
open RAHAT_App.html      # macOS
start RAHAT_App.html     # Windows
xdg-open RAHAT_App.html  # Linux
```

Or double-click the file. That's the entire setup.

> **Note:** The AI Assistant's "live" mode calls the Anthropic API and only works when this page is rendered inside a Claude.ai artifact. Everywhere else (including opening this file directly), every AI feature automatically falls back to deterministic, data-grounded local logic — so nothing breaks, ever, regardless of connectivity. This is by design, not a limitation: disaster-hit regions can't be assumed to have reliable internet.

---

## Key Features

### For citizens
- Browse government-verified disasters with search, filters, and sort
- Contribute money or physical supplies to a specific, itemized need
- Track every contribution through a 4-stage journey (Received → Verified → In Logistics → Distributed)
- Report a hyperlocal need for official verification
- Sign up to volunteer
- Earn badges, climb the donor leaderboard, download a shareable Impact Certificate

### Public Funds Transparency
- Hash-chained ledger of NDRF/SDRF/CSR/PM CARES fund entries
- Utilization certificate status tracking
- Rule-based anomaly & fraud detection
- Citizen grievance reporting
- One-click RTI query drafting against any fund entry
- Full CSV/JSON export (RTI-ready open data)

### Agentic AI
- **Ask mode** — grounded Q&A over the platform's live data
- **Agent mode** — plans *and executes* multi-step tasks:
  - Smart Donation Planner (optimize a budget across underfunded needs, then execute)
  - Bulk triage of pending community reports
  - Full public-funds audit

### For authorities (Official Portal)
- Platform-wide Impact Dashboard (KPIs, category donut, spend-over-time, resource allocation by state)
- Per-disaster field update logging and community-report approval
- Volunteer roster management
- Inter-camp surplus/deficit resource rebalancing

*(See `RAHAT_Platform_Overview.md` for the complete feature list and all 15 USPs.)*

---

## Tech Stack

### This prototype
| Layer | Technology |
|---|---|
| Structure/Styling | HTML5 + CSS3 (custom properties, full dark mode) |
| Logic | Vanilla JavaScript — no framework, no bundler |
| Charts | Hand-rolled inline SVG |
| Certificates | HTML5 Canvas → PNG |
| State | In-memory (resets on reload by design) |
| AI | Anthropic Messages API with offline-first fallback |
| Exports | Client-side Blob → CSV/JSON |

### Planned production stack
| Layer | Technology |
|---|---|
| Frontend | React / Flutter |
| Backend | Node.js / FastAPI |
| Database | PostgreSQL / Firebase |
| AI/ML | Python, Scikit-learn |
| Geospatial | Mapbox / GIS |
| Security | RBAC + encryption |
| Payments | Authorized government payment gateway |
| Cloud | AWS / Azure / Government infrastructure |

---

## Project Structure

```
RAHAT_App.html                 # The entire application — open this
RAHAT_Platform_Overview.md     # Full USP + feature documentation
```

Everything — markup, styles, and logic — lives in the one HTML file. There is no separate build artifact.

---

## Data & Scope Notes

This is a hackathon prototype. To use it honestly in a demo or submission:

- All disasters, funds, and donors are **illustrative mock data**, clearly labeled in-app.
- Aadhaar/OTP verification and UPI payment steps are **simulated**, not wired to real rails.
- The ledger's hash-chaining is **illustrative tamper-evidence**, not production cryptography.
- Data resets on page reload — there is no backend persistence in this prototype.

---

## Roadmap

- [ ] Real backend with persistent storage (PostgreSQL)
- [ ] Government API integration for verified disaster/need feeds
- [ ] Real payment gateway integration
- [ ] Aadhaar-based identity verification
- [ ] Production-grade audit logging for the public funds ledger
- [ ] Native mobile apps (React Native / Flutter)
- [ ] Real GIS-based relief mapping (Mapbox)

---

## Team

**SevaTech** — Smart India Hackathon 2026

---

## License

Prototype built for Smart India Hackathon 2026. All rights reserved by Team SevaTech unless otherwise specified.
