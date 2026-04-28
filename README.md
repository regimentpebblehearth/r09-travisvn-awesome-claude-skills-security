# 🔒 Security & Compliance Skills Suite
### Derived from [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)

![Domain](https://img.shields.io/badge/Domain-Security%20&%20Compliance-red?style=for-the-badge)
![Commands](https://img.shields.io/badge/Commands-10-blue?style=for-the-badge)
![Workflows](https://img.shields.io/badge/Workflows-5-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

> **Adaptation of `travisvn/awesome-claude-skills` for Security & Compliance use cases.**
> Source focus: _curated Claude Skills resources and customisation tools_

---

## What This Skill Suite Does

Security audits, vulnerability management, GDPR/SOC2/ISO27001 compliance and incident response.

This collection provides **10 specialised commands** and
**5 multi-step workflows**, all with a consistent
structured-output UI so you always know exactly where you are and what to do next.

---

## Quick Install

```bash
# Clone this skill
cp -r . ~/.claude/skills/r00-travisvn-awesome-claude-skills--security/

# Register in Claude Code
# In a Claude Code session:
/read ~/.claude/skills/r00-travisvn-awesome-claude-skills--security/SKILL.md
```

---

## Commands

| Command | Description |
|---------|-------------|
| `/owasp-scan` | OWASP Top-10 code scan with exploit description, CVSS score and remediation |
| `/dep-cve` | Dependency CVE report with exploitability score and upgrade path |
| `/gdpr-audit` | GDPR data-flow map, consent gaps and DPA checklist |
| `/soc2-readiness` | SOC 2 Type II readiness gap analysis across all 5 Trust Service Criteria |
| `/threat-model` | STRIDE threat model for architecture diagram with risk matrix |
| `/pentest-report` | Structured penetration test report: executive summary, findings and remediation |
| `/secret-detect` | Pre-commit secret detection hook config with entropy scanning |
| `/iam-audit` | IAM least-privilege audit: over-permissioned roles, stale access and MFA gaps |
| `/incident-playbook` | Security incident playbook: triage → contain → eradicate → recover → lessons |
| `/privacy-policy` | GDPR/CCPA-compliant privacy policy generator from data inventory |

**Usage:**
```bash
/owasp-scan <target>
/dep-cve --scope full --output md
```

---

## Workflows (Multi-step)

| Workflow | Description |
|----------|-------------|
| `secure-sdlc` | Shift-left SDLC: threat model → code scan → DAST → pen test → sign-off |
| `breach-response` | Data breach response: detect → assess → notify → remediate → post-mortem |
| `compliance-audit` | Full compliance audit: scope → gap analysis → evidence → remediation plan |
| `zero-trust-design` | Zero-trust architecture design: identity → network → workload → data layers |
| `vendor-security` | Third-party vendor security assessment: questionnaire → risk score → decision |

**Usage:**
```bash
/workflows:secure-sdlc <target> --scope full
```

---

## UI Design

All commands display structured output with:

- **Progress panels** — real-time step tracking
- **Findings tables** — sorted by severity (🔴🟠🟡🟢)
- **Action checklists** — quick wins → medium-term → strategic
- **Summary cards** — at-a-glance metrics after each command


## Progress Display Example

```
╔══════════════════════════════════════════════════╗
║  Security Audit  —  api.domain.com               ║
╠══════════════════════════════════════════════════╣
║  OWASP scan      ✓   14 checks run                ║
║  CVE scan        ✓   234 deps checked             ║
║  IAM audit       ⟳   Scanning roles …             ║
║  GDPR check      ░   Pending                      ║
╚══════════════════════════════════════════════════╝

FINDINGS  (sort: severity desc)
┌──────┬──────────────────────────────┬──────────┬──────────────┐
│ Sev  │ Finding                      │ CVSS     │ Status       │
├──────┼──────────────────────────────┼──────────┼──────────────┤
│  🔴  │ SQL injection /api/search    │  9.8     │ ✗ Open       │
│  🔴  │ JWT none-alg accepted        │  9.1     │ ✗ Open       │
│  🟠  │ CORS wildcard on /api/*      │  6.5     │ ⚠ In-Review  │
│  🟡  │ Missing rate limiting        │  5.3     │ ⚠ In-Review  │
│  🟢  │ CSP header present           │   —      │ ✓ Pass       │
└──────┴──────────────────────────────┴──────────┴──────────────┘
```


---

## Interaction Pattern

Every command follows this 5-step structure:

```
① Scope Confirmation  — verify target and options with user
② Live Analysis       — progress bar while working
③ Findings Table      — structured results sorted by impact
④ Action Plan         — prioritised, time-boxed recommendations
⑤ Next Steps          — suggested follow-up commands
```

---

## Source Repository

This suite is derived from
**[travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)**
which focuses on: _curated Claude Skills resources and customisation tools_.

Improvements in this adaptation:
- Domain-specific command vocabulary for Security & Compliance
- Enhanced structured output with visual progress tracking
- Prioritised action plans with time estimates
- Workflow orchestration for end-to-end processes
- Consistent UI conventions across all commands

---

## License

MIT — free to use, modify and distribute.
