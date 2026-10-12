# Controller interface research

**Status:** Open investigation.

Goal: client controller state -> wired Ethernet -> microcontroller -> native N64 controller port; return rumble/status where practical.

Research BlueRetro as a reference implementation, subject to its license and hardware compatibility. Establish voltage, open-drain/line driving requirements, timing, ground reference and protection before wiring.

Incremental test:
1. Original controller baseline.
2. Known-good adapter reproduces native controller behavior.
3. MCU local fixed button-state test.
4. Wired network input injection.
5. End-to-end timing, disconnect and reconnect behavior.

Never drive the console's data line directly from an unverified GPIO configuration.
