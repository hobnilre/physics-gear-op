# Verification record

Date: 2026-09-27. The article predicts measurements and reports none.
Verification here means exact mathematical, editorial, build, and visual
checks; it does not mean physical validation of the selected open questions.

## Exact calculations

All scratch calculations ran inline in the session using exact rational
arithmetic, symbolic differentiation/integration, and algebraic substitution.
No scratch program, simulation, numerical trajectory, quadrature output,
dataset, or notebook is part of the repository. No numerical integrator
or solver was run. Matrix-exponential work expressions are untruncated
closed forms, not computed trajectories.

An integrated final check passed 157 scalar/vector assertions. Additional
symbolic checks covered the five regular/return/overlap circuit balances,
both magnetic polarity decompositions, the dynamic state/store map, the
material-state transient correction, and both wider capacitance controls.
The calculations included:

| Calculation | Independent checks |
|---|---|
| Simple train | Pitch and three-planet phase constraints; positive carrier-disc inertia; rolling; free-body torques; H=13/6 and K=673/72; steady shaft, mesh, and pin works. |
| Transients | Exact affine torque laws; separately integrated shaft works in ground, carrier, and sun observations; field works and independent endpoints; each planet's spin/orbit store and its own three port works. Ring equals ground only on the held-ring control. |
| History and locking | Integration-by-parts shares for both intermediate histories; total 13/6; separate fixed-drive and scaled-drive limits; endpoint state formulas. |
| Lead-outs | Hooke angle composition and exact derivative; complete-period support integral with inertial term; unequal-angle primitive; ratio-two bevel products in both frames; stator conversion values; loaded free-body recomputation and shared axle cancellation. |
| Compound gears | All five pitch-compatible quadruples; exact R and both held-member ratios; torque and power balance in all four observations; physical versus mapped diagnostic difference −241/100. |
| Other geometry | Four Ravigneaux rolling constraints, pitch-centre distances, massless reaction multipliers, ground/carrier works, and ratio 6/5. No stepped-planet formula was substituted for this geometry. |
| Contact and impact | Finite spring/damper input, heat and endpoints; power jump with no state jump; restitution impulse, outgoing velocities, individual side works, kinetic loss 3/16. |
| Full compliant train | Six contact gradients, event at 1/2 s, separate gap/contact integrals, 99/32 J ground input, −7/4 J heat, six 9/64 J spring endpoints, carrier shaft works, field −1/2 J, and both ground/carrier residuals zero. |
| Other mechanical terms | Unequal fractions sum to one and contact works to 7 J; pin couple −1/3 J; reversal signed halves and absolute transfer; radial products and both frame endpoints; full vector field control. |
| Winding circuits | Symbolic KCL/KVL cancellation for isolated/tapped, both physical receiver returns, and two simultaneous receiver branches. Each of the seven powers remains independently defined. |
| Magnetic matrix | Positive determinant in the regular domain; exact common/leakage decomposition for both polarities; each constrained boundary derived before its approach path. |
| Circuit controls | RC bond 5/6 J and optional added receiver; probe branch works and endpoints; 1 V/2 V clamp integrals; perfect-coupling input/store; scaled prepared capacitor and winding stores. |
| Correspondence | State/effort substitutions in the independently stated dynamic equations; capacitor/inertia and magnetic/elastic energy equality; compatible initial states and extra supply ports required. |
| Reference and actuator | Compensated/disabled capacitor law; driver 403/40000 J and heat 3/40000 J; exact actuator ODE, output integral, copper integral, and inductive endpoint; strict negative departure from 2 J; jump-work lower bound. |
| Passive preparation | Actual two-section impedance; both finite values and limits; exact prepared-state ODE solution and individual heat integrals; resistive versus reactive finite releases. |
| Hidden modes | RC decay, both capacitor endpoints and heat; single-mode energy bound 1/20000000000 J; two-mode exact cancellation with 1/1000000 J total store. |
| Common preparation | Three state equations; physical preparation-source products; completed-square energy range; half-period coil works and flux signs at each stated control. |
| Charge sharing | KCL mode decomposition; two separate channel integrals; every equal/unequal capacitance endpoint and orientation scaling; commuting maps with different channel work. |
| Wider ratios | Ratios 1/2000 and 2000, exact stage time ln(2)/2001, independently evaluated final stores 21/1334000 and 10667/21344 J, individual heat integrals and total 5/21344 J. |
| Thermal/material | Thermal ODE and exact exported/retained split; nonlinear ramp source/copper/store integrals; periodic lag state and all three works; transient offset's independent endpoints and corrected period integrals. |
| Sensors/supplies | Sensor source and resistor integrals; plant ODE and unequal-backaction port; controller, bias, finite rail, and combined endpoints; separate source-off recovery law. |
| Cycles | Every prescribed interval's independent work and endpoints; finite passive relaxation retains state; illustrative converter delivery/recovery factors applied separately. |
| Uncertainty | Exact finite effort–flow expansion and capacitor bound; phase/gain/polarity integrals; 100 V endpoint error; torque and actuator budgets including second-order products and remaining allowance. |

