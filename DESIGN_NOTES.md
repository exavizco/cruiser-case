# Design Notes & Known Issues

This file documents the current state of the Cruiser case design, the known
problems with it, and good starting points for anyone who wants to improve it.
We're putting this on the record so you don't have to rediscover everything
the hard way.

## Context

This case was designed around the [Exaviz Cruiser](https://www.exaviz.com)
(CM5) carrier board. The prototype was produced in **metal (CNC/sheet)** and
the finish quality was genuinely excellent - it feels solid and looks great in
hand. But the design was never finished or validated to the point where we were
comfortable shipping it, and it was **never adapted for 3D printing**. The CAD
in this repo (`cad/cruiser-case-assembly.step.zip`) is that prototype design,
as-is.

If you're adapting this for FDM/resin printing, expect to rework wall
thickness, tolerances, bosses, and supports from the ground up - the geometry
was authored with machined metal in mind, not additive manufacturing.

## What's good (worth keeping)

- **Form factor is space-efficient.** Very little wasted internal volume.
- **Two-piece top-shell + bottom-plate layout** is clean and makes assembly
  easy and inexpensive.
- **Front aesthetic** (logo + hex vent + power button) looks sharp.
- **Internal layout** for the board and the two HDD bays is sensible.

## Known issues (where to start)

These are the concrete problems we found in the prototype. Most are good
first contributions:

1. **Recessed ports.** The rear I/O and the front USB3 port sit too deep in
   the case. Some plugs may not seat properly. Port cutouts/depth need to be
   pulled forward to match real connector geometry.
2. **PCB mounting not rigid.** The board isn't held tightly. Standoff/screw
   lengths need to match the board, and the mount could use proper bosses
   (see "Improvement ideas" below).
3. **Power button.** The prototype used an oversized button that fouls the HDD
   (the drive has to be removed to close the case) and lacks the right
   connector. Target spec: a small momentary button, **3.3 V, < 1 mA load**,
   with a plug that mates to the board header (not soldered/hand-wired).
4. **HDD tray support.** The trays should rest on rubber gaskets/grommets for
   vibration isolation. The prototype added extra metal posts under the trays
   instead, defeating the isolation. Plan for proper grommets and tray
   supports.
5. **Fan connectors.** The fan connector on the prototype did not match the
   board's fan header. Verify against the current Cruiser fan header.
6. **Stray USB3 mounting plate.** There's an extra plate under the front USB3
   mount that serves no purpose - can be removed.
7. **Lid/underside fasteners.** The screws holding the lid on need a cleaner,
   more finished solution.
8. **Overall weight/thickness.** The metal version is thicker and heavier than
   it needs to be (see wall-thickness note below).
9. **Antenna placement blocks 2.5GbE LEDs.** With the antenna where it is, you
   can't see the 2.5GbE link LEDs. Moving the antenna to the fan side resolves
   this (would require a longer antenna lead).

## Improvement ideas

Engineering suggestions gathered while evaluating the design:

- **Reduce wall thickness.** The outer housing wall is ~**5.2 mm**; it can come
  down to roughly **2 - 2.5 mm** for lighter weight and better
  manufacturability (especially relevant if molding or printing in plastic).
- **Add corner bosses.** Add bosses at the four corners to hold the PCB firmly
  without vibration/movement.
- **Add screw locations in safe clearance areas.** A few additional, carefully
  placed screw holes increase rigidity without risking the board.
- **HDD shelves and fan mounts.** Bent sheet metal (steel or aluminum) works
  well here, or plastic - keep it simple.
- **Fasteners.** Use appropriate metric screw sizes throughout.

## Notes for contributors

- The STEP file is the mechanical **source of truth**. Import it into FreeCAD,
  Fusion 360, SolidWorks, Onshape, etc. to remix.
- The design is **not tied to metal** - plastic (printed or molded) is totally
  fine, and you're free to change the design as needed. Making it look and
  function well is what matters; you do not have to preserve the current
  geometry.
- High-value first contributions: a clean print-ready export (STL/3MF), fixed
  port depths, proper PCB bosses, and a sane power-button mount.

If you build or print one, we'd love to see it - open an issue or a PR.
