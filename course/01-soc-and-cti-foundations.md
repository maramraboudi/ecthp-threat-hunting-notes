# 1. Security operations and CTI foundations

## Learning outcomes

- Describe how security operations reduce risk through visibility, detection, response, and recovery.
- Explain where CTI supports the SOC and where it does not replace controls or incident response.
- Distinguish an operational security event from an analytic conclusion.

## The security operations context

A SOC combines people, processes, and technology to monitor an organization's environment and coordinate defensive action. Common functions include alert triage, incident response, detection engineering, vulnerability management, threat hunting, and threat intelligence. Smaller teams may combine roles; clear ownership and escalation paths still matter.

A useful operational loop is:

**Prepare and instrument -> observe -> detect -> investigate -> contain/respond -> recover -> learn.**

Logging, asset context, identity controls, backups, and tested procedures establish the conditions for effective detection and response. A hunt cannot recover evidence that was never collected or retained.

## What CTI contributes

Cyber threat intelligence is evidence-based analysis about threats, adversaries, capabilities, opportunities, and likely effects, produced for a decision-maker. It helps answer a question such as: *Which threat behaviors should this organization prioritize, and what evidence would show that they are present?*

CTI can help teams prioritize vulnerabilities, enrich alerts, develop behavior-based detections, scope incident investigations, brief leadership, and improve security planning. It cannot guarantee attribution, replace local telemetry, or make an irrelevant indicator actionable by itself.

## From data to decision support

- **Data:** unprocessed observations, such as a DNS query or process event.
- **Information:** observations organized and given basic context, such as repeated DNS requests from one host.
- **Intelligence:** evaluated and interpreted information that answers a stakeholder question and informs a decision.

The transformation adds provenance, time, context, alternative explanations, confidence, and an action appropriate to the recipient. More data is not automatically more intelligence.

## SOC and CTI collaboration

| Partner | Useful exchange |
|---|---|
| SOC analyst | Alert enrichment, current behaviors, confidence, and investigation pivots. |
| Hunter | Testable behavior hypotheses, collection coverage, and hunt outcomes. |
| Incident responder | Campaign context, likely follow-on activity, and evidence requirements. |
| Detection engineer | Observable behavior, data prerequisites, false-positive risks, and test cases. |
| Vulnerability manager | Threat exploitation evidence, asset exposure, and prioritization rationale. |
| Leadership | Business risk, uncertainty, options, and decisions required. |

## Common failure modes

- Buying feeds without a requirement or consumer.
- Treating a threat actor label as proof of who caused an event.
- Blocking every indicator without validating relevance or operational impact.
- Producing polished reports that arrive too late to change a decision.
- Expecting the hunting team to compensate for missing logs or weak identity controls.

## Review prompts

1. What decision would a CTI product help one SOC stakeholder make?
2. Give an example of raw data, information, and intelligence from the same observation.
3. Why is threat intelligence not a substitute for incident response?
