# Cisco Packet Tracer build guide

This guide produces a genuine `.pkt` file on Amir's own system. No binary lab file is included in this repository.

## 1. Place and name devices

Add one router, one managed switch, two wireless access points, one server, and representative endpoints. Use neutral names such as `R-EDGE`, `SW-ACCESS`, `AP-STAFF`, `AP-GUEST`, `SRV-NET`, `PC-ADMIN`, `PC-CLINICAL`, and `PC-IT`.

## 2. Cable the topology

Connect the router to the switch, the server and wired endpoints to access ports, and each AP to its assigned access port. Let link negotiation complete before troubleshooting.

## 3. Create VLANs and assign ports

Create VLANs 10, 20, 30, 40, 50, 60, and 999. Assign each endpoint/AP/server port to its intended access VLAN. Configure the router uplink as an 802.1Q trunk and permit only required VLANs.

## 4. Configure routing

Create one router subinterface per routed VLAN, using the gateway addresses in the addressing plan. Apply matching `encapsulation dot1Q` tags and enable the parent interface.

## 5. Configure addressing and services

Start with static endpoint addresses to simplify fault isolation. Then optionally configure DHCP pools, excluding gateways and reserved ranges. Configure a fictional DNS record such as `portal.clinic.example` pointing to the lab server. The `.example` domain is reserved for documentation.

## 6. Configure wireless

Use separate non-sensitive SSIDs such as `Clinic-Staff-Lab` and `Clinic-Guest-Lab`. Never commit passphrases. Record only `[REDACTED]` in screenshots or notes. Map each AP to the correct VLAN.

## 7. Baseline tests before ACLs

Verify host configuration, same-VLAN communication, each gateway, permitted inter-VLAN paths, DHCP, and DNS. Save a baseline copy of the `.pkt` file locally.

## 8. Add proposed ACL policy

Adapt the examples in `configs/` to the exact Packet Tracer device/IOS feature set. Test both allowed and denied paths. A security control is not verified by a successful test alone: record at least one expected allow and one expected deny.

## 9. Save genuine evidence

Save the completed `.pkt` file and add sanitised screenshots using the screenshot checklist. Update the implementation ledger from **Proposed** to **Verified** only for tests that pass.

## Test matrix

| Test | Expected after policy | Actual | Evidence |
|---|---|---|---|
| Admin host → admin peer | Allow | Pending | — |
| Clinical host → services DNS | Allow | Pending | — |
| IT host → switch management | Allow | Pending | — |
| Admin host → switch management | Deny | Pending | — |
| Guest host → clinical host | Deny | Pending | — |
| Guest host → simulated internet | Allow | Pending | — |
