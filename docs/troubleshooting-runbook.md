# Troubleshooting runbook

Work from the physical layer upward and record observations before changing configuration.

1. **Physical/link:** confirm device power, cable type, connected port, and green link state.
2. **Local configuration:** inspect IP address, prefix/mask, gateway, DNS server, and DHCP status with `ipconfig /all` or the Packet Tracer desktop tools.
3. **Local stack:** ping `127.0.0.1`, then the host's own address.
4. **Local segment:** ping a peer in the same VLAN; inspect the ARP table with `arp -a`.
5. **Gateway:** ping the VLAN gateway. Check switch access VLAN, trunk allowed VLANs, router subinterface tag, and interface state.
6. **Remote segment:** test a specifically permitted destination. A timeout may be an intended ACL result.
7. **Name resolution:** test the destination by IP, then by hostname; inspect DNS settings if only the hostname fails.
8. **Path:** use `tracert`/`traceroute` to identify the last responding hop. Do not assume every timeout is a routing failure because devices may suppress ICMP.
9. **Packet evidence:** capture only on an authorised lab interface and apply a narrow display filter.

## Incident note template

```text
Date/time:
Source and destination zone:
Expected result:
Observed result:
Commands/tests used:
Relevant configuration checked:
Root cause:
Corrective action:
Retest result:
Sanitised evidence path:
```
