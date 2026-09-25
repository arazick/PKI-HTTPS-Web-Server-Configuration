# PKI & HTTPS Web Server Configuration (SEED Lab)

## Overview
This repository contains the setup and documentation for configuring a local **Public Key Infrastructure (PKI)** and deploying a secure **Apache HTTPS web server** within a Docker container. The project covers Root CA key generation, Certificate Signing Requests (CSRs), X.509 certificate issuance with Subject Alternative Names (SAN), web server configuration, and browser trust mechanics.

## Technologies Used
* **Tools:** OpenSSL, Docker, Apache Web Server, Linux / Bash, Firefox
* **Protocols & Standards:** PKI, X.509 Certificates, SSL/TLS, HTTPS, RSA Cryptography, SAN Extensions

## Summary of Lab Tasks

### Task 1: Root Certificate Authority (CA) Setup
* Generated a 4096-bit RSA private key and self-signed X.509 Root CA certificate.
* Verified key algorithm parameters ($e = 65537$) and verified X509v3 extensions (`Basic Constraints`, `Subject Key Identifier`, `Authority Key Identifier`).

### Task 2 & 3: Web Server Certificate Signing & Issuance
* Created a 2048-bit private key and Certificate Signing Request (CSR) for server domain `www.razick.com`.
* Configured Subject Alternative Name (SAN) extensions to support multi-domain coverage (`www.razickZ.com`, `www.razickB.com`, etc.).
* Signed and issued the server certificate using the custom Root CA.

### Task 4: HTTPS Deployment & Troubleshooting
* Configured an Apache SSL Virtual Host (`razick_apache_ssl.conf`) inside Docker and enabled the SSL module.
* Resolved local DNS resolution failure by updating the system `/etc/hosts` file.
* Resolved browser certificate trust warnings by importing the Root CA certificate into the browser's Certificate Manager.

## Full Lab Report
For complete implementation details, step-by-step terminal outputs, and configuration screenshots, view the full document in this repository.
