# Practice and self-check

These are original study questions written for this guide. They are not copied from a certification exam or answer key. Try each prompt before opening the rationale.

## Questions

1. A vendor bulletin lists an IP address associated with a malware sample from eight months ago. What should you check before adding it to a blocklist?
2. A hunt based on a report returns no matching endpoint events. Name at least three reasons this does not prove the behavior was absent.
3. Explain the difference between STIX and TAXII in one sentence each.
4. A public JavaScript bundle reveals an administrative route, but the server returns an authorization denial to a normal user. What has been shown, and what has not?
5. You find a process-creation event with an unusual parent-child relationship. What context and corroboration would you seek before calling it malicious?
6. A source's report is copied by five other blogs. How does that affect your confidence in the claim?
7. Write a falsifiable hunt hypothesis for detecting unexpected service creation on a defined set of lab hosts.
8. Which should take precedence: preserving a low-confidence indicator match or following incident-response policy after corroborating active compromise? Explain.
9. A TLP:AMBER item arrives through an external feed. What should the recipient verify before sharing it with a partner?
10. A network hunt finds outbound DNS queries to a rare domain. Name two benign explanations and two additional data sources that could help assess the activity.

## Suggested reasoning

1. Check provenance, first/last observation, context, confidence, shared hosting, internal relevance, expected lifetime, possible business impact, and expiry. A stale or shared address may not be safe to block.
2. Sensor coverage may be absent, retention may have expired, the parser/field may be wrong, time zones may be inconsistent, or the behavior may differ from the report. Validate the telemetry first.
3. STIX represents structured threat information; TAXII is a protocol for exchanging such information.
4. Route disclosure and reconnaissance aid are shown; server-side authorization failure is not. Keep testing within the authorized lab.
5. Parent/child process, user, host role, command context, signer, time, change windows, prevalence, related file/network/identity events, and benign software activity.
6. Repetition may reflect copying rather than independent corroboration. Trace the claim to its origin and seek independent evidence.
7. Example: "If unauthorized persistence was established on the in-scope lab hosts during the review window, endpoint audit data should show a new service registration outside approved change activity, correlated with its creating process and account." Define scope, logs, alternatives, and stop criteria.
8. Escalate corroborated active compromise through policy. Preserve relevant evidence; do not allow an unvalidated indicator task to delay response.
9. Verify the current TLP definition, permitted recipient, organizational policy, original source, and whether the partner is allowed to receive that information. TLP is handling guidance, not access control.
10. Benign software updates or enterprise security tools are possible; correlate with endpoint process data, proxy/firewall logs, DNS resolver history, asset role, change records, or vendor documentation.

## Practical drills

- Take one public advisory and record claim, source, date, evidence, uncertainty, relevant behaviors, and one local question.
- Given a synthetic event bundle, write a hunt hypothesis and list the telemetry needed to test it.
- Create a short technical handoff and a separate management summary from the same fictional evidence.
