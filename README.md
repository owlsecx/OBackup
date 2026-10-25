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

OBackup is an offline, read-only auditor for backup configuration and exposed backup artifacts across a wide range of tools (restic, borg, duplicity, bacula/bareos, amanda, rsnapshot, timeshift, deja-dup, duplicati, rclone, cron and systemd timers). It flags unencrypted destinations, plaintext credentials, weak permissions, missing rotation and cleartext transports, and scans directories for exposed SQL dumps, config backups, key files and disk images. Findings map to CWE and MITRE ATT&CK with remediation and a 0–100 risk score, and it never modifies or deletes backups.

---

## ✨ Features

- Tolerant parsers for restic, borg, duplicity, bacula/bareos, rclone, cron and more
- Detects unencrypted destinations, plaintext creds, weak permissions and no rotation
- Exposed-artifact scanner for SQL dumps, .bak/.old configs, key files and VM images
- Magic-byte sniffing and safe archive member listing
- CWE + MITRE ATT&CK (T1005/T1530/T1552) mapping with per-finding remediation
- Export TXT/MD/JSON/CSV/SARIF with CI gates; strictly read-only

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBackup --scan quick
./OBackup --config /etc/restic/ --scan-artifacts /var/backups --fail-on high
./OBackup --root /mnt/image --scan full --format json -o report.json
./OBackup --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
