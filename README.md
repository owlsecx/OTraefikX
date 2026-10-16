# 🦉 OTraefikX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OTraefikX** — Modern Reverse-Proxy Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline Traefik & Caddy reverse-proxy configuration security auditor

---

## ✨ Features

- Stdlib YAML-subset / TOML / JSON / Caddyfile parsers, Traefik CLI-flag + TRAEFIK_* env and Docker-label models
- Traefik: API/dashboard, entryPoints, TLS options, transports, middlewares, providers, ACME, logging
- Docker: compose / inspect — docker.sock, privileged, published dashboard, implicit exposure, inline secrets
- Caddy: Caddyfile + JSON — admin API, auto_https, TLS, basicauth hashes, file_server, headers, on-demand TLS
- Score + grade A+…F, CWE + MITRE ATT&CK per rule
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity
- Offline & read-only: no network, files never modified

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OTraefikX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
