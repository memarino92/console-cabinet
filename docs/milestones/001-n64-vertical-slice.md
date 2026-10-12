# Milestone 001 — N64 end-to-end vertical slice

**Status:** Planned

## Goal
From a separate client, select an N64 game, boot it on a **real N64**, see and hear its video/audio over a wired local network, and play using a controller without interacting physically with the console during normal game startup.

## Acceptance criteria
- [ ] Verified working N64 runs a known-good, user-supplied game image through a compatible loader.
- [ ] HDMI mod or other tested video path produces stable video/audio.
- [ ] Capture host receives video/audio; a remote wired client plays the stream.
- [ ] Controller input from that client reaches the N64 through a native-protocol bridge.
- [ ] A remote command selects/stages the game and triggers the necessary reset/start sequence.
- [ ] .NET API initiates the sequence and exposes meaningful progress/failure state.
- [ ] Setup and recovery steps are documented; another contributor can reproduce the demo.
- [ ] Measured input-to-display latency, resolution, frame rate and startup time are recorded (no premature targets).

## Workstreams and dependencies
1. **Baseline:** Validate motherboard, PSU, cooling, cartridge and original controller before mods.
2. **Video:** Install/validate digital HDMI solution; confirm capture compatibility; measure latency.
3. **Game loading:** Validate commercial flashcart and determine whether ROM selection can be automated without console-side button presses.
4. **Input:** First validate known-good native controller adapter, then prototype Ethernet-to-native protocol.
5. **Node control:** Reset signaling, status and safe power behavior; use original PSU for v0.
6. **Software:** Minimal .NET Server/Agent, ROM catalog, session state and streaming launcher.
7. **Integration:** End-to-end demo, observability and failure recovery.

## Non-goals
No custom rack, NAS, HDMI matrix, multiple consoles, FPGA cartridge design or simultaneous sessions.

## Risks to resolve early
- USB-equipped flashcart does **not** automatically imply unattended remote ROM loading; validate its protocol.
- Controller ports have platform-specific electrical requirements; do not connect 3.3V GPIO directly without verifying levels and protection.
- HDMI signal lock is not proof the game booted correctly.
- Capture buffering and client decode may dominate latency.
- HDMI modifications may require fine-pitch soldering and board-revision compatibility checks.

## Evidence
Track reproducible tests, firmware versions, hardware revisions, photos, measured results and links to source docs in GitHub Issues or research notes.
