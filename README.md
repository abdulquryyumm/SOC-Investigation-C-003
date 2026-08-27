# SOC-Investigation-C-003
Suspicious DNS Activity

## 1. Investigation Overview
This investigation focused on a suspicious DNS activity, using the available PCAP file to examine the incident and determine whether the activity was normal, suspicious, or malicious.

## Evidence
- Primary evidence: Wireshark PCAP file.
- Random-looking subdomains were observed.
- DNS queries occurred at very short intervals.
- Different subdomains resolved to the same destination IP address.

  ## Findings
- Source IP: `10.0.2.15`
- DNS server: `10.0.2.3`
- 20 suspicious DNS queries were identified.
- The queries resolved to `203.0.113.77`.
- The activity occurred between approximately 7.80 and 9.44 seconds.

## Analysis
The subdomains were random-looking, and the queries occurred roughly every 0.18 seconds. There were 20 queries within a very short period, and the different subdomain names resolved to the same IP address. The pattern appeared automated rather than the result of normal human interaction.

## Business Risk
- Potential data transfer or leakage of confidential company information.
- Disruption of the affected employee's operations and productivity.
- Potential lateral movement to other systems if the affected host is compromised.

## Conclusion
The DNS activity is classified as suspicious because of the random-looking subdomains, the short intervals between queries, and the fact that the queries resolved to the same destination IP address. The available evidence shows the behaviour observed but does not establish the intent behind the activity.

