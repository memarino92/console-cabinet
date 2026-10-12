# Architecture (proposed)

> Status: **Proposal**, not an accepted implementation specification.

```text
Client (game selection + input + video playback)
  |                 ^
  v                 | encoded video
.NET Server         |
  | sessions        Video capture/encoder host
  |                 ^
  v                 | HDMI
Cabinet Agent       Real N64 + HDMI mod
  |         ^
  |         | native controller signaling
  v         |
MCU / cartridge loader / power-reset interface
```

## Logical boundaries
- **Server:** Catalog, session lifecycle, resource reservations, diagnostics, and UI/API. .NET is the intended stack.
- **Agent:** Machine-local access to game loader, capture hardware, and serial/USB devices. Could initially run on the same x86 host as the server.
- **Firmware:** Deterministic native controller protocol and reset/power electronics; no message bus on the MCU.
- **Video:** HDMI ingress, encoding, LAN transport, client decoding. The capture/encoder hardware and protocol remain unselected.
- **Storage:** Local test ROM directory initially; NAS as future authoritative storage, with console-specific staging/caching.

## Example session
Requested -> Reserving -> PreparingGame -> ConfiguringInput -> StartingConsole -> WaitingForVideo -> Running -> Stopping -> Completed. Errors transition to Failed, release reservations and preserve diagnostics.

Commands must be idempotent where practical. The observed hardware state is authoritative for recovery, not merely the last command issued.

## Open design questions
- Commercial flashcart interface for reliable programmatic N64 ROM selection.
- HDMI mod compatibility and installation effort for the chosen motherboard revision.
- Hardware capture latency and Linux support.
- Controller bridge electrical interface, voltage levels and timing.
- x86 mini PC selection; hardware encoder compatibility and latency.
- Direct-HDMI fallback for public demos.
- How to verify boot success beyond HDMI signal lock.
- Whether Server and Agent need separate processes in v0.

See [N64 milestone](../milestones/001-n64-vertical-slice.md) and [research](../research/).
