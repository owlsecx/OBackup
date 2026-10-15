# 🦉 OBackup

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OBackup** — Offline Backup Configuration & Exposure Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline backup configuration & exposure auditor

---

## ✨ Features

- Tolerant offline parsers for restic, borg/borgmatic, duplicity/duply, bacula & bareos, amanda, rsnapshot, timeshift, deja-dup (dconf dump), duplicati exports, rclone.conf, systemd .service/.timer, crontab lines and ad-hoc rsync / tar / mysqldump / pg_dump scripts
- Ruleset: unencrypted destinations, plaintext creds, weak store permissions, no rotation / infinite retention, secrets backed up without exclusion, missing encryption flags, same-filesystem targets, cleartext transports (ftp://, rsync://, http://)
- Exposed-artifact scanner: SQL dumps, .bak/.old/.orig copies of configs, SQLite/DB dumps, tarballs of /etc or /home, shadow copies, git bundles, VM disk images, private keys / .env / wallets, credential files
- Magic-byte sniffing + safe archive member listing
- CWE + MITRE ATT&CK (T1005 / T1530 / T1552 ...) map, severity, remediation per finding, risk score 0-100
- Exports: TXT / Markdown / JSON / CSV / SARIF 2.1.0
- CI gates (--min-severity, --fail-on), --demo self-test
- Strictly read-only: never modifies or deletes backups

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBackup
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
