# Suspicious Network Behaviour Analysis

## Objective
To compare normal web browsing traffic with reconnaissance scan traffic.

## Environment
- Windows OS
- Wireshark
- Nmap

## Normal Traffic Analysis
Observed DNS queries followed by successful TCP handshakes.
Traffic pattern showed sequential communication typical of legitimate browsing.

## Scan Traffic Analysis
Observed multiple SYN packets sent to a single host across different ports.
Connections were not completed (half-open connections).
This behaviour indicates SYN scan reconnaissance activity.

## Detection Insight
Repeated half-open TCP connections to multiple ports can signal port scanning attempts.

## Conclusion
Basic packet inspection can help differentiate legitimate user activity from reconnaissance behaviour.
