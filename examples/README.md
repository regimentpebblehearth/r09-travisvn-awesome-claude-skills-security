# 🔒 Examples — Security & Compliance

## Example 1: Quick Command

**Input:**
```
/owasp-scan my-target --output md
```

**Claude's Response:**

```
╔══════════════════════════════════════════════════╗
║  OWASP-SCAN                                    ║
╠══════════════════════════════════════════════════╣
║  Target: my-target                               ║
║  Output: Markdown                                ║
║  Starting analysis …                             ║
╚══════════════════════════════════════════════════╝

[░░░░░░░░░░]   0%  Initialising …
[████░░░░░░]  40%  Collecting data …
[████████░░]  80%  Scoring …
[██████████] 100%  ✓ Complete

┌──────────────────────────────┬──────────┬─────────────────────────────────┐
│ Item                         │ Priority │ Action                          │
├──────────────────────────────┼──────────┼─────────────────────────────────┤
│ Issue A found in target      │  🔴 High │ Fix immediately — see docs      │
│ Optimisation opportunity B   │  🟠 Med  │ Schedule for next sprint        │
│ Minor improvement C          │  🟡 Low  │ Add to backlog                  │
│ Element D looks good         │  🟢 Pass │ No action needed                │
└──────────────────────────────┴──────────┴─────────────────────────────────┘

┌─────────────────────────────────────────┐
│  SUMMARY  —  OWASP-SCAN                 │
├─────────────────────────────────────────┤
│  Items analysed :  24                   │
│  Issues found   :  3  (🔴 1  🟠 1)     │
│  Quick wins     :  2 actions             │
│  Est. impact    :  High                  │
└─────────────────────────────────────────┘

💡 Recommended next: /dep-cve
```

---

## Example 2: Full Workflow

**Input:**
```
/workflows:secure-sdlc my-target --scope full
```

**Progress Display:**

```
╔══════════════════════════════════════════════════════════╗
║  WORKFLOW: SECURE-SDLC                                  ║
╠══════════════════════════════════════════════════════════╣
║  Step 1/7  Discovery        ✓  Completed  1m 32s        ║
║  Step 2/7  Audit            ✓  Completed  6m 14s        ║
║  Step 3/7  Prioritisation   ✓  Completed  2m 08s        ║
║  Step 4/7  Planning         ⟳  Running …               ║
║  Step 5/7  Execution        ░  Pending                  ║
║  Step 6/7  Validation       ░  Pending                  ║
║  Step 7/7  Reporting        ░  Pending                  ║
╠══════════════════════════════════════════════════════════╣
║  Overall:  [████████░░░░]  57%   ETA: ~18 min           ║
╚══════════════════════════════════════════════════════════╝
```

---

## Tips

1. **Start with a quick command** to get oriented before running a full workflow.
2. **Use `--scope quick`** for a fast scan, `--scope full` for production audits.
3. **Chain commands**: run analysis first, then use the findings as input for planning.
4. **Save reports**: add `--output html` and pipe to a file for stakeholder sharing.
