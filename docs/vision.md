# Vision

Console Cabinet is an open-source platform for playing a personally maintained game library on **original console hardware**, remotely managed over a local network.

## What makes it different
- The console's original CPU/GPU executes the game; Console Cabinet is not a console emulator.
- Games are selected from a software interface and made available to physical console nodes through platform-specific loading mechanisms.
- Native video is captured and streamed to a client, while controller input travels back to the real console.
- The same orchestration concepts should extend to N64, PS1, PS2, original Xbox, and later platforms.

## Design principles
1. **Authentic execution:** No software emulation of the game console.
2. **Vertical slices:** Prove a complete playable path before investing in rack fabrication or custom PCBs.
3. **Observable and recoverable:** Physical state is not assumed from successful API calls; verify it.
4. **Open interfaces:** Document protocols and hardware integration points so others can contribute.
5. **Offline-capable:** Exhibition deployments must not require Internet connectivity.
6. **Portability as a goal, not a constraint on the first prototype:** Eventually package the system in a portable molded road rack.

## Out of scope for the first milestone
Multi-console scheduling, multi-user simultaneous streaming, custom rack enclosure, NAS procurement, custom FPGA cartridge, and a polished game-library frontend.

## Legal and licensing boundary
Users are responsible for obtaining and using game images lawfully. The project does not distribute copyrighted game images, BIOS dumps, keys, or proprietary console firmware. MIT applies to repository-authored software and documentation unless a file says otherwise; third-party hardware, firmware and design assets retain their own licenses. Choose a hardware-design license before publishing original PCB design files.
