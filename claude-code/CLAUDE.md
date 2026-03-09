# EU Compliance Rules for AI Coding Tools
# Source: https://prompt-master.dev — Free EU compliance framework
# License: MIT | See DISCLAIMER.md for limitations
#
# DISCLAIMER: This file provides general guidance only and does not
# constitute legal advice. Always consult a qualified legal professional.

## GDPR — Always-On Rules

- NEVER store personal data without a documented legal basis (consent, contract, legitimate interest)
- ALL user-facing data collection MUST have explicit opt-in consent — no pre-ticked boxes
- Every piece of personal data MUST be deletable via a user-triggered action (Art. 17)
- Default to data minimization: only collect fields strictly necessary for the feature
- Cookie/tracking consent MUST be opt-in with granular choices (analytics, marketing, functional)
- Any data shared with third parties requires a Data Processing Agreement (DPA)
- Personal data must be encrypted at rest and in transit
- Implement data retention policies — no indefinite storage without justification

## AI Act — Always-On Rules

- Before building any AI/ML feature, classify its risk tier:
  - Unacceptable: Social scoring, subliminal manipulation, real-time biometric ID → BANNED
  - High: Employment, credit, education, law enforcement AI → heavy obligations
  - Limited: Chatbots, content generation → transparency required
  - Minimal: Spam filters, search, recommendations → no extra obligations
- ALL AI-generated content shown to users MUST be labeled as AI-generated
- High-risk AI requires: audit logging, human oversight toggle, bias documentation
- Never build: social scoring, real-time biometric ID, or manipulative AI features
- Main enforcement deadline: August 2, 2026

## Data Act — Always-On Rules

- Users MUST be able to export ALL their data in structured, machine-readable format (JSON/CSV)
- No dark patterns that hinder data portability or switching providers
- IoT data must be accessible to the user who generated it
- Data sharing with third parties on fair, reasonable, non-discriminatory terms

## ePrivacy — Always-On Rules

- No cookies or tracking before user consent is given
- Essential cookies only may be set without consent (session, CSRF, load balancing)
- Consent must be as easy to withdraw as it is to give

## Workflow Triggers

### Before implementing any feature:
1. Does it collect personal data? → Document the legal basis
2. Does it use AI/ML? → Classify the risk tier
3. Does it share data with third parties? → Verify DPA is in place
4. Does it set cookies? → Verify consent mechanism exists

### Before building any AI feature:
1. Classify risk tier (unacceptable/high/limited/minimal)
2. Determine role: Provider (building AI) vs Deployer (using third-party API)
3. Implement transparency: label AI output, disclose AI interaction
4. If high-risk: add audit logging, human oversight, bias documentation

### Before any deployment:
1. Verify infrastructure is in EU region
2. Verify privacy policy covers all data processing
3. Verify consent mechanisms work correctly
4. Verify data export functionality is available

## Code Annotations

Add these comments to make compliance auditing easier:

- `// PII: <description>` — marks personal data fields
- `// LEGAL_BASIS: <consent|contract|legitimate_interest>` — legal basis for processing
- `// AI_RISK_TIER: <unacceptable|high|limited|minimal>` — AI Act risk classification
- `// AI_TRANSPARENCY: <disclosure-type>` — AI transparency implementation
- `// CONSENT_REQUIRED: <yes|no — reason>` — whether consent is needed
- `// RETENTION: <duration|reason>` — data retention policy

## Key Deadlines

| Regulation | Key Date | What Happens |
|---|---|---|
| AI Act — Prohibited practices | Feb 2, 2025 | Already enforced |
| AI Act — GPAI obligations | Aug 2, 2025 | General-purpose AI rules |
| AI Act — Main obligations | Aug 2, 2026 | High-risk, transparency rules |
| AI Act — Full enforcement | Aug 2, 2027 | All remaining provisions |
| GDPR | Already enforced | Fines up to 4% global revenue |
| Data Act | Sep 12, 2025 | Data portability obligations |

---

*For the full compliance framework with 60+ files, checklists, templates, and
architectural guidance, visit [prompt-master.dev](https://prompt-master.dev).*
