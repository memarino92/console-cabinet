# Console Cabinet

**Original console hardware. Networked game library. Software-defined control.**

Console Cabinet is an open-source experiment in running games on **real retro console motherboards** while remotely orchestrating game loading, controller input, power/reset, and low-latency video streaming over a local network.

The first goal is a complete **Nintendo 64 vertical slice**, not a finished rack or multi-console platform. The long-term ambition is a portable, offline-capable rack appliance suitable for meetups and conferences.

## How it works (proposed)

```text
Game library -> .NET session orchestration -> hardware agent -> real N64
                                                           |         ^
                                                   HDMI capture  controller bridge
                                                           |
                                                  LAN stream -> client
```

The console itself executes the game. Console Cabinet does **not** emulate its CPU/GPU.

## Project status

**Planning / research.** No validated hardware stack or working end-to-end prototype is claimed. Candidate devices and physical packaging are documented as proposals, not purchases or accepted decisions.

## Start here
- [Vision and principles](docs/vision.md)
- [Architecture proposal](docs/architecture/overview.md)
- [N64 milestone and acceptance criteria](docs/milestones/001-n64-vertical-slice.md)
- [Candidate hardware bill of materials](docs/hardware/bill-of-materials.md)
- [Architecture decision records](docs/architecture/decisions/README.md)
- [Contributing](CONTRIBUTING.md)

## Roadmap
1. Validate real N64, ROM loader and HDMI capture.
2. Stream playable video/audio over wired Ethernet.
3. Bridge remote controller input into the native N64 port.
4. Orchestrate game selection and reset from a .NET API.
5. Package a robust, offline-capable demo; then investigate additional consoles.

## Licensing

Repository-authored software and documentation are released under [MIT](LICENSE). Third-party dependencies and designs keep their own licenses. Hardware design licensing will be selected before original PCB design files are published. No copyrighted game images, BIOS files or console keys are distributed.
