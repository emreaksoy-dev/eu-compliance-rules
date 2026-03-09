# EU Compliance Rules for GitHub Copilot

> Source: [prompt-master.dev](https://prompt-master.dev) — Free EU compliance framework
> License: MIT | See DISCLAIMER.md for limitations
>
> **DISCLAIMER:** This file provides general guidance only and does not
> constitute legal advice. Always consult a qualified legal professional.

## GDPR (General Data Protection Regulation)

- NEVER store personal data without a documented legal basis (consent, contract, legitimate interest)
- ALL data collection MUST have explicit opt-in consent — no pre-ticked boxes
- Personal data MUST be deletable via user action (Art. 17 right to erasure)
- Default to data minimization: only collect what is strictly necessary
- Cookie/tracking consent MUST be opt-in with granular choices
- Third-party data sharing requires a Data Processing Agreement (DPA)
- Encrypt personal data at rest and in transit
- Implement data retention policies — no indefinite storage

## AI Act (Regulation 2024/1689)

- Classify AI features by risk tier before building:
  - **Banned:** Social scoring, subliminal manipulation, real-time biometric ID
  - **High risk:** Employment, credit, education, law enforcement AI
  - **Limited risk:** Chatbots, content generation (transparency required)
  - **Minimal risk:** Spam filters, search (no extra obligations)
- Label ALL AI-generated content shown to users
- High-risk AI needs: audit logging, human oversight, bias documentation
- Main enforcement deadline: August 2, 2026

## Data Act (Regulation 2023/2854)

- Users MUST export ALL their data in machine-readable format (JSON/CSV)
- No dark patterns hindering data portability or provider switching
- IoT data accessible to the generating user

## ePrivacy Directive

- No cookies or tracking before consent
- Only essential cookies without consent (session, CSRF)
- Consent withdrawal must be as easy as giving consent

## Workflow Checklist

Before implementing any feature, check:

1. Does it collect personal data? → Document the legal basis
2. Does it use AI/ML? → Classify the risk tier
3. Does it share data with third parties? → Verify DPA
4. Does it set cookies? → Verify consent mechanism

## Code Annotations

Mark compliance-relevant code with these comments:

- `// PII: <description>` — personal data fields
- `// LEGAL_BASIS: <consent|contract|legitimate_interest>` — processing basis
- `// AI_RISK_TIER: <unacceptable|high|limited|minimal>` — risk classification
- `// CONSENT_REQUIRED: <yes|no — reason>` — consent requirement

---

*Full framework with 60+ files: [prompt-master.dev](https://prompt-master.dev)*
