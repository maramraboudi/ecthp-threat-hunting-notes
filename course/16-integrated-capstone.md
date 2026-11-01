# 16. Integrated capstone: from CTI question to hunt

## Scenario

A fictional industry-sharing group reports that organizations in your sector have seen unusual identity-provider sign-ins followed by a new background service on a small number of Windows servers. The report names no victim and provides no verified indicator. Your organization operates customer-facing services and has identity logs, EDR process telemetry, and firewall/DNS records, but retention differs by source.

This exercise uses no real target, indicator, or exploit. It tests analytical planning and defensive evidence handling.

## Tasks

### 1. Direction

Write one decision-linked PIR and two collection questions. Identify the stakeholders who should receive the eventual result and who owns any response action.

### 2. Source evaluation

List what you know about the report's provenance, recency, directness, corroboration, and uncertainty. State what you cannot conclude about actor identity or campaign attribution.

### 3. Prioritize

Assess relevance to your fictional assets, likely impact, actionability, confidence, and telemetry coverage. Explain whether to hunt now, gather more intelligence, or first improve data collection.

### 4. Hypothesis and scope

Write a falsifiable hypothesis about the reported sequence. Define a time window, in-scope servers, required fields, expected evidence, benign alternatives, and stop/escalation conditions.

### 5. Analysis plan

Describe how you would correlate identity sign-ins, endpoint process/service events, DNS, and firewall records. Explain normalization of timestamps and how you would account for log gaps or shared infrastructure.

### 6. Findings and dissemination

Prepare two short conclusions: one for a SOC/hunter and one for a manager. Each must separate observation from assessment, state confidence and limitations, and recommend a proportionate next action.

### 7. Feedback

Choose measures for hunt value, such as validated leads, time to useful evidence, detection improvements, or telemetry gaps closed. Avoid counting raw queries as success.

## Suggested output checklist

- PIR and collection plan.
- Source-quality note.
- Hunt hypothesis and data matrix.
- Alternative-explanation list.
- Sanitized analytic summary.
- Follow-up detection/control and feedback owner.

There is no single correct conclusion. The quality of reasoning, evidence provenance, scope discipline, and uncertainty handling matter more than guessing an actor name.
