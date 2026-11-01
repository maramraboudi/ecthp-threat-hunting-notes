# 8. Threat intelligence platforms

## Learning outcomes

- Explain typical TIP functions and their relationship to SIEM, SOAR, EDR, and case-management systems.
- Evaluate a TIP by outcomes, governance, and data quality rather than feature count.
- Identify risks of automation and feed overload.

## What a TIP can do

A threat intelligence platform (TIP) may centralize collection from internal and external sources, normalize data, deduplicate and enrich observables, retain provenance, correlate related objects, manage indicator lifecycles, support analyst collaboration, and distribute approved intelligence to other tools.

A TIP may connect to SIEM, SOAR, endpoint, network, ticketing, or sharing systems. These integrations have different purposes: a TIP manages intelligence context; a SIEM analyzes events; SOAR coordinates workflows; EDR provides endpoint telemetry and response controls. Product boundaries vary.

## A typical flow

**Sources -> ingest -> validate/normalize -> enrich -> analyst review -> prioritize -> share or operationalize -> measure -> expire/revise.**

Human review is important when an action could block business traffic, affect an account, or disseminate sensitive information. Automate low-risk enrichment first; require approvals and rollback paths for disruptive actions.

## Selection and governance questions

- Which intelligence requirements and consumers will the platform serve?
- Can it preserve provenance, confidence, source markings, and expiry?
- How does it represent relationships and avoid duplicate or conflicting objects?
- Which formats, schemas, APIs, access controls, and audit trails are supported?
- How are sensitive data, retention, access, deletion, and sharing controlled?
- Can analysts trace an automated block back to its source and reverse it?
- What operational effort is required to maintain parsers, integrations, and data quality?

## Common pitfalls

A TIP can amplify bad data at scale. Unvetted feeds create noise, stale indicators generate false positives, enrichment services may have privacy implications, and automation can block shared infrastructure. Measure whether the system improves decisions, reduces time to useful context, or improves detection quality. Feed volume alone is not a success metric.

## Review prompts

1. What should happen before a newly ingested indicator can trigger an automatic block?
2. What information must remain traceable after enrichment and deduplication?
3. Which outcome measures matter more than the number of feeds connected?
