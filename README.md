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

# 🧠 Skills Demonstrated

This project demonstrates practical skills in:

Cybersecurity
File integrity monitoring
Cryptographic hashing
Hash comparison
Detection of file modification
Basic security verification techniques
Understanding of data integrity
Python Programming
Python functions
File handling
Exception handling
Conditional statements
User input
Hash generation
Modular programming
Linux
Kali Linux command-line usage
File creation and modification
Running Python scripts
Using Linux hashing utilities
Basic directory and file management
Security Analysis
Establishing a file hash baseline
Comparing baseline and current hashes
Identifying unexpected file changes
Interpreting integrity-check results
Version Control
Git repository initialization
Git commits
GitHub repository management


# 🔬 Methodology

The project followed a simple file integrity verification workflow.

# Step 1: File Selection

A target file is selected for integrity verification.

Example:

test_files/test1.txt

<img width="1326" height="582" alt="Calculating file harsh" src="https://github.com/user-attachments/assets/60536049-33e2-49f2-ae6a-c14e8b47ee46" />


# Step 2: Hash Generation

The Python program reads the file in binary mode and generates a cryptographic hash using either:

SHA-256
MD5

Example:

File
 ↓
Read file contents
 ↓
Hash algorithm
 ↓
Cryptographic hash

# Step 3: Establishing a Baseline

The original hash generated from the unchanged file is recorded and used as the expected or baseline hash.

Example:

Expected Hash:
ABC123................
# Step 4: File Integrity Verification

The program calculates the hash of the file again and compares it with the expected hash.

Expected Hash
      ↓
     COMPARE
      ↑
Current Hash

<img width="960" height="337" alt="intergrity status displayed" src="https://github.com/user-attachments/assets/f746b457-c2f1-41f2-9b6d-b28f13ea4067" />

# Step 5: Integrity Decision

If both hashes are identical:

Expected Hash == Current Hash
            ↓
    INTEGRITY VERIFIED

If the hashes are different:

Expected Hash != Current Hash
            ↓
       FILE MODIFIED
# Step 6: Modification Testing

The original test file is deliberately modified to simulate an unauthorized or unexpected change.

Example:

echo "Unauthorized modification." >> test_files/test1.txt

The integrity checker is then executed again using the original hash.

The difference between the original and current hash demonstrates that even a small change in file contents produces a different hash.

<img width="836" height="341" alt="file modification detected" src="https://github.com/user-attachments/assets/b2451b39-655f-480c-a021-1b7197079bfa" />


# 🧪 Laboratory Environment

The project was developed and tested in a Kali Linux cybersecurity laboratory environment.

# Environment Configuration
Operating System : Kali Linux
Programming Language : Python 3
Terminal : Linux Terminal
Hash Algorithms : SHA-256 / MD5
Version Control : Git
Repository : GitHub

# Test Environment

A dedicated test directory was created:

file-integrity-checker/
│
├── integrity_checker.py
├── README.md
├── requirements.txt
│
└── test_files/

The test files were used to generate baseline hashes and subsequently simulate file modifications.

# Program Features

The File Integrity Checker provides the following options:

============================================================
              FILE INTEGRITY CHECKER
============================================================

1. Calculate SHA-256 hash
2. Calculate MD5 hash
3. Check file integrity
4. Exit
# Feature 1: SHA-256 Hash Generation

Calculates the SHA-256 cryptographic hash of a selected file.

# Feature 2: MD5 Hash Generation

Calculates the MD5 hash of a selected file for comparison and educational purposes.

# Feature 3: Integrity Verification

Compares the expected hash with the current hash and reports whether the file has been modified.

# Feature 4: File Modification Detection

Detects changes by identifying differences between the original and current hash values.

# 🔎 Testing and Validation

The program was tested using the following procedure.

Test 1: Generate SHA-256 Hash
# python3 integrity_checker.py

The SHA-256 hash of the original file was generated.

The result was independently verified using the Kali Linux command:

# sha256sum test_files/test1.txt

The hash generated by the Python program matched the hash produced by the Linux utility.

Test 2: Generate MD5 Hash

The MD5 hash was generated using the Python program and independently verified using:

# md5sum test_files/test1.txt

Test 3: Verify File Integrity

The original hash was supplied to the integrity checker.

Expected result:

# Status: [✓] INTEGRITY VERIFIED

Test 4: Detect File Modification

The test file was modified:

# echo "Unauthorized modification." >> test_files/test1.txt

The integrity checker was then executed using the original hash.

Expected result:

# Status: [!] FILE MODIFIED

This confirmed that the program could successfully detect changes to the file.

🔐 Security Concept

Cryptographic hashing can be used to create a digital fingerprint of a file.

A hash is generated from the contents of the file:

Original File
     ↓
SHA-256
     ↓
Hash Value

When the file is modified, its contents change and a different hash is normally produced:

Modified File
     ↓
SHA-256
     ↓
Different Hash Value

Therefore, comparing the original hash with the current hash provides a practical method for detecting changes.

Integrity Verification
Matching Hashes
       ↓
File unchanged
       ↓
Integrity Verified
Modification Detection
Different Hashes
       ↓
File contents changed
       ↓
Possible modification

# ⚠️ Security Considerations

SHA-256 is preferred for modern security applications because MD5 has known collision weaknesses.

MD5 is included in this project primarily for educational and comparison purposes.

The expected hash should also be protected from unauthorized modification. If an attacker can modify both the target file and its stored baseline hash, the integrity-checking mechanism can be compromised.

For stronger real-world implementations, baseline hashes should be stored securely and protected against unauthorized modification.

# 📁 Project Structure
file-integrity-checker/
│
├── integrity_checker.py    # Main Python application
├── README.md               # Project documentation
├── requirements.txt        # Project dependencies
│
└── test_files/
   
#  Install directory
cd file-integrity-checker
3. Run the Program
python3 integrity_checker.py
4. Select an Operation

Choose from:

1. Calculate SHA-256 hash
2. Calculate MD5 hash
3. Check file integrity
4. Exit
   
# 📸 Project Demonstration

The demonstration should show:

Kali Linux laboratory environment.
Project directory and files.
Python program execution.
SHA-256 hash generation.
Hash verification using sha256sum.
Original file integrity verification.
Modification of the test file.
Detection of the modified file.

# 📊 Expected Results
Test	Expected Result
- Generate SHA-256	SHA-256 hash displayed
- Generate MD5	MD5 hash displayed
- Compare matching hashes	Integrity Verified
- Compare different hashes	File Modified
- Verify existing file	Successful
- Verify missing file	Error message displayed

# 🚀 Future Improvements

Future versions of the project could include:

- Automatic storage of baseline hashes.
- Support for multiple files in a single scan.
- JSON-based hash databases.
- Automatic integrity reports.
- Timestamped scan results.
- Log file generation.
- Adding hashing algorithms.
- Graphical user interface.
- Real-time file integrity monitoring.

# 📚 Learning Outcomes

Through this project, practical knowledge was gained in:

- Cryptographic hashing
- File integrity monitoring
- Python cybersecurity programming
- Linux command-line operations
- Security testing
- Hash verification
- Git and GitHub workflow
- Technical cybersecurity documentation

# 👨‍💻 Author

ATEMLEFAC NKAFU BECHEM

Cybersecurity Engineer

# Cybersecurity #Python #FileIntegrity #Cryptography #KaliLinux #EthicalHacking #CyberSecurityInternship #SAMAITechnologies


This project is intended for educational and cybersecurity training purposes.
