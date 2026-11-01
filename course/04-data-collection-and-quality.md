# 4. Data collection and quality

## Learning outcomes

- Build a collection plan using internal, public, community, and commercial sources.
- Evaluate coverage, provenance, reliability, timeliness, and legal constraints.
- Identify data gaps that limit an analysis or hunt.

## Collection begins with the question

Start with the requirement and list the evidence needed to answer it. A useful plan records: question, source, owner, collection method, time range, expected fields, sensitivity, retention, access restrictions, and known blind spots. Collect the minimum useful data, under approved policy.

## Source families

**Internal sources** may include endpoint detection, operating-system events, identity and authentication services, DNS, DHCP, firewall and proxy logs, email security, cloud audit events, application and database logs, vulnerability inventories, incident records, and previous hunt results. These sources show what happened in the organization's environment, subject to their coverage and configuration.

**External sources** may include government advisories, vendor research, standards, vulnerability records, public malware analysis, carefully vetted open-source reporting, information-sharing communities, and commercial threat services. External reports offer context; they do not prove an indicator is present locally.

## Source evaluation

Track two separate judgments:

- **Source reliability:** how dependable the source has been and how it obtained the information.
- **Information credibility:** how plausible and corroborated this specific claim is.

A reputable source can publish an uncertain claim; an unknown source can provide a claim later corroborated elsewhere. Record what you know rather than collapsing both into a single unexplained score. Admiralty-style grading systems are useful shorthand only when their definitions are applied consistently and explained to consumers.

Evaluate:

1. Origin and collection method.
2. Direct observation versus hearsay or copied reporting.
3. Recency and whether the information has changed.
4. Independent corroboration and confidence.
5. Relevance to your assets, sector, geography, and controls.
6. Sharing, privacy, licensing, and retention conditions.

## Data quality and coverage

Normalize timestamps to a documented standard, preserve original values, handle missing fields explicitly, deduplicate without erasing provenance, and map fields carefully. Enrichment (for example, ASN or certificate metadata) adds context but may be inaccurate or stale. Keep the original value alongside enrichment and note when/how it was obtained.

For hunts, construct a telemetry coverage matrix: behavior of interest, data source, required fields, retention period, collection status, parser quality, and owner. A negative query result is meaningful only if the relevant sensor was active, correctly configured, and retained data for the time period.

## Review prompts

1. Which internal source could confirm whether a reported behavior occurred locally?
2. How do source reliability and claim credibility differ?
3. Why should normalized data retain the original value and provenance?
