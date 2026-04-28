---
model: claude-sonnet-4-6
type: workflow
domain: security
source_repo: travisvn/awesome-claude-skills
---

# 🔒 Workflow: Breach Response

> **Data breach response: detect → assess → notify → remediate → post-mortem**

## Overview

This multi-step workflow orchestrates the full **breach response**
process for Security & Compliance. Each step has clear inputs, outputs and
success criteria displayed via structured UI panels.

## Workflow Steps

| # | Phase | Description | Command |
|---|-------|-------------|---------|
| 1 | **Discovery** | Gather context, define scope and success criteria | `/breach-response-step-1` |
| 2 | **Audit** | Run all relevant analysis commands in parallel | `/breach-response-step-2` |
| 3 | **Prioritisation** | Score findings by impact × effort matrix | `/breach-response-step-3` |
| 4 | **Planning** | Build phased action plan with owners and timelines | `/breach-response-step-4` |
| 5 | **Execution** | Step-by-step guided execution with checkpoints | `/breach-response-step-5` |
| 6 | **Validation** | Verify outcomes against success criteria | `/breach-response-step-6` |
| 7 | **Reporting** | Generate stakeholder report with before/after metrics | `/breach-response-step-7` |

## Starting the Workflow

```bash
/workflows:breach-response [target] [options]
```

**Options:**
- `--scope [full|quick|targeted]` — analysis depth (default: full)
- `--output [md|json|html]` — report format (default: md)
- `--notify [slack|email|none]` — completion notification

## Workflow Dashboard

```
╔══════════════════════════════════════════════════════════╗
║  WORKFLOW: BREACH-RESPONSE                              ║
╠══════════════════════════════════════════════════════════╣
║  Step 1/7  Discovery        ✓  Completed  2m 14s        ║
║  Step 2/7  Audit            ✓  Completed  8m 47s        ║
║  Step 3/7  Prioritisation   ⟳  Running …               ║
║  Step 4/7  Planning         ░  Pending                  ║
║  Step 5/7  Execution        ░  Pending                  ║
║  Step 6/7  Validation       ░  Pending                  ║
║  Step 7/7  Reporting        ░  Pending                  ║
╠══════════════════════════════════════════════════════════╣
║  Overall:  [████████░░]  43%   ETA: ~22 min             ║
╚══════════════════════════════════════════════════════════╝
```

## Completion Report Template

At the end of the workflow Claude generates:

```markdown
## Breach Response — Completion Report

**Date:** {date}
**Duration:** {duration}
**Scope:** {scope}

### Executive Summary
{2-3 sentence summary for stakeholders}

### Key Findings
| Priority | Finding | Impact | Owner | Due |
|----------|---------|--------|-------|-----|

### Before / After Metrics
| Metric | Before | After | Delta |
|--------|--------|-------|-------|

### Next Review
Recommended follow-up: {date + 30 days}
```
