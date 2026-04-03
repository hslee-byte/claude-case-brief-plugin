---
name: case-brief
description: Summarize a case into issue-rule-application-conclusion, distinguish ratio from obiter, evaluate precedent weight, track cited and citing cases, check whether the underlying law remains current, and present source-traceable legal analysis with verification date and uncertainty notes.
---

# Case Brief

Use this skill when the user wants a structured case brief from a case number, decision text, excerpt, or file.

## Workflow

1. Read the decision and identify:
   - court
   - case number
   - decision date
   - case type
   - parties or procedural posture
2. Evaluate precedent weight and state the reason for that rating.
3. Organize the case by the court's issue order.
4. For each issue, produce:
   - Issue
   - Rule
   - Application
   - Conclusion
5. Distinguish:
   - ratio decidendi
   - obiter dictum
   and explain why each passage belongs in that category.
6. Check whether the cited statute remains current and whether later cases maintained, limited, or changed the rule.
7. Add practical use notes, distinguishing points, and citation purpose.

## Output Rules

For each issue, separate:

- Rule
- Rule source
- Court's reasoning standard
- Current-law usability
- Uncertainty
- Verification date

Use identifiable source fields when possible:

- statute name + article / paragraph / item
- court + decision date + case number
- quoted holding from the opinion

## Detailed Issue Template

```text
[Issue N]

Issue:
- The legal question in the court's order of analysis

Rule:
- The operative legal rule

Rule source:
- Statute / precedent / quoted holding

Court's reasoning standard:
- The test or framework the court actually used

Application:
- How the court applied the rule to the facts

Key facts:
- Facts that likely drove the outcome

Conclusion:
- The outcome on this issue

Ratio / Obiter:
- Quote or summarize the passage
- Explain why it is ratio or obiter

Current-law usability:
- Whether later statutory amendment or later cases affect present-day use

Citation purpose:
- rule statement / factual analogy / rebuttal support

Uncertainty:
- Missing opinion pages, unclear appellate status, incomplete later-history check, etc.

Verification date:
- YYYY-MM-DD
```

## Constraints

- Preserve critical holdings in the court's own words where possible.
- Do not blur ratio and obiter.
- Keep practical implications separate from the court's actual holding.
- If later history or current validity is not verified, say so explicitly.
