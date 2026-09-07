# Architecture

## Requirements

- Isolate clinical, administrative, IT, staff wireless, guest, and services traffic.
- Keep device management reachable only from the IT segment.
- Give guest devices no route to internal subnets.
- Provide a small services zone for DHCP/DNS simulation.
- Make every component reproducible in Cisco Packet Tracer with no specialist hardware.

## Logical components

| Component | Suggested Packet Tracer device | Purpose |
|---|---|---|
| Edge router | ISR router with 802.1Q support | Default gateways and inter-VLAN routing |
| Access switch | 2960-class switch | VLAN access and trunking |
| Wireless access points | Two APs | Separate staff and guest wireless networks |
| Services host | Generic server | DHCP and DNS lab services |
| Endpoints | PCs/laptops/tablets | Representative clinic clients |
| Internet test target | Optional server beyond second router | Controlled external-connectivity simulation |

## Trust boundaries

The router subinterfaces form the Layer 3 boundary between zones. The switch trunk carries tagged VLAN traffic. Wireless clients join only their assigned SSID/VLAN. ACLs are a proposed extension that enforce the traffic policy in `security-design.md`.

## Scope boundaries

This is an educational simulation, not a production healthcare design. It contains no patient systems, medical-device certification assumptions, high-availability design, regulatory compliance claim, or connection to a real clinic.
