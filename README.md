<p align="center">
  <img src="assets/nethub-banner.svg" alt="NETHUB" width="600"/>
</p>

<h1 align="center">NETHUB</h1>

<p align="center">
  <strong>V0 Isolated Browser — Ghost Protocol — Zero Tracking — Zero Telemetry</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ALICE-V0-00ccaa?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iMTAiIGZpbGw9IiMwMGNjYWEiLz48L3N2Zz4=" alt="ALICE V0"/>
  <img src="https://img.shields.io/badge/Ghost_Protocol-ACTIVE-5b3dff?style=flat-square" alt="Ghost Protocol"/>
  <img src="https://img.shields.io/badge/Tracking-ZERO-ff3366?style=flat-square" alt="Zero Tracking"/>
  <img src="https://img.shields.io/badge/Telemetry-ZERO-ff3366?style=flat-square" alt="Zero Telemetry"/>
  <img src="https://img.shields.io/badge/ANTI--NETRUNNER-PROTECTED-ff6600?style=flat-square" alt="ANTI-NETRUNNER"/>
</p>

---

## What is NETHUB?

**NETHUB** is a privacy-first, isolated Electron browser built for the **ALICE** ecosystem. It enforces ghost protocol at every layer — no tracking, no telemetry, no fingerprinting, no data leaks.

Every request passes through a hardened proxy engine with rotating user agents, stripped headers, and full session isolation.

## Features

| Feature | Status |
|---|---|
| **WebRTC Disabled** | All WebRTC APIs blocked — no IP leak via STUN/TURN |
| **Session Isolation** | Each session runs sandboxed with contextIsolation |
| **Proxy Engine** | All traffic routed through ghost proxy — no direct connections |
| **Rotating User-Agent** | Random UA per request from a curated pool |
| **No Fingerprinting** | WebGL disabled, spellcheck off, no client data headers |
| **DNT / Sec-GPC** | Do Not Track + Global Privacy Control on every request |
| **No Referer / Origin** | Headers stripped on all outbound requests |
| **Single Instance** | Lock ensures only one NETHUB process runs |
| **Permission Deny-All** | Geolocation, notifications, media, MIDI — all denied by default |
| **Background Networking Off** | No pings, no phishing detection, no default app connections |
| **CSP Override** | Content-Security-Policy managed at proxy level |
| **X-Frame-Options Bypass** | Allows embedding any content through proxy |

## Architecture

```
┌─────────────────────────────────────────────┐
│                  NETHUB                      │
│                                              │
│  ┌──────────┐    ┌──────────┐    ┌────────┐ │
│  │ Electron │───▶│  Ghost   │───▶│ Proxy  │ │
│  │ Renderer │    │ Protocol │    │ Engine │ │
│  └──────────┘    └──────────┘    └────────┘ │
│       │               │              │       │
│  ┌────▼────┐    ┌─────▼─────┐  ┌────▼────┐ │
│  │ Sandbox │    │ Header    │  │ UA Rot  │ │
│  │ Context │    │ Stripper  │  │ Pool    │ │
│  └─────────┘    └───────────┘  └─────────┘ │
└─────────────────────────────────────────────┘
```

## Ghost Protocol Stack

1. **Network Layer** — WebRTC disabled, background networking off, no pings
2. **Header Layer** — Referer/Origin stripped, DNT+Sec-GPC injected, X-Client-Data removed
3. **Proxy Layer** — All external traffic proxied, rotating UA, response headers sanitized
4. **Renderer Layer** — contextIsolation, sandbox, no nodeIntegration, no WebGL
5. **Permission Layer** — All sensitive permissions denied by default

## Part of the ALICE Ecosystem

NETHUB is one module in the **A.L.I.C.E** (Autonomous Linked Intelligence for Comprehensive Execution) framework. It provides the browsing layer with full ghost protocol integration.

- [A.L.I.C.E](https://github.com/VZero911/A.L.I.C.E) — Core framework
- [THESEED](https://github.com/VZero911/THESEED) — L0 blockchain engine
- [ALICEHUB](https://github.com/VZero911/ALICEHUB) — Centralized hub
- **NETHUB** — Isolated browser (this repo)

## Requirements

- Node.js 18+
- Electron 33+
- ALICE backend services

## Usage

```bash
npm install
npm start
# or open a URL directly:
npm start -- https://example.com
```

---

<p align="center">
  <sub>Built by <strong>V0</strong> — <a href="https://github.com/VZero911">@VZero911</a></sub>
</p>

---

> **ANTI-NETRUNNER** — This repository uses character-level code hashing for intellectual property protection. Full source code is available on request with identity verification. Contact: [VZero911](https://github.com/VZero911)
