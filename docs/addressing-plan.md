# IPv4 addressing plan

The plan uses RFC 1918 private space created for this fictional lab. Host addresses are examples; no address was copied from a university or workplace network.

| VLAN | Zone | Subnet | Gateway | Example allocation |
|---:|---|---|---|---|
| 10 | Administration | `10.10.10.0/24` | `10.10.10.1` | DHCP `.100–.199` |
| 20 | Clinical | `10.10.20.0/24` | `10.10.20.1` | DHCP `.100–.199` |
| 30 | IT management | `10.10.30.0/24` | `10.10.30.1` | Static/DHCP `.50–.99` |
| 40 | Staff Wi-Fi | `10.10.40.0/24` | `10.10.40.1` | DHCP `.100–.219` |
| 50 | Guest Wi-Fi | `10.10.50.0/24` | `10.10.50.1` | DHCP `.100–.239` |
| 60 | Shared services | `10.10.60.0/24` | `10.10.60.1` | Servers `.10–.49` |
| 999 | Native/unused | No user subnet | None | No endpoints |

## Conventions

- `.1` is the default gateway.
- `.2–.9` are reserved for infrastructure where applicable.
- `.10–.49` are reserved for servers/appliances.
- DHCP ranges avoid infrastructure addresses.
- VLAN 999 is unused for endpoints and can be the explicitly configured native VLAN.

Using `/24` networks prioritises clarity and reproducibility. A future exercise can redesign them using VLSM after estimating realistic host counts.
