---
name: "r00-travisvn-awesome-claude-skills--security"
description: >
  🔒 Security & Compliance skill suite derived from travisvn/awesome-claude-skills.
  Security audits, vulnerability management, GDPR/SOC2/ISO27001 compliance and incident response.
  Provides 10 specialised commands for security, compliance, gdpr workflows.
version: "1.0.0"
domain: security
tags: ["security", "compliance", "gdpr", "soc2", "owasp", "pentest"]
source: "https://github.com/travisvn/awesome-claude-skills"
license: MIT
---

# 🔒 Security & Compliance Skill Suite

> Derived from **travisvn/awesome-claude-skills** · Focus: _curated Claude Skills resources and customisation tools_

## Overview

This skill provides 10 production-ready commands tailored for
**Security & Compliance** workflows. All commands follow a consistent
interaction pattern with structured output, progress tracking and
actionable recommendations.

## Available Commands

- `/owasp-scan` — OWASP Top-10 code scan with exploit description, CVSS score and remediation
- `/dep-cve` — Dependency CVE report with exploitability score and upgrade path
- `/gdpr-audit` — GDPR data-flow map, consent gaps and DPA checklist
- `/soc2-readiness` — SOC 2 Type II readiness gap analysis across all 5 Trust Service Criteria
- `/threat-model` — STRIDE threat model for architecture diagram with risk matrix
- `/pentest-report` — Structured penetration test report: executive summary, findings and remediation
- `/secret-detect` — Pre-commit secret detection hook config with entropy scanning
- `/iam-audit` — IAM least-privilege audit: over-permissioned roles, stale access and MFA gaps
- `/incident-playbook` — Security incident playbook: triage → contain → eradicate → recover → lessons
- `/privacy-policy` — GDPR/CCPA-compliant privacy policy generator from data inventory

## Interaction Pattern

Every command follows this structured response format:

```
1. CONTEXT CHECK   — Verify inputs and confirm scope with user
2. ANALYSIS        — Deep analysis with live progress display
3. FINDINGS TABLE  — Structured results with severity / priority
4. RECOMMENDATIONS — Prioritised action list (quick wins first)
5. NEXT STEPS      — Suggested follow-up commands
```

## UI Conventions

| Symbol | Meaning              |
|--------|----------------------|
| ✓      | Passed / complete    |
| ✗      | Failed / critical    |
| ⚠      | Warning / review     |
| ⟳      | In progress          |
| ░      | Pending              |
| 🔴     | Critical severity    |
| 🟠     | High severity        |
| 🟡     | Medium severity      |
| 🟢     | Low / informational  |

Progress bars use block characters:
`[████████░░] 80%`

## Quick Start

```bash
# Install this skill
cp -r . ~/.claude/skills/r00-travisvn-awesome-claude-skills--security/

# In Claude Code
/read ~/.claude/skills/r00-travisvn-awesome-claude-skills--security/SKILL.md
```

Then simply describe your task and Claude will route to the
appropriate command automatically.
