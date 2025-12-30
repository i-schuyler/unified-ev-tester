# Contributing

Thanks for your interest in contributing to Unified Tester.

This project is a hardware-facing test harness for incremental EV subsystem validation.  
It prioritizes clarity, restraint, and real-world behavior over rapid feature growth.

---

## What We Welcome

- **Bug reports** (especially reproducible ones)
- **Documentation improvements**
- **Small, well-scoped pull requests**
- **Hardware notes** that improve safety or clarity
- **Command/menu alignment fixes** (truthful and exhaustive menus matter here)

---

## What We Avoid

- Adding lots of new subsystems without a clear need
- Turning the project into a generalized framework
- “Magic” automation that reduces clarity or observability
- Breaking changes to the command interface without strong reason

---

## Before You Open a PR

Please include:

1. **What changed** (1–3 sentences)
2. **Why it changed** (the problem it solves)
3. **How it was tested**
   - Hardware used (if relevant)
   - Any test conditions or constraints

If your change touches safety-critical behavior (charging, pumps, high voltage assumptions), please add or update documentation in `docs/`.

---

## Style Guidelines

- Prefer explicit, descriptive names over clever ones
- Keep commands consistent with the taxonomy in the docs
- Make serial output human-readable and predictable
- Add comments only when they clarify intent or constraints

---

## Boundaries

This project is shared in the spirit of usefulness and care.  
Maintainer time is limited, and not every feature request will be accepted.

Thanks for keeping contributions focused and aligned.
