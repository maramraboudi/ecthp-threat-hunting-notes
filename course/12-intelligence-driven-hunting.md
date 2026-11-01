# 12. Intelligence-driven hunting

## Learning outcomes

- Convert external reporting into local, testable questions.
- Separate intelligence claims from local evidence.
- Prioritize behaviors based on organizational relevance and telemetry.

## The translation chain

**Report claim -> source evaluation -> behavior/ATT&CK mapping -> local exposure -> hypothesis -> telemetry plan -> query -> validation -> decision.**

Do not begin with a threat actor name and search for anything that could fit it. Extract the specific behavior, source and observation date, confidence, known alternatives, and prerequisites. Then ask whether your organization has relevant assets and whether available data could show the behavior.

## Prioritization

A practical priority considers:

- **Relevance:** does the activity intersect with the organization's sector, geography, exposed technology, identity model, or risk?
- **Actionability:** can the team investigate or reduce the risk with current controls?
- **Criticality:** what business impact follows if the threat is present?
- **Confidence and freshness:** how strong and current is the underlying evidence?
- **Coverage:** can telemetry answer the question over the required period?

A high-severity external report may be low priority for a particular organization if exposure is absent; a less dramatic behavior may deserve attention if it affects a critical asset.

## Correlation without over-attribution

Correlation can link events by shared observables, timing, infrastructure, behavior, or victim context. Preserve the link type and confidence. Shared hosting, a common tool, or a similar technique does not prove common control or actor identity. Validate matches against local context and independent sources.

A helpful distinction:

- **Enrichment** adds attributes about an object (for example, provider or registration context).
- **Contextualization** explains why the object matters to this question, environment, campaign, and time period.

## A hunt-tasking template

```text
Question / decision:
Source claim and provenance:
Behavior to test:
Local relevance and assets:
Hypothesis:
Time window and scope:
Required data / fields:
Coverage and known gaps:
Benign alternatives:
Validation and escalation criteria:
Output audience and expected action:
```

## Review prompts

1. How do you keep a threat report from becoming an assumption about your own environment?
2. When might a stale indicator still have historical value but no blocking value?
3. What local facts would make an external report actionable?
