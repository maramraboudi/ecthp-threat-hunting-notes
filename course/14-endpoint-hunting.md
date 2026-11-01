# 14. Endpoint threat hunting

## Learning outcomes

- Identify endpoint telemetry relevant to process, identity, persistence, and execution hypotheses.
- Recognize common Windows event sources and their limits.
- Build a behavior-first investigation rather than relying on filenames alone.

## Endpoint evidence

Useful sources may include EDR telemetry, Windows Security logs, Sysmon, PowerShell logs, service and scheduled-task events, registry auditing, file events, application control, and identity-provider records. Verify collection, configuration, retention, time synchronization, and host coverage before drawing conclusions.

Examples of useful event families include process creation, logon success/failure, account/group changes, service installation, scheduled-task registration, and PowerShell operational logging. Sysmon event IDs often used in investigations include process creation (1), network connection (3), process access (10), file creation (11), and registry events (12-14); availability and meaning depend on the deployed Sysmon version and configuration. Windows Security event IDs also depend on audit policy. Confirm local documentation rather than assuming a field exists.

## Process and persistence questions

For a process event, retain parent and child image, command line, user, host, timestamp, integrity level, signer/hash where available, and nearby activity. Names alone are weak evidence: legitimate binaries can be abused, and names can be changed.

For persistence hypotheses, look for unexpected changes to services, scheduled tasks, autorun locations, accounts, or privileged groups. Compare with software deployment, IT maintenance, and approved administrative tooling. Correlate changes with the creating process and identity, not only the resulting object.

## Hunt workflow

1. Confirm asset, time window, and available endpoint sensors.
2. Select a behavior and define expected process/account/configuration evidence.
3. Query a narrow population; compare with host role and baseline.
4. Pivot by process ancestry, user, host, time, network connection, and related file/configuration events.
5. Validate with change records and a second data source.
6. Escalate suspected active compromise through incident response.

## Detection query concepts

A defensive search can filter process-creation telemetry for unusual parent/child combinations or suspiciously rare command-line characteristics, then group by signer, user, host role, and prevalence. Treat terms as leads, not proof. For example, a string match for a script interpreter is too broad by itself; tune with parent process, command context, user, destination, and baseline.

Do not run commands or manipulate endpoints to reproduce adversary persistence outside an explicitly authorized disposable lab. Detection validation should use benign simulations approved by the organization.

## SIEM workflow

In a SIEM such as Splunk or an Elastic-based stack, first select the correct data source/index and time range, then inspect field names and event coverage before composing a search. Normalize host and user identities, filter to the scoped behavior, summarize frequency and peer prevalence, and inspect a small set of relevant records. Search syntax and schemas differ by deployment; copy neither a query nor an event ID without confirming local collection and field mappings.

For process-creation telemetry, a generic investigation may group records by host, user, parent process, child image, signer, and time. For logon or persistence questions, join the relevant security or endpoint event with identity, host role, maintenance, and change context. Keep broad searches bounded to reduce load and protect privacy.

## Review prompts

1. Why is process name alone a weak indicator?
2. What additional context helps distinguish a service installation from approved software deployment?
3. What does the absence of an event mean if the audit policy was not enabled?
