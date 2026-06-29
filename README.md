<a href="https://www.exaviz.com">
  <img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/exaviz-logo.svg" alt="Exaviz" height="40">
</a>

# Cruiser Case

**Open CAD design for an enclosure that fits the [Exaviz](https://www.exaviz.com) Cruiser carrier board.**

This repository holds the mechanical design files for a case for the Cruiser
(CM5) carrier board. We're publishing the CAD as the mechanical source of
truth so the community can build on it, refine it, and print it.

<img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/case-front.png" alt="Cruiser case - front view" width="640">

## Status: early, not yet print-ready

Full transparency: this is the case assembly we designed (and had built as a
metal prototype - the finish was genuinely beautiful), but we **never adapted
it for 3D printing** and never finished validating it. Tolerances, port depths,
wall thickness, and mounting all need work before it's ready to print.

Rather than let it sit on a hard drive, we've open-sourced it as-is. See
**[DESIGN_NOTES.md](DESIGN_NOTES.md)** for the full list of known issues, what's
good about the design, and concrete starting points.

**Contributions are very welcome** - if you adapt it into a clean,
print-ready model (STL / 3MF), tune tolerances, or improve the design, please
open a pull request or an issue. We'd love to fold your work back in and credit
you.

## Gallery

| | |
|---|---|
| <img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/case-rear.png" alt="Rear I/O" width="380"> | <img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/case-rear-angle.png" alt="Rear angle" width="380"> |
| Rear I/O: 2x HDMI, 4x USB, RJ45, 8x PoE | Rear three-quarter with side venting |
| <img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/case-internal-top.png" alt="Internal top view" width="380"> | <img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/case-internal-front.png" alt="Internal front view" width="380"> |
| Top view (transparent): board + dual HDD bays | Front three-quarter (transparent): fans + board |

## What's in here

| Path | Description |
|------|-------------|
| `cad/cruiser-case-assembly.step.zip` | The full case assembly in STEP (ISO 10303) format, zipped (~14 MB zipped, ~98 MB uncompressed). The mechanical source of truth. |
| `cad/cruiser-case.FCStd` | Native FreeCAD document with the same geometry. Open it directly in FreeCAD (no unzip needed). |
| `DESIGN_NOTES.md` | Known issues, what works, and where to start. |
| `images/` | Renders of the design. |

### Using the CAD file

- **FreeCAD users:** open `cad/cruiser-case.FCStd` directly (no unzip needed).
- **Everyone else:** download `cad/cruiser-case-assembly.step.zip`, unzip it, and
  open the `.step` file in any CAD tool that reads STEP (Fusion 360, SolidWorks,
  Onshape, etc.). STEP is a neutral, widely supported interchange format, so you
  can import it almost anywhere to remix or export a printable mesh.

## Board reference

| Board | Compute | Notes |
|-------|---------|-------|
| **Cruiser** | Raspberry Pi CM5 | PoE carrier board. See [exaviz.com](https://www.exaviz.com) and [exa-pedia.com](https://www.exa-pedia.com) for specs. |

## Contributing

1. Fork the repo and create a branch.
2. Make your changes (CAD edits, print-ready exports, fit notes, photos).
3. Open a pull request describing what you changed and, ideally, how it printed.

Issues for fit problems, dimension questions, or design ideas are equally welcome.
Start with **[DESIGN_NOTES.md](DESIGN_NOTES.md)**.

## Links

- **Website:** [www.exaviz.com](https://www.exaviz.com)
- **Documentation:** [www.exa-pedia.com](https://www.exa-pedia.com)
- **Contact:** [info@exaviz.com](mailto:info@exaviz.com)

## License

MIT License with Commons Clause - see [LICENSE](LICENSE) for details.

Free to use, modify, and share. **Commercial sale is not permitted** under the
Commons Clause - if you want to use this commercially, please talk to us at
[info@exaviz.com](mailto:info@exaviz.com).

Copyright (c) 2026 Axzez LLC (aka Exaviz)
