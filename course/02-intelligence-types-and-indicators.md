# 2. Intelligence types and indicators

## Learning outcomes

- Match strategic, operational, tactical, and technical intelligence to its audience.
- Explain what an indicator can and cannot establish.
- Use indicator context, age, confidence, and expected lifetime in defensive decisions.

## Intelligence by decision horizon

| Type | Typical question | Example product |
|---|---|---|
| Strategic | What threat trends may affect our organization or sector? | Leadership assessment tied to business choices. |
| Operational | Which campaigns or capabilities are relevant, and how may they develop? | Campaign brief for incident response and planning. |
| Tactical | Which behaviors and procedures should defenders anticipate? | ATT&CK-mapped behavior summary for detection engineering. |
| Technical | What observable artifacts can be searched or shared now? | A qualified, time-bounded indicator set with provenance. |

These categories overlap. A tactical finding can inform a strategic risk decision, but the product should still fit the consumer's needs and technical depth.

## Indicators and observables

An indicator of compromise is an observable artifact that may be associated with malicious activity in a defined context. Examples include a file hash, domain, IP address, certificate, email artifact, process relationship, or behavioral sequence. An observable is not automatically malicious: a public cloud IP may host many unrelated tenants, and a process name can be spoofed.

Assess indicators using:

- **Specificity:** how uniquely it points to the activity of interest.
- **Provenance:** who reported it, how it was collected, and whether the source is primary.
- **Confidence:** how strongly evidence supports the analytic claim.
- **Freshness and lifetime:** when it was observed and how quickly it may become stale.
- **Relevance:** whether it intersects with the organization's assets and threat model.
- **Actionability and risk:** what control can use it, and what disruption a false positive could cause.

Keep the observation distinct from the inference. "A process connected to this address at this time" is an observation; "this proves actor X compromised the host" is a much stronger claim requiring corroboration.

## Indicator lifetime and the Pyramid of Pain

The Pyramid of Pain is a conceptual model: hashes and simple infrastructure are often easy to change, while behavior and adversary procedures can be more costly to replace. It is not a guarantee that every TTP is unique or durable. Combine short-lived indicators for fast matching with behavior-focused detections that remain useful when infrastructure changes.

An indicator lifecycle includes discovery, validation, contextualization, operational use, monitoring for change, expiry or revocation, and lessons learned. Expiration and review dates prevent stale data from silently becoming a permanent blocklist.

## Practice

For a reported domain, write down source, first/last observed time, associated behavior, confidence, relevance to local assets, possible benign use, and a proposed response. Decide whether to alert, investigate, block, monitor, or reject it, and explain why.

## Review prompts

1. Which intelligence type best supports a board-level investment decision? A detection rule? A short-lived block?
2. Why should an IP address match not be treated as actor attribution?
3. What conditions should cause an indicator to expire or be re-evaluated?
