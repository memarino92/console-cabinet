# N64 prototype bill of materials (candidate, not a purchase order)

> Status: Research. Prices, availability and compatibility have **not** been verified for an order.

| Component | Candidate | Purpose | Status |
|---|---|---|---|
| N64 | Working console with original PSU, heatsinks, Jumper Pak | Authentic execution | Needed |
| Cartridge loader | SummerCart64 or equivalent developer-friendly flashcart | Stage game images | Verify unattended loading |
| HDMI output | PixelFX Retro GEM N64 kit or compatible alternative | Digital output | Verify motherboard and install |
| Capture | Linux-compatible USB 3 HDMI capture, possibly Magewell | Ingest audio/video | Benchmark latency first |
| Host | Intel N100 or used Intel business mini PC with Quick Sync | .NET Agent, capture/encode | Compare options |
| Node MCU | Ethernet-capable ESP32 or MCU + wired interface | Reset and controller interface | Prototype/validate |
| Controllers | Original N64 controller + modern USB controller | Baseline and client | Needed |
| Cabling | HDMI, USB, Cat6, N64 controller extension | Interconnects | Needed |
| Network | Existing router/switch, wired Gigabit | Test transport | Reuse if possible |
| Storage | Existing laptop/host disk | Game image staging | No NAS required |
| Electronics | Iron, flux, multimeter, wire, insulation, microscope as needed | Safe assembly/debugging | Inventory existing tools |

## Procurement gates
1. Confirm the N64 revision and HDMI mod compatibility.
2. Demonstrate manual game loading before relying on remote automation.
3. Confirm capture device formats and Linux drivers.
4. Validate physical and electrical controller connections.
5. Defer road rack purchase until component measurements and cooling design exist.

## Future portable exhibition profile
Preference: approximately 8U molded Gator/SKB-style road rack, single power and display hookup, private offline-capable network, optional direct HDMI fallback. This is a **design preference**, not an approved enclosure or verified fit.
