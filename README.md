# Cyber Threat Intelligence & Threat Hunting Study Guide

An independent, structured set of study notes that connects the CTI lifecycle to practical defensive threat hunting, including topics useful when preparing for INE's eCTHP certification. It is organized as a course: foundations, collection and analysis, hunting methods, network and endpoint investigations, and an integrated capstone.

> **Unofficial study aid.** This project is not created by, affiliated with, or endorsed by INE or any certification provider. Certification names and marks belong to their respective owners. Verify current exam objectives, eligibility, and course content with [INE](https://ine.com/learning/certifications). These notes do not reproduce the supplied course PDFs or provide exam answers.

## Start here

- [Course map and learning outcomes](course/INDEX.md)
- [Study plan](course/00-study-plan.md)
- [CTI foundations](course/01-soc-and-cti-foundations.md)
- [Threat hunting fundamentals](course/10-threat-hunting-fundamentals.md)
- [CTI-to-hunt workflow](course/12-intelligence-driven-hunting.md)
- [eCTHP-focused study crosswalk](course/17-ecthp-study-crosswalk.md)
- [Synthetic hunt lab](labs/README.md)
- [Original practice questions](practice/README.md)
- [References and source note](REFERENCES.md)

## What you will learn

- Translate organizational questions into intelligence requirements and a collection plan.
- Evaluate source reliability, information credibility, relevance, and confidence without overstating attribution.
- Use OSINT responsibly; normalize and enrich observables; understand STIX, TAXII, and TLP.
- Apply the Cyber Kill Chain and MITRE ATT&CK as complementary analytic models.
- Build scoped, testable hunt hypotheses from threat intelligence and local telemetry.
- Investigate network and endpoint evidence, document limitations, and turn validated findings into detections or response actions.

## Suggested sequence

1. Read the CTI foundation and lifecycle lessons.
2. Work through collection, OSINT, standards, analysis, and dissemination.
3. Study hunting strategy and hypothesis formation.
4. Practice network and endpoint hunts using authorized lab data.
5. Complete the capstone and original review questions; explain your reasoning before consulting the answer rationale.

## Safe use

All investigation exercises are defensive. Use synthetic data, public training datasets, or systems for which you have explicit authorization. Do not collect personal data unnecessarily, probe third-party systems, reuse real credentials, or publish sensitive indicators without permission. See [the course scope](course/00-study-plan.md#scope-and-safe-practice).

## Contents

```text
.
|-- README.md
|-- REFERENCES.md
|-- CONTRIBUTING.md
|-- labs/
|   |-- README.md
|   `-- synthetic-events.csv
|-- course/
|   |-- INDEX.md
|   |-- 00-study-plan.md
|   |-- 01-soc-and-cti-foundations.md
|   |-- 02-intelligence-types-and-indicators.md
|   |-- 03-intelligence-lifecycle.md
|   |-- 04-data-collection-and-quality.md
|   |-- 05-osint-method.md
|   |-- 06-sharing-standards.md
|   |-- 07-analytical-models.md
|   |-- 08-threat-intelligence-platforms.md
|   |-- 09-dissemination-and-feedback.md
|   |-- 10-threat-hunting-fundamentals.md
|   |-- 11-hunt-strategies-and-hypotheses.md
|   |-- 12-intelligence-driven-hunting.md
|   |-- 13-network-hunting.md
|   |-- 14-endpoint-hunting.md
|   |-- 15-analysis-detection-and-reporting.md
|   `-- 16-integrated-capstone.md
`-- practice/
    `-- README.md
```

The course modules are original summaries and learning aids, not a substitute for official training or current exam objectives.
