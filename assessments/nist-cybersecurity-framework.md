# Incident Report – Denial of Service (DoS) Attack
## NIST Cybersecurity Framework (CSF)

## Context

The organization experienced a denial-of-service (DoS) attack that disrupted
internal network operations for approximately two hours. During the incident,
network services became unresponsive due to a flood of ICMP packets, preventing
legitimate internal traffic from accessing network resources.

The incident was contained by the incident response team, and a post-incident
analysis was conducted to improve the organization’s security posture using the
NIST Cybersecurity Framework (CSF).

## Summary

The DoS attack was caused by a malicious actor sending a high volume of ICMP
packets into the network through an unconfigured firewall. This traffic
overwhelmed network resources and caused a temporary outage of internal network
services.

Following containment and recovery, additional security controls were
implemented to prevent similar incidents in the future.

## Identify

The investigation identified the following risks and vulnerabilities:

- The firewall lacked rules to control or rate-limit incoming ICMP traffic.
- Source IP address verification was not enabled, allowing spoofed traffic.
- Limited monitoring capabilities delayed early detection of abnormal traffic
  patterns.

These gaps allowed a malicious actor to exploit ICMP traffic to perform a DoS
attack against the network.

## Protect

To reduce the likelihood of future attacks, the organization implemented the
following protective measures:

- Firewall rules to limit the rate of incoming ICMP packets.
- Source IP address verification on the firewall to detect and block spoofed
  IP addresses.
- Policies to ensure firewall configurations are reviewed and maintained
  regularly.

These controls help reduce exposure to denial-of-service attacks and improve
network resilience.

## Detect

Detection capabilities were improved by deploying:

- Network monitoring software to identify abnormal traffic patterns.
- An IDS/IPS system configured to detect and filter suspicious ICMP traffic.

These tools increase visibility into network activity and enable faster
identification of potential DoS attacks.

## Respond

During the incident, the response team:

- Blocked incoming ICMP traffic at the firewall.
- Took non-critical services offline to reduce network load.
- Restored critical network services as a priority.

For future incidents, response procedures include analyzing firewall logs,
network monitoring alerts, and IDS/IPS data to quickly contain threats and
identify attack sources.

## Recover

After containment, normal network operations were restored in phases, starting
with critical services. Firewall configurations and ICMP controls were verified
before fully restoring all services.

Post-recovery monitoring was maintained to confirm network stability and ensure
no residual malicious traffic remained. Lessons learned from the incident were
used to improve recovery processes and reduce downtime in future events.
