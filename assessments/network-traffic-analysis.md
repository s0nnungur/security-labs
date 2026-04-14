# Network Traffic Analysis – DNS and ICMP Incident

## Context

Several users reported being unable to access the website
www.yummyrecipesforme.com. When attempting to load the page, users received a “destination port unreachable” error.

As part of the investigation, network traffic was captured using tcpdump while attempting to access the website.

## Observations

- DNS queries were sent from the client IP address 192.51.100.15 to the DNS server at 203.0.113.2.
- The queries were sent over UDP and targeted port 53, which is used for DNS.
- Each DNS request was followed by an ICMP error message stating:
  “udp port 53 unreachable.”
- The same error occurred repeatedly across multiple attempts.

## Analysis

The tcpdump logs indicate that the DNS resolution process failed before any HTTPS connection could be established.

Because DNS queries over UDP to port 53 consistently returned ICMP “port
unreachable” messages, the DNS server was unable to receive or process DNS requests. This suggests that no service was listening on port 53 or that traffic to this port was blocked.

The failure of DNS resolution prevented the browser from obtaining the IP
address of the website, making the site unreachable despite the web server
itself not being directly contacted.

## Protocols Involved

- UDP: Used to send DNS queries from the client to the DNS server.
- ICMP: Used by the DNS server to report that UDP port 53 was unreachable.

## Impact

- Users were unable to access the website.
- All services dependent on DNS resolution for this domain were affected.
- The issue occurred at the network and DNS layer, not at the application layer.

## Suspected Root Cause

The most likely cause of the incident is a DNS service failure due to one of the following:
- DNS service not running on the server
- Firewall or network rules blocking UDP traffic on port 53
- Misconfiguration of the DNS service

## Next Steps

- Verify that the DNS service is running on the affected server.
- Check firewall and network rules to ensure UDP port 53 is allowed.
- Restart or reconfigure the DNS service if necessary.
- Monitor traffic to confirm successful DNS resolution after remediation.
