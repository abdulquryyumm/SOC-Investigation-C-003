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
