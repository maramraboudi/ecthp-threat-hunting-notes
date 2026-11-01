# 3. The intelligence lifecycle

## Learning outcomes

- Build a complete intelligence workflow around a decision requirement.
- Explain why the lifecycle is iterative rather than a one-way pipeline.
- Identify quality checks at each phase.

## Lifecycle stages

1. **Planning and direction:** clarify the decision, audience, scope, and priority intelligence requirements (PIRs).
2. **Collection:** obtain relevant data from authorized internal and external sources.
3. **Processing and exploitation:** parse, normalize, deduplicate, translate, enrich, and prepare evidence for analysis.
4. **Analysis and production:** evaluate source and information quality, test explanations, assess confidence, and create a useful product.
5. **Dissemination:** deliver the product to the right person, in the right format and time.
6. **Feedback:** measure whether it helped and refine requirements, sources, and products.

The phases may overlap and repeat. New evidence can change a judgment; a consumer's response can create a new requirement.

## Planning: write a useful requirement

A good requirement is specific, decision-linked, and answerable within a defined period. Instead of "learn about ransomware," ask: "Which ransomware behaviors have been observed against our sector in the last six months, and which of our exposed services and telemetry sources affect priority?" Distinguish long-term PIRs from narrower collection questions.

Define scope, owner, urgency, confidence needs, and how the result will be used. Planning prevents indiscriminate collection and reduces privacy and storage risk.

## Collection and processing controls

Choose sources because they can answer the requirement, not merely because they are available. Record collection method, timestamps, licensing or sharing constraints, and known gaps. During processing, preserve the original artifact, parse into a consistent schema, retain source references, and avoid changing the meaning of timestamps or fields.

## Analysis and production

Separate facts, assumptions, and judgments. Seek corroboration, consider benign alternatives, and record confidence with its basis. Do not equate repeated reporting from sources that all copied the same original report with independent corroboration. State what is unknown and what new evidence would change the assessment.

## Dissemination and feedback

A flash alert, technical report, executive brief, and hunt hypothesis are different products. Select one based on the audience and decision. Feedback should ask about timeliness, relevance, clarity, false positives, and whether the recipient acted. A report that is accurate but unusable has not completed the cycle.

## Worked example: suspicious authentication activity

- **Direction:** determine whether recent unusual sign-ins may involve targeted credential abuse and whether response is needed.
- **Collection:** identity-provider logs, endpoint logons, VPN records, approved threat reporting, and asset/user context.
- **Processing:** normalize time zones and user identifiers, deduplicate events, preserve provenance.
- **Analysis:** compare baseline, source quality, geography/device context, session behavior, and benign explanations.
- **Production:** give the SOC a scoped set of accounts, time window, evidence, confidence, and recommended validation steps.
- **Feedback:** measure useful leads, misses, and missing telemetry; revise the next requirement.

## Review prompts

1. What decision would your PIR support?
2. Where can provenance be lost during processing?
3. What feedback would tell you the intelligence product changed an outcome?
