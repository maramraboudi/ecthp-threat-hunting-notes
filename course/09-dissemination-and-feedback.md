# 9. Dissemination and feedback

## Learning outcomes

- Select a product format based on audience, urgency, and decision.
- Write an assessment that separates observation, inference, confidence, and action.
- Use feedback to improve the intelligence cycle.

## Match product to consumer

| Consumer | Useful content |
|---|---|
| SOC analyst | Relevant indicators/behaviors, source, confidence, time window, and safe pivots. |
| Threat hunter | Testable hypothesis, expected evidence, data prerequisites, scope, and alternatives. |
| Incident responder | Known activity, possible follow-on behavior, priority evidence, and decision points. |
| Detection engineer | Behavioral logic, required telemetry, benign lookalikes, validation plan, and maintenance needs. |
| Executive | Business exposure, likely/possible outcomes, uncertainty, options, and decision required. |

A fast alert, a technical bulletin, a campaign assessment, and an executive briefing should not be identical copies. Use the shortest format that supports the decision, and link to detail when needed.

## A concise analytic structure

1. **Key judgment:** what is assessed and why it matters.
2. **Evidence:** what was directly observed and where it came from.
3. **Assessment:** how evidence supports or weakens the claim.
4. **Confidence and alternatives:** what remains uncertain and plausible alternatives.
5. **Relevance:** affected assets, sector, exposure, or telemetry.
6. **Action:** what the recipient should consider doing.
7. **Provenance and handling:** sources, dates, restrictions, and expiry.

Avoid absolute language when evidence is incomplete. Make confidence meaningful by describing its basis, not merely adding a label.

## Feedback and metrics

Ask whether the product was timely, relevant, understandable, and used. Record whether it helped confirm a hunt, reduce investigation time, improve a detection, change remediation priority, or avoid a false positive. Also record misses, source quality problems, telemetry gaps, and actions that caused disruption.

Useful measures include time from requirement to delivery, percentage of products tied to a requirement, validated detection/hunt outcomes, consumer feedback, stale-indicator rate, and response to identified gaps. Avoid metrics that reward raw report counts or indicator volume.

## Review prompts

1. How would the same finding differ in an executive brief and a hunter tasking?
2. What does a confidence statement need to explain?
3. Name a metric that reflects operational value rather than output volume.
