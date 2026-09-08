# Sanitised evidence register

This folder contains only genuine screenshots extracted from my coursework. None were generated, reconstructed, or presented as proof that the fictional clinic lab is complete.

## Approved images

| File | What it demonstrates | Sanitisation applied | Evidence boundary |
|---|---|---|---|
| `packet-tracer-wired-wireless-topology.png` | Packet Tracer layout with wired and wireless endpoints | Cropped to the topology; re-encoded as PNG to discard document metadata | Prior coursework skill; not the clinic topology |
| `packet-tracer-segmented-topology.png` | Organising endpoints into separate functional groups | Cropped to the topology; re-encoded as PNG to discard document metadata | Visual grouping only; not proof of VLAN or ACL configuration |
| `wireshark-icmp-analysis-sanitised.png` | Filtering and inspecting ICMP Echo Request/Reply traffic | Application chrome cropped; source/destination addresses and raw frame bytes covered with opaque redaction; re-encoded as PNG | Prior coursework skill; not a clinic-lab capture |

## Material deliberately excluded

- Assessment-question pages and university instructions.
- Third-party router, switch, cabling, connector, and product images.
- Router setup screens that exposed passwords or security answers.
- Command prompts containing personal user paths, student numbers, or real network details.
- Captures exposing public/private addresses, real MAC addresses, or raw packet bytes that could not be safely presented.

## Checklist for future clinic-lab evidence

Before committing every image:

- Crop out desktop notifications, browser tabs, account names, and unrelated applications.
- Remove student numbers, university branding/private addresses, lecturer details, and assessment text.
- Redact real MAC/public IP addresses, SSIDs, credentials, and secrets.
- Use only the fictional lab hostnames and RFC 1918 addresses in this repository.
- Confirm the screenshot represents a test actually performed.
- Add a caption in the relevant document describing the expected and observed result.

Do not use blank, generated, or reconstructed images that could be mistaken for evidence. Keep original `.pkt` and capture files private until they have been manually reviewed.
