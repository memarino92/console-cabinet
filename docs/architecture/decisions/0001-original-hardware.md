# ADR 0001: Original hardware executes games

- Status: Accepted
- Date: 2026-10-11

## Context
Most retro frontends run game images through software emulators. Console Cabinet aims to remotely operate physical consoles and make their video and input accessible over a network.

## Decision
The console's original CPU/GPU will execute the game. Software may stage game images, coordinate physical devices, translate controllers, encode video, and manage sessions, but it will not replace the console's game-execution hardware with an emulator.

## Consequences
- Requires platform-specific game loading and physical controller/video integration.
- Hardware availability, failures and latency are first-class concerns.
- The control plane can be console-agnostic, while adapters remain console-specific.
- A software emulator can be useful for development/testing mocks but is not a production game-execution backend for the project's core promise.
