# Synthetic hunt lab

`synthetic-events.csv` is a small fictional dataset created for this guide. Hosts, users, events, and destinations are illustrative; `198.51.100.24` is in a documentation-only address range and `example.test` is reserved for examples. The file contains no real telemetry.

## Exercise: investigate a suspicious sequence

1. Load the CSV into a spreadsheet, notebook, or local test SIEM.
2. Filter for `process_start` events and group by host, parent process, process, and user. Identify a relationship worth investigating.
3. Correlate that host and time with `network_connection` events. State what is known and what cannot be inferred from the destination alone.
4. Review `service_created` and authentication events. Use `change_ticket` as one context field, not as proof that an event is safe.
5. List two benign explanations and the additional evidence needed to distinguish them.
6. Write a finding with scope, observations, confidence, limitations, and a proportionate next action.

## Expected reasoning

The WS-17 process and network events are a lead because a user-launched scripting process followed by an outbound connection may merit review. The log does not show the script content, process command line, destination ownership, or full endpoint context, so it does not prove malicious activity. The SRV-04 service event has a change reference and a subsequent connection, which should be checked against the approved change and binary provenance. Authentication failures followed by success on WS-31 warrant contextual review but may reflect a mistyped password. Correlate with identity-provider records, EDR, DNS/proxy logs, change management, asset ownership, and a baseline before deciding.

This exercise is about evidence-led analysis, not assigning a threat actor or taking action against an external host.
