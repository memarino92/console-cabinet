# Contributing

Console Cabinet is an early-stage open-source hardware/software project. Research, measured experiments, reproducible bug reports, architecture feedback, firmware, and code are welcome.

## Working agreements
- Open an issue for significant new work; link evidence and primary documentation where possible.
- Propose substantial architectural changes with an ADR in `docs/architecture/decisions/`.
- Distinguish tested behavior from assumptions and vendor claims.
- Keep platform-specific details behind clearly described interfaces.
- Never commit copyrighted ROMs, BIOS images, console keys, private credentials, or proprietary firmware.
- Respect licenses of referenced open-source projects and hardware designs.
- Prefer small, reviewable changes with reproducible tests and conventional commit messages.

## Safety
Console modifications may damage equipment or cause injury. Disconnect power before working on boards. Validate voltages and pinouts before applying power. Do not expose mains conductors or bypass protective grounding.

## Getting started
Read [the vision](docs/vision.md), [architecture proposal](docs/architecture/overview.md), and [first milestone](docs/milestones/001-n64-vertical-slice.md). Code/toolchain instructions will be added as implementation begins.
