# 🦉 OTraefikX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OTraefikX** — Modern Reverse-Proxy Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OTraefikX is an offline, read-only Traefik v2/v3 configuration auditor that parses static YAML/TOML and dynamic configuration, Docker-label providers and command-line flags with stdlib-only parsers. It flags the insecure API/dashboard, the Docker-socket provider, missing TLS options, weak entrypoints, exposed metrics and Let's Encrypt storage issues. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Static and dynamic config parsers (YAML/TOML subset) plus Docker-label and CLI-flag providers
- API/dashboard checks: api.insecure, unauthenticated dashboard, exposed debug and ping endpoints
- Provider risk: Docker socket mounted/exposed, exposedByDefault, file provider watch and KV backends
- TLS checks: minVersion, cipher suites, default cert, sniStrict and missing TLS on routers
- Entrypoint, middleware (auth/headers/rate-limit), metrics/tracing exposure and ACME storage perms
- CWE+ATT&CK mapping, score/grade and TXT/MD/JSON/CSV/SARIF export with --fail-on gating

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OTraefikX --scan -f sarif -o traefik.sarif
./OTraefikX --static /etc/traefik/traefik.yml --dynamic /etc/traefik/dynamic.yml
./OTraefikX -r /mnt/image --fail-on high --json
./OTraefikX --demo
./OTraefikX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OTraefikX --help   # watch every network call
firejail --net=none ./OTraefikX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
