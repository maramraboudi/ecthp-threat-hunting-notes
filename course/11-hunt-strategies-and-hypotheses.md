# 11. Hunt strategies and hypotheses

## Learning outcomes

- Select a hunt strategy appropriate to the trigger and available evidence.
- Write a falsifiable, bounded hypothesis.
- Plan what telemetry would support or challenge it.

## Common hunt strategies

These labels are practical categories, not a universal taxonomy:

- **Structured / TTP-led:** start from a documented behavior or technique and look for evidence of its execution.
- **Unstructured / exploratory:** investigate an analyst-observed anomaly or pattern that lacks a complete threat narrative.
- **Situational / risk-led:** respond to a new vulnerability, campaign, incident, business exposure, or change in threat context.
- **Indicator-led:** pivot from a qualified indicator, checking provenance, context, and age before searching.

A hunt may combine these. Keep the question clear enough that another analyst can reproduce the reasoning.

## Hypothesis design

A useful hypothesis states:

> Given **[specific threat behavior or risk]**, we expect **[observable evidence]** in **[data sources]** during **[time window]** on **[in-scope assets]**, unless **[known limitation or alternative]** explains it.

It should be testable and falsifiable. Avoid framing the hunt as a conclusion, such as "Actor X is inside our network." Prefer a behavior statement, such as "If unauthorized persistence was established on managed Windows endpoints, we may find new autorun-related changes followed by an unusual process launch during the review window."

## From hypothesis to data plan

1. Identify assets and an approved time range.
2. Map the behavior to observable events and data sources.
3. Check source coverage, retention, parsers, and timestamp quality.
4. Define a baseline or peer group for comparison.
5. List benign explanations and what would distinguish them.
6. Decide how to validate a lead and when to escalate.
7. Record expected outcomes before querying to reduce confirmation bias.

## Example: unusual child process

**Trigger:** a detection-engineering review identifies a rarely observed parent/child relationship in endpoint telemetry.
**Hypothesis:** on managed endpoints, this process relationship may indicate an unexpected script-driven execution during the specified period.
**Data:** process creation records with image path, parent, command line, user, host, timestamp, and signature/reputation context.
**Alternatives:** software deployment, administrative scripts, approved IT tooling, or incomplete parent-process telemetry.
**Validation:** compare against change windows and host role, then corroborate with related file, identity, and network events.
**Outcome:** document confirmed benign activity, suspicious evidence, or inconclusive results and telemetry gaps.

The example intentionally avoids a ready-to-run malicious command; the goal is reasoning over defensive telemetry.

## Review prompts

1. What evidence would falsify your hypothesis?
2. How does an unstructured hunt differ from an unbounded search?
3. Why define benign explanations before reviewing results?
