# Finite Transfers and Open Energy Balances

Exact controls and decisive measurements for gears, windings, and their supplies.

Hob Nilre & Bo C. Herlin · 27 September 2026

[Read the article](finite-transfers-and-open-energy-balances.pdf) ·
[Markdown source](finite-transfers-and-open-energy-balances.md)

A self-contained companion to
[*Frames, Returns, and Port Power*](https://github.com/hobnilre/physics-gear/blob/main/frames-returns-and-port-power.pdf).
The article develops exact finite comparisons for the 46 selected questions.
It predicts measurements; it contains no apparatus data or numerical trajectories.
Physical closure of the open questions remains conditional on the specified measurements.

Build with `make pdf`. Requirements: GNU Make, Pandoc, XeLaTeX, the TeX Gyre
fonts, and the LaTeX packages used in `preamble.tex` and `figures/figure-style.tex`.
`make -B pdf` rebuilds all figures and the article. `make clean` removes only
ignored build output and keeps the distributable PDFs.

Notation and fixed values are in [notes/conventions.md](notes/conventions.md).
The separate [coverage audit](notes/coverage-audit.md) preserves each question's
scope and closure conditions. [Verification notes](notes/verification.md) record
the algebra, reference, build, and visual checks.

This is a local Git repository with no remote. No commit is made by the build.
