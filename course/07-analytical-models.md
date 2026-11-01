# 7. Analytical models for CTI

## Learning outcomes

- Use the Cyber Kill Chain and ATT&CK to structure questions, not to label every incident mechanically.
- Identify prevention, detection, disruption, and recovery opportunities.
- Reduce analytic bias and show uncertainty.

## Cyber Kill Chain

The Lockheed Martin Cyber Kill Chain presents an intrusion as a sequence of broad stages: reconnaissance, weaponization, delivery, exploitation, installation, command and control, and actions on objectives. Its value is in asking where a chain might be interrupted and what evidence exists before impact. Real operations may skip, repeat, or reorder stages; cloud, identity, and insider activity may not fit neatly into a linear model.

## Courses of action

A defensive course-of-action matrix maps stages or behaviors to possible responses. Typical defensive verbs include discover, detect, deny, disrupt, degrade, deceive, and destroy. Use only actions authorized by policy and proportionate to evidence. Deception or active disruption requires governance, safety review, and explicit authority; do not improvise counterattacks.

## MITRE ATT&CK

ATT&CK is a knowledge base of adversary behaviors observed and documented across domains. It organizes **tactics** (the adversary's objective in a context), **techniques** (how an objective is achieved), and **sub-techniques** (more specific implementations), with supporting procedures, mitigations, and data components.

Use ATT&CK to:

- Translate reporting into behavior-focused hunt questions.
- Identify relevant telemetry and detection coverage.
- Describe observed behavior using a shared vocabulary.
- Compare documented activity and plan defensive improvements.

ATT&CK is not a complete attack checklist, an attribution engine, or a maturity score. A technique mapping means evidence was assessed as consistent with that behavior; it does not prove a specific actor. Matrices and identifiers change, so link to the current ATT&CK page and record version/context.

## Combining the models

The Kill Chain gives a high-level temporal sequence and highlights intervention points. ATT&CK provides more granular behavioral descriptions. A useful analysis may use both: identify a broad stage, map observed behavior to ATT&CK, state the evidence and data source, then identify a defensive action. Avoid forcing an event into a technique when the evidence is insufficient.

## Structured analytic techniques

Analysts can reduce bias with explicit techniques, including:

- **Analysis of competing hypotheses:** list plausible explanations, identify evidence that distinguishes them, and test evidence against each.
- **Key assumptions check:** make hidden assumptions visible and consider what would invalidate them.
- **Red team analysis:** examine how an adversary could exploit a defensive assumption, within authorized analytic planning.
- **Indicators and signposts:** define observable developments that would raise or lower confidence in an assessment.
- **Timeline and link analysis:** organize events and relationships while retaining source and uncertainty.

No technique removes bias automatically. Document judgment, evidence quality, alternatives, and confidence.

## Review prompts

1. When is a linear kill-chain model a poor fit?
2. What is the difference between an ATT&CK tactic and technique?
3. How would competing-hypothesis analysis challenge an early attribution?
