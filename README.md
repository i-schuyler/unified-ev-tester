# Unified Tester — EV Subsystem Validation Tool
> ⚠️ This repository is under active preparation. Documentation and interfaces may change before the v1.0.0 release.

Unified Tester is a hardware-facing test harness for **incrementally validating and debugging electric vehicle (EV) subsystems**.

It was built to answer a simple but often unmet need in DIY and conversion projects:

> *“How do I safely test one subsystem at a time — chargers, pumps, BMS logic, CAN parsing — before choosing how to integrate them together within a live vehicle?”*

Unified Tester prioritizes clarity, safety, and real-world behavior over abstraction or automation.

---

## What This Is

Unified Tester is:

- A **manual command/control environment** for EV subsystems
- Designed for **bench testing, staged integration, and live debuggging**
- Intended to be used with **real hardware** (CAN devices, pumps, chargers, etc.)
- Modular and extensible, with each subsystem tested independently
- Human-readable and serial-driven by design

The core interface is a serial command menu that exposes all available actions explicitly.

---

## What This Is *Not*

Unified Tester is **not**:

- An autonomous system
- A driving controller
- A real-time safety system
- A drop-in solution for production vehicles

It is a **tool for learning, validation, and confidence-building** — not for operating a vehicle in motion.

---

## Design Philosophy

Unified Tester is built around a few guiding principles:

- **Incremental testing beats heroic debugging**
- **Subsystems should prove themselves in isolation**
- **Human clarity is a safety feature**
- **Hardware reality matters more than elegant abstractions**
- **Manual control reveals edge cases automation hides**

The goal is to reduce the cognitive and physical risk of EV development by making behavior observable and intentional.

---

## Typical Use Cases

Unified Tester is useful when you want to:

- Validate CAN parsing against real devices
- Manually command a charger or DC/DC converter
- Exercise coolant or power steering pumps safely
- Test ramping, limits, and fault behavior
- Confirm assumptions before integrating into a vehicle control stack
- Learn how subsystems *actually* behave under real conditions

---

## Command Interface

All interaction happens through a serial console.

The menu:
- Lists all available commands
- Groups commands by subsystem
- Reflects the actual capabilities compiled into the firmware
- Is intended to be truthful and exhaustive

For a full list of commands and behaviors, see:
docs/command_reference.md

---

## Safety Notes

Working with EV hardware involves real electrical, thermal, and mechanical risk.

You are responsible for:
- Proper isolation
- Appropriate fusing
- Safe power levels
- Understanding your hardware’s specifications

Unified Tester does **not** enforce safety interlocks beyond what is explicitly implemented.

This project is provided as a testing and exploration tool.
It is not intended for use in an active driving system.

See:
docs/safety.md

---

## Hardware & Platform

Unified Tester is typically used with:
- Microcontrollers capable of CAN (e.g. ESP32-based platforms)
- Real EV subsystems (chargers, BMS, pumps, etc.)
- Bench or staged vehicle environments

Hardware details and assumptions are documented here:
docs/hardware.md

---

## Project Status

This project is actively used in real EV development and may evolve as understanding deepens.

Stability is prioritized over rapid feature growth.

---

## Contributing

Contributions are welcome when they align with the project’s goals and philosophy.

- Bug reports are appreciated
- Pull requests should be focused and well-scoped
- Feature requests may be considered, but are not guaranteed

Please keep in mind that this project values **clarity and restraint** over expansion.

---

## License

This project is released under the MIT License.

You are free to use, modify, and distribute it, with attribution.

---

## Contact

If you are working on a complex or safety-critical EV project and want a second set of eyes, you can reach me via GitHub.

No guarantees of support are implied — this project is shared in the spirit of usefulness and care.

---

## Closing Note

Unified Tester exists because many EV projects fail or stall not from lack of intelligence, but from lack of safe, incremental validation.

If this tool helps you slow down, see clearly, and build with confidence, then it has done its job.
