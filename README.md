# EU Compliance Rules for AI Coding Tools

> **Ship fast. Stay compliant.** Drop-in compliance rules for your AI coding tool.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## What Is This?

Ready-to-use configuration files that teach your AI coding tool about EU compliance requirements. Drop the right file into your project and your AI assistant will automatically flag compliance issues as you build.

Covers **GDPR**, the **AI Act**, the **Data Act**, and the **ePrivacy Directive**.

> **DISCLAIMER:** These files provide general guidance only and do not constitute legal advice. EU regulations are complex and context-dependent. Always consult a qualified legal professional. See [DISCLAIMER.md](DISCLAIMER.md).

## Quick Start

1. Find your AI coding tool below
2. Copy the config file into your project
3. Start coding — your AI will now flag compliance issues

## Supported Tools

| Tool | Config File | Copy To |
|------|------------|---------|
| **Claude Code** | [`claude-code/CLAUDE.md`](claude-code/CLAUDE.md) | Project root |
| **Cursor** | [`cursor/.cursorrules`](cursor/.cursorrules) | Project root |
| **GitHub Copilot** | [`github-copilot/.github/copilot-instructions.md`](github-copilot/.github/copilot-instructions.md) | `.github/` directory |
| **Windsurf** | [`windsurf/.windsurfrules`](windsurf/.windsurfrules) | Project root |
| **Cline** | [`cline/.clinerules`](cline/.clinerules) | Project root |
| **Aider** | [`aider/.aider.conf.yml`](aider/.aider.conf.yml) | Project root |
| **Kiro** | [`kiro/.kiro/steering.md`](kiro/.kiro/steering.md) | `.kiro/` directory |
| **Amazon Q** | [`amazon-q/.amazon-q/rules.md`](amazon-q/.amazon-q/rules.md) | `.amazon-q/` directory |
| **JetBrains AI / Junie** | [`jetbrains-ai/.junie/guidelines.md`](jetbrains-ai/.junie/guidelines.md) | `.junie/` directory |
| **Gemini CLI** | [`gemini-cli/GEMINI.md`](gemini-cli/GEMINI.md) | Project root |

## What's Covered

Each config file includes rules for:

### GDPR (General Data Protection Regulation)
- Consent requirements (opt-in, no pre-ticked boxes)
- Data minimization principles
- Right to erasure (Art. 17)
- Data Processing Agreements for third parties
- Encryption at rest and in transit
- Data retention policies

### AI Act (Regulation 2024/1689)
- Risk tier classification (banned / high / limited / minimal)
- Transparency obligations (label AI-generated content)
- High-risk system requirements (audit logging, human oversight)
- Key enforcement deadlines (Aug 2, 2026)

### Data Act (Regulation 2023/2854)
- Data portability requirements (JSON/CSV export)
- Anti-dark-pattern provisions
- IoT data access rights

### ePrivacy Directive
- Cookie consent requirements
- Essential vs non-essential cookies
- Consent withdrawal mechanisms

## Code Annotations

All files include standard compliance annotations for your codebase:

```javascript
// PII: user email address
// LEGAL_BASIS: consent
// AI_RISK_TIER: limited
// CONSENT_REQUIRED: yes — collects user preferences
// RETENTION: 30 days after account deletion
```

## Key Deadlines

| Date | What Happens |
|------|-------------|
| **Feb 2, 2025** | AI Act — Prohibited practices enforced |
| **Aug 2, 2025** | AI Act — General-purpose AI rules |
| **Sep 12, 2025** | Data Act — Data portability obligations |
| **Aug 2, 2026** | AI Act — Main obligations (high-risk, transparency) |
| **Aug 2, 2027** | AI Act — Full enforcement |

## Want the Full Framework?

These config files are compliance *triggers* — reminders to check the right things at the right time. For the complete framework with 60+ files including:

- Detailed checklists for every regulation
- Architecture patterns and conventions
- Feature spec templates with compliance sections
- Operational runbooks (incident response, breach notification)
- Legal document templates (privacy policy, ToS, cookie policy)
- Security guidelines and testing strategies

**Visit [prompt-master.dev](https://prompt-master.dev)**

## Free Interactive Tools

- [AI Act Classifier](https://prompt-master.dev/tools/ai-act-classifier) — Provider or Deployer? Find out in 2 minutes
- [Compliance Checker](https://prompt-master.dev/tools/compliance-checker) — Full interactive compliance assessment
- [Compliance Roadmap](https://prompt-master.dev/tools/compliance-roadmap) — Personalized EU compliance timeline
- [Security Audit](https://prompt-master.dev/tools/security-audit) — Find vulnerabilities in AI-generated code

## Contributing

Contributions welcome! If you use an AI coding tool that's not listed, feel free to:

1. Fork this repo
2. Add a config file in the tool's expected format
3. Open a PR

Please keep the disclaimer header in all config files.

## License

[MIT](LICENSE) — Use freely in personal and commercial projects.

---

*Built by [PromptMaster](https://prompt-master.dev) — Free tools and frameworks for vibe coders building EU-ready apps.*
