# Finite Transfers and Open Energy Balances

Physical tests of loaded gears, switched returns, and prepared states

A self-contained companion to
[*Frames, Returns, and Port Power*](https://github.com/hobnilre/physics-gear).

## What this article adds, and why it matters

The fourth central shaft gives a concrete first experiment: attach a receiver
to the planet output, maintain the declared motion, and measure the changed
shaft works and reactions. The companion follows that apparatus into its
physical joints, supports and instruments, then develops equally specific
questions about switched electrical returns and prepared cell states.

- **One receiver changes carrier work by $7/3$ J in the ideal control.** The
  article derives the local free bodies and an independent uncertainty budget.
  A dimensioned Oldham coupling resolves a separate spatial-force model;
  actual universal-joint forces still require their own identification.
- **A switched tap is a physical connection.** The isolated-primary circuit
  retains both secondary sections, both RC branches, finite switch edges,
  gate supplies, clamps and thermal states. Clocked attraction, hybrid
  operation, matched useful service and generator shaft work have distinct
  conditions.
- **The same terminal can conceal different energy.** Series cells prepared
  at $(1,1)$ and $(3,-1)$ V give the same terminal history while retaining
  1 and 5 J. A finite loaded-probe protocol defines binary identification;
  a paired-work protocol retains preparation costs and actual final stores.
- **Signs and work have separate proofs.** An LC exchange increases absolute
  charge from 10 to 28 C at unchanged total reactive energy. A finite shunt
  example proves every sign event throughout its window. Three-store reset
  order changes both individual heat deliveries and final state.
- **Measurements need independent uncertainty.** Torque, angle, voltage,
  current, material, thermal and supply observations have separate roles.
  The article distinguishes an exact control, acquisition of an unknown
  physical law, a calibrated comparison and a complete energy residual.

The article retains 51 selected questions and bounded outcomes, with each
identifier beside its local model. All results are exact or explicitly
conditional. No apparatus measurements are reported, and broader physical
questions remain distinct from resolved model examples.

## Article and build

[Read the article (PDF)](finite-transfers-and-open-energy-balances.pdf) · [Manuscript source](finite-transfers-and-open-energy-balances.md)

Install GNU Make, Pandoc, XeLaTeX and the TeX Gyre fonts, including the LaTeX
packages used by `preamble.tex` and the standalone TikZ/PGFPlots figures. Run `make pdf`
from this repository. The build uses only files in this checkout; no sibling
repository or private working files are needed.

The first page gives the PDF creation time in UTC, followed by this repository's
GitHub link. An up-to-date PDF keeps its timestamp; `make -B pdf` forces a rebuild.
Intermediates go to ignored `build/` by default; `BUILD_DIR=/absolute/path`
selects another location. `make clean` removes that build directory and keeps
the published PDF and figure assets.