The independent port primitive follows by differentiating yyᵀ and using
column vectorization. It remains valid for singular A because φ₁ is an
entire matrix function. The physical-channel quadratic form is specified
before the store comparison. All complete ideal controls have zero residual
by independently obtained works and endpoint states. Model omissions retain
unknown physical magnitude and sign.

## Consistency with the permitted reading material

Shared identical controls agree with the main article or originating
derivation: stator heat difference 7π/50; all compound ratios; complete-port
minus mapped ratio −241/100; finite reference endpoint (9+exp(−10))²/50;
hidden microfarad energy; common-preparation range 95/2 to 115/2.
The simple-train rational example has its own declared inertias and rates,
so other numerical configurations are not treated as matching comparisons.

The source's fixed-radius Coriolis-force wording, finite Hooke endpoint
ripple, contact-side attribution, and zero-locus terminology were checked
against their definitions. The resulting distinctions are recorded in
[coverage-audit.md](coverage-audit.md). Previously successful bounded
mathematical results remain separate from hardware questions and outstanding
computational convergence on other models.

Every abstract, table, figure, and conclusion value is covered by these
checks and agrees with [conventions.md](conventions.md). The five standalone
figures contain only schematics or the exact closed-form curves printed in
the article. They contain no measured or simulated data.

## References

All five bibliography entries are cited beside supporting claims. The
checks used the supplied main manuscript or primary institutional pages:

1. Nilre and Herlin (2026): title, subtitle, author, date and public PDF URL
   checked in the permitted read-only main Markdown. All article references
   use the required [GitHub PDF](https://github.com/hobnilre/physics-gear/blob/main/frames-returns-and-port-power.pdf).
2. Culpepper: the [MIT OpenCourseWare PDF](https://ocw.mit.edu/courses/2-000-how-and-why-machines-work-spring-2002/432880e8fab4781d81ef88470751b397_PlanetaryGearTrains.pdf)
   identifies Martin L. Culpepper, has the stated title and five pages, and
   gives the carrier-relative construction. The 2002 date identifies the
   Spring 2002 course edition; the slides also carry earlier copyright years.
3. MIT: the official [S22 Chapter 31 PDF](https://ocw.mit.edu/courses/8-01sc-classical-mechanics-fall-2016/mit8_01scs22_chapter31.pdf)
   has 34 pages and the referenced Section 31.4 on pp. 7–15. It supports
   the rotating-velocity law, not an unmeasured energy discrepancy.
4. Haus and Melcher (1989): book metadata verified with MIT's published
   edition and [Section 9.7](https://web.mit.edu/6.013_book/www/chapter9/9.7.html).
   The citation supports finite magnetic storage and ideal-transformer limits.
5. JCGM 100:2008: title, year and DOI verified on the official
   [BIPM publication page](https://www.bipm.org/en/doi/10.59161/jcgm100-2008e).
   The DOI resolver itself returned an access error in one tool request;
   the BIPM record independently confirms the DOI. The article cites the
   2008 edition for uncertainty inputs and correlation. Its finite nonlinear
   bounds are derived independently, not attributed to that reference.

## Editorial and repository checks

- Exactly 46 target IDs, each once as plain bracketed introductory text;
  the seven main-manuscript IDs match the mandatory first seven targets.
- All 46 targets have individual scope and closure entries in the coverage
  audit and distinct measurement comparisons in the article.
- Case-insensitive prohibited-word/phrase and source-name scans pass.
  Pandoc's parsed prose contains no source snake_case identifiers; TeX
  mathematical subscripts are mathematical notation, not source identifiers.
- Every equation/figure reference resolves; PDF text contains no `??`.
  No accidental control characters or unescaped `quad` tokens remain.
- All bibliography entries are used, the main article always links to its
  specified public PDF, and article prose contains no read-only local paths.
- No scripts, notebooks, CSV files, or copied project scaffolding occur in
  the deliverables. Build intermediates and review images stay in `build/`.
- The original AGENTS.md is retained. The user's doodles.md was not read,
  edited, or staged. The Git repository is local, with no remote and no commit.

## Build and page review

`make -B pdf` rebuilt all five standalone figures and the article successfully
with Pandoc and XeLaTeX. An independent two-pass XeLaTeX diagnostic of the
same Pandoc source reports no overfull boxes, missing glyphs, unresolved
references, or font substitutions. One benign underfull paragraph warning
remains in the MIT bibliography entry; the visible entry fits its margins.

The article is 32 pages. All pages were rendered to PNG and inspected, and
pages changed by the final textual/font corrections were rendered again for
review. All five figures were individually inspected after changes. The
review checked captions, labels, polarity and force arrows, equation numbers,
table continuations, and text clipping. The PDF metadata has the required
title and author. Distributable article and figure PDFs accompany their sources.
