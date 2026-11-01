# 6. CTI sharing standards and protocols

## Learning outcomes

- Explain how structured formats support machine-readable sharing.
- Distinguish STIX content from TAXII transport.
- Apply handling labels without treating them as technical access controls.

## STIX

Structured Threat Information Expression (STIX) is a structured language for representing cyber threat information. STIX 2.x uses objects and relationships to describe items such as threat actors, campaigns, malware, tools, indicators, attack patterns, vulnerabilities, sightings, and analytic reports. The graph of relationships can express context more richly than a flat indicator list.

A STIX object is not automatically accurate or useful. Producers still need provenance, timestamps, confidence, marking/handling rules, and lifecycle management. Consumers should validate schemas, preserve source references, and avoid treating an indicator object as proof of malicious activity.

## TAXII

Trusted Automated eXchange of Intelligence Information (TAXII) is an application-layer protocol used to exchange CTI, commonly STIX content, between services. In short: **STIX describes the information; TAXII supports its exchange.** They can be used separately; not every STIX feed is delivered over TAXII.

## Other formats and their context

- **OpenIOC** is an earlier open format for describing indicators; check whether current tools and partners still support it.
- **CybOX** was an earlier observable-expression effort whose concepts were incorporated into STIX; it is not generally a separate modern transport protocol.
- **IODEF** describes incident information for exchange and coordination; it serves a different but adjacent purpose.

Before selecting a format, check current specifications, product support, required extensions, and the receiving partner's profile. Version mismatches and inconsistent interpretation can undermine interoperability.

## TLP 2.0

The Traffic Light Protocol communicates intended sharing boundaries. It is a handling convention, not encryption, authorization, or a substitute for organizational policy:

| Marking | General handling intent |
|---|---|
| TLP:RED | Limited to named recipients; do not share further. |
| TLP:AMBER+STRICT | Share within the recipient's organization only. |
| TLP:AMBER | Share within the recipient's organization and its clients, as appropriate to the original purpose. |
| TLP:GREEN | Share within the community; do not publish publicly. |
| TLP:CLEAR | May be shared publicly, subject to copyright and applicable rules. |

Use the current [FIRST TLP standard](https://www.first.org/tlp/) and local policy. Do not silently downgrade handling markings when copying data to another system.

## Practical sharing checklist

- Validate format and schema version.
- Preserve source, created/modified/validity times, confidence, and relationships.
- Apply handling markings and verify the consumer is permitted to receive the data.
- Minimize personal and sensitive information.
- Define expiry, revocation, deduplication, and correction procedures.
- Test what the consumer actually does with the shared content.

## Review prompts

1. What is the distinction between STIX and TAXII?
2. Why is TLP not a technical access-control mechanism?
3. What metadata would you preserve when sharing an indicator?
