# EU Compliance Rules for JetBrains AI / Junie

> Source: [promptmaster.dev](https://promptmaster.dev) — Free EU compliance framework
> License: MIT | See DISCLAIMER.md for limitations
>
> **DISCLAIMER:** This file provides general guidance only and does not
> constitute legal advice. Always consult a qualified legal professional.

## GDPR Rules

- NEVER store personal data without a documented legal basis (consent, contract, legitimate interest)
- ALL data collection MUST have explicit opt-in consent — no pre-ticked boxes
- Personal data MUST be deletable via user action (Art. 17 right to erasure)
- Default to data minimization: only collect what is strictly necessary
- Cookie/tracking consent MUST be opt-in with granular choices
- Third-party data sharing requires a Data Processing Agreement (DPA)
- Encrypt personal data at rest and in transit
- No indefinite storage — implement retention policies

## AI Act Rules

- Classify AI features by risk tier before building:
  - **Banned:** Social scoring, subliminal manipulation, real-time biometric ID
  - **High risk:** Employment, credit, education, law enforcement AI
  - **Limited risk:** Chatbots, content generation (transparency required)
  - **Minimal risk:** Spam filters, search (no extra obligations)
- Label ALL AI-generated content shown to users
- High-risk AI needs: audit logging, human oversight, bias documentation
- Main enforcement: August 2, 2026

## Data Act Rules

- Users MUST export ALL their data in machine-readable format (JSON/CSV)
- No dark patterns hindering data portability or provider switching
- IoT data accessible to the generating user

## ePrivacy Rules

- No cookies or tracking before consent
- Only essential cookies without consent (session, CSRF)
- Consent withdrawal must be as easy as giving consent

## Before Any Feature

1. Personal data? → Document legal basis
2. AI/ML feature? → Classify risk tier
3. Third-party sharing? → Verify DPA
4. Sets cookies? → Verify consent mechanism

## Code Annotations

- `// PII: <description>` — personal data fields
- `// LEGAL_BASIS: <consent|contract|legitimate_interest>` — processing basis
- `// AI_RISK_TIER: <unacceptable|high|limited|minimal>` — risk classification
- `// CONSENT_REQUIRED: <yes|no — reason>` — consent requirement

---

*Full framework with 60+ files: [promptmaster.dev](https://promptmaster.dev)*
