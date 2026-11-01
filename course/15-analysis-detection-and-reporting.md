# 15. Analysis, detection, and reporting

## Learning outcomes

- Validate a lead before escalating it as an incident.
- Turn repeatable hunt evidence into detection logic.
- Produce a clear, uncertainty-aware hunt record.

## Validate and scope

A single indicator match is a starting point. Check source, time, host/user context, known business purpose, related process or network events, and whether the same behavior appears across a peer group. Separate observed facts from analytic interpretation. Look for evidence that weakens the hypothesis as carefully as evidence that supports it.

When suspicious activity is found, establish the affected assets and time bounds using authorized telemetry. Preserve only necessary evidence, follow chain-of-custody requirements where applicable, and use the incident-response process for containment decisions. Do not isolate systems or disable accounts without assigned authority unless policy explicitly authorizes it.

## From hunt to detection

A useful detection captures behavior with relevant context rather than a single fragile artifact. Document:

- Behavior and analytic rationale.
- Data source, required fields, and coverage assumptions.
- Query/logic and test data.
- Expected benign matches and tuning guidance.
- Severity, owner, response playbook, and escalation route.
- Versioning, expiration/review date, and feedback mechanism.

Test detections against known benign and synthetic cases. Monitor false positives and false negatives. A hunt that finds nothing may still reveal a collection gap or improve a baseline.

## Reporting template

```text
Hunt title and owner:
Question / trigger:
Scope and time window:
Hypothesis:
Sources and coverage:
Method / query summary:
Key observations:
Alternative explanations:
Assessment and confidence:
Affected assets / business relevance:
Actions and escalation:
Limitations / data gaps:
Detection or control follow-up:
Feedback date:
```

Avoid publishing credentials, session tokens, personal data, raw payloads, or unapproved indicators. Use a sanitized case reference where detailed evidence must be stored in a restricted system.

## Review prompts

1. What corroboration would you seek before escalating a suspicious process event?
2. How can an unsuccessful hunt improve security?
3. What operational details make a detection maintainable by someone else?
