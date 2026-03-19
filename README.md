# SecurityPrep Baseline

**An opinionated backend security baseline for startups, product teams, and AI coding agents.**

SecurityPrep Baseline defines the core security controls, implementation guidance, and review rules needed to build modern backend systems securely by default.

It focuses on the areas teams most often get wrong in production:

> **Authentication, authorization, edge protection, service trust, key management, observability, and data access control.**

---

## Why this exists

Most backend systems are not insecure because teams ignore security.

They are insecure because:

* Authentication is implemented correctly, but **authorization is incomplete or inconsistent**
* Trust is established at login, but **not enforced across services and data layers**
* Systems are exposed to the internet without **proper edge protections**
* Secrets and keys are **scattered and poorly scoped**
* Logs exist, but **do not capture security-relevant events**
* AI-generated code is **functionally correct but insecure by default**

SecurityPrep Baseline addresses this by defining:

> **Where trust is established, how it is propagated, where it must be enforced, and how it is observed.**

---

## What this is

* A **backend security control system**
* A **reference for engineers building production systems**
* A **review framework for security and architecture decisions**
* A **machine-readable baseline for AI coding agents**

---

## What this is not

* A compliance framework (SOC2, ISO, etc.)
* A complete security program
* A replacement for experienced security engineers

---

## Core security domains

SecurityPrep Baseline is organized around the core trust boundaries of backend systems.

### 1. Identity and Authentication

Defines how identity is established and verified.

Covers:

* User identity lifecycle
* Login and session management
* JWT and token handling
* Cookie security
* MFA for sensitive users
* Account recovery flows
* Workload/service identity

---

### 2. Authorization and Policy Enforcement

Defines how access decisions are made and enforced.

Covers:

* Role-based and policy-based access control
* Server-side authorization checks
* Object and resource-level access
* Tenant isolation
* Admin and sensitive action controls
* Authorization at API and data layers

---

### 3. Edge and API Protection

Defines how systems are protected from the public internet.

Covers:

* TLS termination at the edge
* Ingress hardening
* Rate limiting and throttling
* DDoS protections
* API abuse controls
* Request validation and limits

---

### 4. Abuse, Fraud, and Risk Controls

Defines how systems detect and respond to malicious or abnormal behavior.

Covers:

* Suspicious login detection
* Bot and automation abuse
* Velocity and anomaly checks
* Risk-based authentication
* Step-up verification patterns
* Fraud detection signals and systems

---

### 5. Secrets, Keys, and Cryptographic Trust

Defines how sensitive credentials and cryptographic material are handled.

Covers:

* Secret storage and access patterns
* API key management
* KMS-backed encryption keys
* Signing key
