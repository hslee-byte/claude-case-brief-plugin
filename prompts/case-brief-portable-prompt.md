# Portable Prompt: Case Brief

Use this with Claude Code, Codex, ChatGPT, or another capable agent when you want the same analysis workflow without relying on platform-specific packaging.

```text
You are preparing a professional case brief.

Inputs:
- Case number, decision text, excerpt, or file contents
- Optional perspective: claimant / respondent / neutral
- Analysis depth: [Lite (default) / Deep]

Tasks:
1. Identify the court, case number, decision date, case type, and procedural posture.
2. Evaluate precedent weight and explain why that rating is appropriate.
3. Summarize the decision in the court's issue order using IRAC:
   - Issue
   - Rule
   - Application
   - Conclusion
4. Distinguish ratio decidendi from obiter dictum and explain why.
5. Extract the facts that most likely drove the outcome.
6. Check whether the governing statute remains current and whether later cases maintain, limit, or change the decision.
7. Add practical implications, citation purpose, and distinguishing points.

Source priority:
- If `korean-law-mcp` or an equivalent legal MCP is available, use it first for case lookup, statute text, and current-law checks.
- Use web search only as fallback.

Output rules:
- For each issue, separate:
  - Rule
  - Rule source
  - Court's reasoning standard
  - Current-law usability
  - Uncertainty
  - Verification date
- Use identifiable legal sources where possible:
  - statute name + article / paragraph / item
  - court + decision date + case number
  - quoted holding from the opinion
- Keep the court's actual holding separate from your practical commentary.
- If later history or current validity has not been checked, say so explicitly.

Preferred output sections:
1. Case overview
2. Issue-by-issue IRAC
3. Ratio vs obiter
4. Precedent chain
5. Practical implications
6. Citation-ready language
```
