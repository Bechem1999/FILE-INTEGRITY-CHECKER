# 🔐 File Integrity Checker

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Hashing](https://img.shields.io/badge/Hashing-SHA--256%20%7C%20MD5-orange)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-black?logo=kalilinux)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

> A Python-based cybersecurity tool for calculating, comparing, and verifying file hashes to detect unauthorized or unexpected file modifications.

---

## 📌 Project Overview

The **File Integrity Checker** is a Python-based cybersecurity tool developed to monitor and verify the integrity of files using cryptographic hash functions.

The tool calculates the **SHA-256** or **MD5** hash of a selected file and compares the current hash with a previously recorded expected hash. When the two hashes match, the file is considered unchanged. When the hashes differ, the tool identifies a possible file modification.

File integrity verification is an important cybersecurity concept because unauthorized changes to files can indicate accidental modification, corruption, malware activity, or other forms of tampering.

This project was developed as part of a practical cybersecurity internship task to demonstrate the application of Python programming and fundamental security concepts in a Kali Linux laboratory environment.

---

## 🎯 Objectives

The main objectives of this project were to:

- Develop a Python-based file integrity verification tool.
- Calculate file hashes using SHA-256 and MD5.
- Compare an expected hash against a newly calculated hash.
- Detect changes made to file contents.
- Display a clear file integrity status.
- Support integrity checking for different files.
- Demonstrate the practical application of cryptographic hashing in cybersecurity.
- Gain hands-on experience with Python and Linux-based security tools.

---

## 🛠️ Tools and Technologies Used

| Tool / Technology | Purpose |
|---|---|
| **Python 3** | Development of the file integrity checker |
| **hashlib** | Generation of SHA-256 and MD5 hashes |
| **os** | File existence and file handling operations |
| **Kali Linux** | Cybersecurity laboratory environment |
| **Linux Terminal** | Program execution and testing |
| **Git** | Version control |
| **GitHub** | Source-code hosting and project documentation |

### Python Libraries

The project uses only Python's standard library, meaning no external packages are required.

```text
hashlib
os
