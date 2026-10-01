# Finite Transfers and Open Energy Balances

Physical tests of loaded gears, switched returns, and prepared states

A self-contained companion to
[*Frames, Returns, and Port Power*](https://github.com/hobnilre/physics-gear).

## Main argument and technical appendices

The short main text follows three measurement decisions: what a planet
receiver changes, what an attached electrical branch changes, and what
terminal observations identify about prepared energy. It derives the first
comparisons and their independent work and endpoint uncertainty requirements.

Seven appendices retain the complete mechanical, winding, switching,
prepared-state, material and shared-output models. The supplied-machine
specification, component bounds and detailed measurement comparisons remain
in this same article and PDF. Simpler prepared-state observations precede
the shared-output fixture.

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
  1 and 5 J. The finite graph has an exact precommutation difference bound
  below $1/1000$ V; later binary discrimination remains conditional on a
  separate loaded-probe separation. Paired receiver-work ordering remains
  unevaluated, with preparation costs and actual final stores retained.
- **Signs and work have separate proofs.** An LC exchange increases absolute
  charge from 10 to 28 C at unchanged total reactive energy. A finite shunt
  example proves every sign event throughout its window. Three-store reset
  order changes both individual heat deliveries and final state.
- **Measurements need independent uncertainty.** Torque, angle, voltage,
  current, material, thermal and supply observations have separate roles.
  The article distinguishes an exact control, acquisition of an unknown
  physical law, a calibrated comparison and a complete energy residual.
- **Finite return, repeated operation and energy identification differ.** A
  six-channel shared-output graph has a certified prepared 5 ms transition.
  An insulated timing-drive model cannot return its full thermal state;
  one loaded electrical-port observation set has a best possible worst-case
  initial-energy error of $1/100$ J on its two known preparations. Electrical,
  shaft and thermal observations test the remaining physical questions.

The measurement route starts with one loaded planet output, one finite
return/probe change and two known cell preparations before the shared-output
assembly. A 10 s probe response over a 5 ms window is explicit in the latter
observation obstruction. The complete supplied-machine model is retained in
an appendix beside its return-map qualifications.

The article retains 54 selected questions and bounded outcomes, with each
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

The title date records the first version. Keep `ARTICLE_DATE` in the Makefile
and the manuscript's `date` fixed across revisions. The separate `PDF created`
timestamp continues to record each PDF rebuild in UTC.
