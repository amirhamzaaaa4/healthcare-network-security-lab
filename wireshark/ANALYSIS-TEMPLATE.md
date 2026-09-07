# Packet analysis template

> Status: Complete this only from a genuine authorised capture. Replace placeholders; do not guess.

## Test context

- Date:
- Lab topology version:
- Capture interface:
- Generated command:
- Display filter:
- Sanitisation performed:

## ICMP Echo Request

| Field | Observed value | Interpretation |
|---|---|---|
| Source IPv4 | `[record from capture]` | Sender |
| Destination IPv4 | `[record from capture]` | Target |
| Type / code | `[record]` | Expected Echo Request is type 8/code 0 |
| Identifier / sequence | `[record]` | Used to match request and reply |
| TTL | `[record]` | Decrements at routed hops |
| Frame length | `[record]` | Captured Ethernet frame size |

## Matching Echo Reply

| Field | Observed value | Interpretation |
|---|---|---|
| Source / destination | `[record]` | Expected to reverse request direction |
| Type / code | `[record]` | Expected Echo Reply is type 0/code 0 |
| Identifier / sequence | `[record]` | Should correspond to request |
| TTL | `[record]` | May help infer path behaviour; do not overstate |

## Conclusion

Describe what the packets demonstrate, any loss or anomaly, and the limits of the observation. A successful ping demonstrates ICMP reachability at that time; it does not prove that every application or port is available.
