# 10. Threat hunting fundamentals

## Learning outcomes

- Distinguish proactive threat hunting from routine monitoring and incident response.
- Define hunt scope, hypothesis, data needs, and stop conditions.
- Explain why logging and baselines are prerequisites.

## What threat hunting is

Threat hunting is a proactive, iterative investigation that searches available evidence for malicious activity that existing alerts may not have identified. A hunt is driven by a question, intelligence, risk, or an observed anomaly. It tests a hypothesis and records both supporting and disconfirming evidence.

Hunting complements alerting; it does not mean ignoring alerts. It is also distinct from incident response: when evidence indicates an active compromise, follow the incident process, preserve evidence, and coordinate containment rather than continuing an uncoordinated exploratory hunt.

## Hunt loop

**Prepare -> form hypothesis -> identify data -> query and pivot -> validate -> scope impact -> report/action -> improve.**

A useful hunt record includes:

- Trigger and intelligence requirement.
- Authorized environment and time range.
- Hypothesis and what would support or weaken it.
- Data sources, fields, coverage, retention, and known gaps.
- Query/analysis steps and result counts.
- Benign alternatives and validation performed.
- Findings, confidence, disposition, owner, and next action.

## Prerequisites

Hunts need reliable asset identity, synchronized timestamps, adequate log retention, relevant process/network/authentication telemetry, query access, and a documented escalation path. Collection should be designed before an incident, not improvised after logs have rolled off. Understand the system baseline and the impact of queries on production data.

## Threat hunting maturity

Maturity models are descriptive aids, not universal certification grades. A team generally progresses by formalizing procedures, improving data coverage and repeatability, developing analytics and automation, validating outcomes, and integrating hunt findings into detections and controls. Automating an unvalidated process can scale errors; fundamentals come first.

## When to stop or escalate

Pause if the target or data falls outside approved scope, collection may affect system availability, personal or sensitive data is unexpectedly involved, evidence suggests an active incident, or a proposed response could disrupt a business service. Preserve minimally necessary evidence and contact the designated owner.

## Review prompts

1. How does hunting differ from scheduled alert triage?
2. What makes a negative result meaningful?
3. What conditions should trigger a stop or incident-response escalation?
