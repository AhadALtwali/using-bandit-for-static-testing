# using-bandit-for-static-testing
# Vulnerable Python Application

## Overview

This project is a deliberately vulnerable Python application created for educational and security testing purposes. It demonstrates several common security weaknesses that can be identified using static application security testing (SAST) tools such as Bandit.

The application includes functionality related to authentication, command execution, file processing, temporary file handling, network communication, and data deserialization. These features intentionally contain insecure coding practices to help students, developers, and security professionals understand how vulnerabilities appear in real-world applications.

## Purpose

The purpose of this project is to:

* Learn secure coding principles
* Practice source code review
* Explore common Python security vulnerabilities
* Test static analysis tools such as Bandit
* Understand how insecure coding practices can lead to security risks

## Included Vulnerabilities

The application intentionally contains the following security issues:

* Hardcoded secrets and credentials
* Weak cryptographic hashing (MD5)
* Command injection
* Code injection using `eval()`
* Unsafe deserialization with Pickle
* Unsafe YAML loading
* Insecure temporary file creation
* Weak random number generation for security-sensitive operations
* Disabled SSL/TLS certificate verification
* Path traversal and unrestricted file access

## Requirements

* Python 3.8+
* requests
* PyYAML
* Bandit (optional for security analysis)

Install dependencies:

```bash
pip install requests pyyaml bandit
```

## Running the Application

```bash
python vulnerable_app.py
```

## Security Analysis with Bandit

Run Bandit against the application:

```bash
bandit -r .
```

Or scan a specific file:

```bash
bandit vulnerable_app.py
```

Bandit should report multiple security findings related to insecure coding practices present in the application.

## Disclaimer

This project is intentionally insecure and should never be used in production environments. It is provided solely for educational, research, and security training purposes.
