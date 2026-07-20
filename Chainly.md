# Chainly 
**Transparency, end to end**

Chainly is an open-source AI-powered data flow intelligence system that traces what actually happens to your data after you log in to digital services.

Most systems describe data handling in privacy policies. Chainly observes real network behavior and reconstructs verifiable, evidence-based data flow graphs that show how information moves, spreads, and is potentially resold across third parties.

---

## Core Vision

Privacy policies describe intent.  
Chainly reveals behavior.

If data moves, it leaves a trail. Chainly makes that trail visible, measurable, and auditable.

---

## What Chainly Does

Chainly analyzes **user-authorized login-triggered network activity** and builds a directed graph of data movement across the digital ecosystem.

It identifies:
- First-party services
- Third-party vendors
- Hidden intermediaries
- Data brokers and resale networks
- Undisclosed recipients

---

## Core Features

### Data Flow Graph Engine
- Builds real-time directed graphs of post-login data movement
- Tracks API calls, redirects, SDK activity, and endpoint propagation
- Visualizes full data lifecycle from authentication onward

### Directed Session Tracing
- Begins at login events
- Follows only causally triggered network requests
- Reconstructs full downstream propagation chains

### Entity Resolution System
- Maps domains → organizations → parent companies
- Uses WHOIS, RDAP, ASN data, and OSINT sources
- Assigns confidence scores to ownership attribution

---

### ToS vs Reality Comparator
Compares declared privacy behavior vs observed behavior:

- Extracts claims from privacy policies and terms of service
- Compares against real network traffic patterns
- Detects mismatches such as:
  - undisclosed third parties
  - expanded data usage beyond stated purpose
  - hidden redistribution chains

Outputs:
- Policy mismatch reports
- Side-by-side “declared vs observed” comparisons
- Evidence-linked graph traces

---

### Distribution Pattern Analysis
- Detects data fan-out after login
- Identifies SDK amplification behaviors
- Flags suspicious third-party propagation chains
- Highlights potential data broker activity

---

### Cross-User Pattern Aggregation (Privacy-Safe Intelligence)
Aggregates anonymized behavior patterns across sessions:

- Identifies recurring downstream endpoints
- Detects systemic data aggregation hubs
- Clusters broker and ad-tech networks
- Surfaces widespread hidden intermediaries

Important:
- No user-identifying data is exposed or reconstructable

Outputs:
- “Endpoint appears in X% of observed flows”
- “Likely mass data aggregation node detected”
- “Cross-network broker cluster identified”

---

### Login Impact Score
Each login session receives a measurable exposure profile:

- Data Spread Score (0–100)
- Third-Party Reach Index
- Broker Exposure Level
- Propagation Depth Score

Example:
> “This login distributed data across 12 entities in 3 network layers”

---

### Data Flow Replay (Forensics Mode)
- Step-by-step reconstruction of data movement
- Timeline-based visualization of each propagation hop
- Highlights:
  - first disclosure point
  - third-party expansion
  - broker entry points

---

### Invisible Recipient Detection
- Detects undisclosed or hidden endpoints
- Flags non-declared data recipients
- Provides confidence scoring and evidence graphs

---

### Broker Signature Library
- Catalog of known data movement patterns
- Detects:
  - ad-tech fan-out structures
  - resale chains
  - SDK-based data amplification
- Used for behavioral matching and early detection

---

### Risk & Compliance Engine
Evaluates observed behavior against:
- GDPR
- CCPA / CPRA
- FTC deceptive practice standards
- other global privacy frameworks

Outputs:
- Risk scores
- Violation likelihood assessments
- Evidence-based explanations

---

## Architecture

### Client Layer
- Browser Extension (TypeScript, WebExtensions API)
- Optional local proxy agent (Rust or Go)

### Backend Services
- Python (FastAPI) — core orchestration and APIs
- Node.js — real-time event streaming and ingestion

### Graph Database Layer
- Neo4j or ArangoDB
- Stores:
  - nodes (domains, orgs, endpoints)
  - edges (data transfers)
  - session graphs and propagation chains

### Storage Layer
- PostgreSQL — metadata, audit logs, reports
- Redis — real-time buffering and session state

### AI & Intelligence Layer
- LLM-assisted entity resolution
- Policy parsing and behavior comparison
- Graph-based inference and anomaly detection

### Data Sources
- WHOIS / RDAP records
- ASN and IP ownership data
- Corporate registry databases
- OSINT + enforcement datasets

---

## Frontend

- React + TypeScript
- Graph visualization (Cytoscape.js or Sigma.js)
- Timeline replay interface
- Risk dashboard
- Login Impact Score visualization

---

## Security Model

- User-authorized monitoring only
- No credential capture
- Encrypted session identifiers
- Zero-knowledge architecture principles
- Local-first processing where possible

---

## Open Source Commitment

Chainly is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.

This ensures:
- Full transparency of the system
- Protection against closed derivative surveillance systems
- Community-driven development and auditing
- Reproducible data flow analysis tooling

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/chainly/](https://roxanneardary.com/chainly/)

---

## License & Notice Requirements

Chainly is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- Chainly specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---

## Summary

Chainly turns hidden post-login data movement into a visible, structured, and auditable graph of truth.

It is designed for transparency, accountability, and systemic visibility into how digital data is actually shared across the modern web.

---

**Chainly — Transparency, end to end.**
