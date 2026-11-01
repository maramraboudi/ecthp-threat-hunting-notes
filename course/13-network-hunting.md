# 13. Network threat hunting

## Learning outcomes

- Select network evidence that can test a hunt hypothesis.
- Recognize why baselines and protocol context matter.
- Explain packet capture, flow records, and metadata limitations.

## Data sources

Depending on architecture and policy, network hunts may use packet captures, NetFlow/IPFIX, DNS resolver logs, proxy and web gateway records, firewall events, IDS alerts, DHCP assignments, VPN records, TLS metadata, and network-device authentication logs. Each source answers different questions. Packet capture offers detail but may be unavailable or privacy-sensitive; flow records scale better but omit application payload.

## Build the baseline first

Understand normal protocols, ports, services, clients, destinations, and time patterns for the environment. Unusual does not mean malicious: service discovery, backup windows, software updates, and misconfigured devices can all produce outliers. Compare like with like (host role, subnet, time, business purpose) and account for NAT, proxies, and shared cloud services.

## Protocol-oriented review

- **DNS:** unusual query volume, rare names, suspicious response patterns, or host-to-resolver deviations; validate against enterprise services and resolver configuration.
- **HTTP(S):** method, host, path, status, user agent, timing, and byte counts where legitimately logged; TLS encryption limits payload visibility.
- **TCP:** connection state, unusual destinations or ports, repeated failures, and unexpected long-lived sessions.
- **ARP/DHCP:** unexpected address changes, duplicate assignments, or device behavior inconsistent with network role.
- **ICMP:** unexpected volume or patterns relative to local operational needs.

These are investigation cues, not signatures. Use multiple fields and corroborating data.

## Safe analysis workflow

1. State the hypothesis and capture scope.
2. Select the least intrusive available source that can test it.
3. Normalize time and join address assignments to asset/user context.
4. Compare with a baseline and known change activity.
5. Pivot to DNS, identity, endpoint, or application telemetry for validation.
6. Record data gaps and retention limits; avoid retaining unrelated payloads.

## Tools and query thinking

Packet analyzers such as Wireshark, command-line capture tools such as tcpdump, and flow or network-analysis tools can help inspect authorized lab data. A packet filter should be narrow and read-only; do not capture networks without permission. Start with a defined interface or provided capture file, a time window, and a protocol filter. Query examples must be adapted to local schemas, and a missing result may mean missing sensor coverage rather than no activity. A network sensor only sees traffic visible at its collection point; a workstation capture is not a view of the whole enterprise.

## Review prompts

1. What can flow records show that a packet capture can show in more detail?
2. Why should an unusual port be interpreted in host and service context?
3. Which other telemetry would help validate suspicious DNS activity?
