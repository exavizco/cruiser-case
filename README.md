<a href="https://www.exaviz.com">
  <img src="https://raw.githubusercontent.com/exavizco/cruiser-case/main/images/exaviz-logo.svg" alt="Exaviz" height="40">
</a>

# Cruiser Case

**Open CAD design for an enclosure that fits the [Exaviz](https://www.exaviz.com) Cruiser carrier board.**

This repository holds the mechanical design files for a case for the Cruiser
(CM5) carrier board. We're publishing the CAD as the mechanical source of
truth so the community can build on it, refine it, and print it.

<!-- GALLERY: case renders / photos go here once added to images/ -->

## Status: early, not yet print-ready

Full transparency: this is the CAD assembly we designed, but **we never got it
dialed in for 3D printing** (tolerances, wall thickness, supports, port
clearances, screw bosses, etc. have not been validated on a printer). We're
open-sourcing it as-is rather than letting it sit on a hard drive.

**Contributions are very welcome** -- if you adapt it into a clean,
print-ready model (STL / 3MF), tune tolerances, or improve the design, please
open a pull request or an issue. We'd love to fold your work back in and credit
you.

## What's in here

| Path | Description |
|------|-------------|
| `cad/cruiser-case-assembly.step.zip` | The full case assembly in STEP (ISO 10303) format, zipped (~14 MB zipped, ~98 MB uncompressed). The mechanical source of truth. |
| `images/` | Logo and (soon) renders / photos. |

### Using the CAD file

1. Download `cad/cruiser-case-assembly.step.zip` and unzip it.
2. Open the `.step` file in any CAD tool that reads STEP -- FreeCAD (free),
   Fusion 360, SolidWorks, Onshape, etc.
3. STEP is a neutral, widely supported interchange format, so you can import it
   almost anywhere to remix or export a printable mesh.

## Board reference

| Board | Compute | Notes |
|-------|---------|-------|
| **Cruiser** | Raspberry Pi CM5 | PoE carrier board. See [exaviz.com](https://www.exaviz.com) and [exa-pedia.com](https://www.exa-pedia.com) for specs. |

## Contributing

1. Fork the repo and create a branch.
2. Make your changes (CAD edits, print-ready exports, fit notes, photos).
3. Open a pull request describing what you changed and, ideally, how it printed.

Issues for fit problems, dimension questions, or design ideas are equally welcome.

## Links

- **Website:** [www.exaviz.com](https://www.exaviz.com)
- **Documentation:** [www.exa-pedia.com](https://www.exa-pedia.com)
- **Contact:** [info@exaviz.com](mailto:info@exaviz.com)

## License

MIT License with Commons Clause -- see [LICENSE](LICENSE) for details.

Free to use, modify, and share. **Commercial sale is not permitted** under the
Commons Clause -- if you want to use this commercially, please talk to us at
[info@exaviz.com](mailto:info@exaviz.com).

Copyright (c) 2026 Axzez LLC (aka Exaviz)
