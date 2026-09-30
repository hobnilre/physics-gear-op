---
title: "Finite Transfers and Open Energy Balances"
subtitle: "Physical tests of loaded gears, switched returns, and prepared states"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-09-30"
abstract: |
  Three questions organize the physical tests of a four-shaft gear and
  related circuits: what an attached load changes, what a changed return
  changes, and what observations identify about prepared energy. Attached
  free bodies predict a 7/3 joule carrier-work difference for one planet
  receiver; actual joint and support laws require identification. A separate
  Oldham model resolves its own spatial forces. Finite winding, switch, cell,
  gate and thermal states define the electrical comparisons. Two series
  preparations conceal 1 or 5 joules behind the same terminal history;
  finite reconnection has a proved precommutation bound and a conditional
  discrimination criterion. Receiver-work ordering remains unevaluated.
  A six-channel shared output admits a prepared 5 millisecond return witness.
  Insulation obstructs full-state repetition, while specified loaded probes
  impose an exact 1/100 joule worst-case energy error on two known states.
  Independent uncertainties and staged measurement decisions delimit these
  results. All predictions are exact or explicitly conditional within
  declared models; no apparatus measurements are reported.
keywords:
  - signed work
  - epicyclic gearing
  - transformer returns
  - prepared energy
  - switching paths
  - measurement uncertainty
documentclass: article
classoption:
  - 11pt
geometry:
  - margin=1.1in
mainfont: "TeX Gyre Termes"
sansfont: "TeX Gyre Heros"
monofont: "TeX Gyre Cursor"
mathfont: "TeX Gyre Termes Math"
numbersections: true
secnumdepth: 3
indent: true
linestretch: 1.05
colorlinks: true
linkcolor: MidnightBlue
urlcolor: MidnightBlue
citecolor: MidnightBlue
---

\begingroup\scriptsize\noindent PDF created: \pdfbuildtimestamp\par\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-gear-op}\par\endgroup

# One apparatus, then its physical tests

A planet rolls between a sun and ring while its centre travels with the
carrier. In the specified ideal layout, two correctly phased universal
joints connect its rotating stub to a separately supported central shaft.
The four accessible shafts are sun, carrier, ring and planet output. When a
receiver loads that fourth shaft, which reactions and work readings change,
and how can their complete physical balance be measured?

[*Frames, Returns, and Port Power* (Nilre and Herlin, 2026)][main]
constructs the ideal four-shaft mechanism and two electrical realizations
of its terminal relations. Here the same construction supplies the first
experiment. A held-ring control predicts a $7/3\,\mathrm J$ change in
carrier work when one output receives $7/3\,\mathrm J$ in one second.
Actual joint forces, moving supports, bearing losses and preparation
must be identified independently. A separate Oldham model makes that
distinction tangible: its known slot forces cannot determine a Cardan
cross's reactions.

The electrical investigation likewise begins with connections that can be
drawn and measured. A switched full-to-tap return is a different circuit
from a change of voltage zero. A series-to-parallel bank change can reveal
energy that its earlier terminal history concealed. Following these
operations requires individual cells, finite winding states, switch and
probe loading, gate supplies and actual reset endpoints.

A shared magnetic receiver adds another connected problem. Six isolated
input cores feed twelve branch windings on one output core. A prepared
finite transition can return work to its sources while supplying a receiver;
full-state repetition and the accuracy of inferred initial energy require
different proofs. The declared model below establishes a finite witness,
an insulated-cycle obstruction and a bounded observation-error obstruction.

The three questions are therefore load response, connection response and
identification of prepared energy. The signed-cell examples precede the
larger shared-output fixture; its complete supplied-machine specification
is in Appendix \ref{sec:machine-specification}. Section
\ref{sec:measurement-route} gives the sequence of measurement decisions.
Exact controls establish their own predictions; unknown
constitutive laws require acquisition; a physical energy remainder requires
simultaneous measurements of all included ports and endpoints. None of
these tasks can supply the missing data for another.

The contribution is a sequence of exact comparisons with explicit physical
identification requirements: loaded shaft works, persistent circuit states
through reconnection, and finite-error energy inference. Each has its own
model and observable. The larger fixtures supply bounded supporting results;
their component count does not extend the scope of the simpler proofs.

# Boundaries, signs, and exact integration

Power is positive into the named system. Mechanical products are
$\mathbf F\cdot\mathbf v+\mathbf M\cdot\symbf{\omega}$ at the
force application point and body; electrical products are complete
voltage differences times oriented current. Thermal export is
$-T_b\dot S_{\rm out}$ at boundary temperature $T_b$; internal entropy
production is not a second boundary heat port. On each explicit interval,
\begin{equation}
 W_j(t_0,t_1)=\int_{t_0}^{t_1}e_jf_j\,dt,\qquad
 r_E=E(t_1)-E(t_0)-\sum_jW_j.
 \label{eq:ledger}
\end{equation}
For vector ports use the corresponding scalar product. Opposite sides of an
internal interface are integrated separately and cancel only when their
actual motions and efforts agree. An impulse represented by a declared
jump law replaces a resolved finite edge; it is never added to that edge
a second time. Both endpoints are constitutive evaluations, not residuals.

![Schematic boundary hierarchy. Shared mechanical or electrical interfaces cancel only for the same realized path. Plant and controller conversion rates are $D$ and $D_c$. Controller and thermal stores remain inside the combined apparatus; external supply, receiver, and ambient transfers remain measurable.](figures/boundaries.pdf){#fig:boundaries width=95%}

\FloatBarrier

Figure \ref{fig:boundaries} shows why enlarging a boundary changes the list of
external transfers. All dimensional coefficients below are illustrative. In displayed worked
paths, $t$ denotes the numerical time in seconds and every coefficient has
the SI units needed for the stated quantity. Unless another interval is
specified, each worked path uses $[0,1]$ s. Equations using symbolic $T$
retain its time units. Configuration I is the simple train; II the linkage;
III the compound geometries; IV the regular winding pair; V the prepared
passive and switched circuits; VI the material and supply controls.

For later linear circuits a useful closed form integrates each port without
solving for a missing work. Augment a constant, polynomial, or sinusoidal
source by its exact differential equations, so that $\dot y=Ay$. For
$P_j=y^TQ_jy$, with $Q_j$ symmetric, define
\begin{equation}
 \mathcal I(Q_j,A,y_0,T)=\operatorname{vec}(Q_j)^T
 T\varphi_1\!\left(T(A\otimes I+I\otimes A)\right)
 \operatorname{vec}(y_0y_0^T),\quad
 \varphi_1(Z)=\sum_{n=0}^{\infty}\frac{Z^n}{(n+1)!}.
 \label{eq:integrator}
\end{equation}
Here $y(T)=e^{AT}y_0$ and $Q_j=(e_jf_j^T+f_je_j^T)/2$ when the two
linear channel vectors are $e_j,f_j$. This entire matrix function is a closed
form, including singular $A$; no series is truncated.

\begin{lemma}[Independent port primitive]
Equation \eqref{eq:integrator} equals the signed integral of that port.
\end{lemma}
\noindent\textit{Proof.}
For $Y=yy^T$, $\dot Y=AY+YA^T$. Column vectorization gives
$\operatorname{vec}Y(t)=e^{t(A\otimes I+I\otimes A)}\operatorname{vec}Y(0)$.
Integrating its convergent exponential series and contracting with $Q_j$
gives the result without using any store. $\square$

For symbolically evaluated work accounts the numerical integration residual
is exactly zero. An exact identity or bound can also be proved without
evaluating every finite work. Where only a fundamental-matrix representation
or a sufficient condition is given, its unevaluated value or hypothesis is
stated explicitly. Physical model error and measurement residuals are
unmeasured. Independently computing works and stores under shared constitutive
assumptions checks those equations; it does not identify their physical scope.

| Treatment | Established information | Information still required |
|-------------------------------|----------------------------------------|------------------------------------------|
| Evaluated exact control | Separate signed works and constitutive endpoints | Applicability of its physical laws |
| Identity or continuous bound | A result for every admitted model history | Individual works when not separately evaluated |
| Conditional finite comparison | Defined graph, history map and decision inequalities | Proof of any unevaluated inequality or work ordering |
| Physical acquisition | A measurable quantity and uncertainty target | Identified laws, calibrated records and actual endpoints |

: Status of the predictions. A missing evaluation or measurement is not a zero residual.

# Gears: free bodies, stores, and physical lead-outs

## The fourth shaft and its first measurable comparison
\label{sec:four-shaft-test}

The planet body carries a rotating stub inside a carrier-mounted bearing.
Two universal joints connect that stub to a separately supported central
shaft $o$, beside the sun, carrier and ring shafts. The parallel-offset
geometry has equal joint angles, with phasing fixed in the carrier's rotating
joint plane. The intermediate shaft fixes that relative phase; equal angles and correct
phasing are the ordinary double-joint conditions [Belden][joints]. With continuous
joint lift $H_\beta(x)$ satisfying
$\tan H_\beta(x)=\tan x/\cos\beta$, the map
$\theta_o=\phi+H_\beta(H_\beta(\theta_p-\phi)+\pi/2)-\pi/2$
reduces to $\theta_o=\theta_p$. The later phase and support controls change
specified parts of this model.

![The recurring four-shaft apparatus. The output is connected to the rotating planet stub, not its carrier-fixed support pin. The yokes are phased relative to the rotating joint plane. Dimensions describe centreline geometry; complete joint forces, packaging and physical clearances require independent identification.](figures/four-shafts.pdf){#fig:four-shafts width=100%}

\FloatBarrier

For teeth $(24,18,60)$, module $1/500\,\mathrm m$, offset
$21/500\,\mathrm m$ and joint-centre axial separation $3/25\,\mathrm m$,
the two mesh equations give
\begin{equation}
 (\omega_s,\omega_c,\omega_r,\omega_o)
 =(u+d,u,u-2d/5,u-4d/3).
 \label{eq:four-observed-rates}
\end{equation}
All torques below enter the assembly. For a single steady loaded planet,
the sun force is $F_s=\tau_s/r_s$, planet spin balance gives
$F_r=F_s-\tau_o/r_p$, and the tangential pin force is $-F_s-F_r$.
The ring and carrier moment arms then give
\begin{equation}
 \tau_r=\frac52\tau_s-\frac{10}{3}\tau_o,\qquad
 \tau_c=-\frac72\tau_s+\frac73\tau_o.
 \label{eq:four-observed-loads}
\end{equation}
These load reactions were obtained before evaluating power.
Hold the ring, maintain $(\omega_s,\omega_c)=(7/2,1)\,\mathrm{rad/s}$
and compare the unloaded planet with $\tau_o=1\,\mathrm{N\,m}$,
at measured $\tau_s=2\,\mathrm{N\,m}$.

Four effective unit inertias give $673/72\,\mathrm J$ at each endpoint,
with orbit counted once in the carrier coefficient. The four separate work
integrals sum to zero. This initialized steady interval has no impulse and
does not assign a preparation work. The later $7\,\mathrm J$ comparison
uses three receivers or total output torque $3\,\mathrm{N\,m}$; it is a
different load. Equal planet speeds do not determine force sharing. Under
equal bilateral contact stiffness, loads $(3,0,0)$ and $(1,1,1)\,\mathrm{N\,m}$
have the same aggregate reactions but sun-force vectors
$(250/3,0,0)$ and $(250/9,250/9,250/9)\,\mathrm N$. Individual
contacts and pin couples need observations when they enter the boundary.

| One-second observation | Unloaded output | Loaded output |
|--------------------------------|---------------------:|------------------:|
| Output rate, rad/s | $-7/3$ | $-7/3$ |
| Carrier torque, N m | $-7$ | $-14/3$ |
| Ring holding torque, N m | $5$ | $5/3$ |
| Sun work into assembly, J | $7$ | $7$ |
| Carrier work into assembly, J | $-7$ | $-14/3$ |
| Ring work into assembly, J | $0$ | $0$ |
| Output work into assembly, J | $0$ | $-7/3$ |

: The same established motion and sun effort with one attached receiver. Independent control authority and actual effort measurements are requirements of this comparison.

The first comparison uses synchronized shaft torque and unwrapped angle;
the held-ring transducer checks its reaction although its work is zero.
As an illustrative calibration requirement for the two carrier observations,
take $|\widehat\tau|\leq8\,\mathrm{N\,m}$,
$|\widehat\omega|\leq101/100\,\mathrm{rad/s}$,
$u_\tau\leq1/200\,\mathrm{N\,m}$ and
$u_\omega\leq1/1000\,\mathrm{rad/s}$. The product bound derived below gives
$2611/100000\,\mathrm J$ for their difference.
A total $1/10\,\mathrm J$ difference budget leaves
$7389/100000\,\mathrm J$ for independently bounded timing, setting and
other observation errors. This resolves the predicted $7/3\,\mathrm J$
change if those requirements are met. A complete residual also needs every
support, drive, thermal and endpoint contribution.

## A dimensioned support model with a different coupling
\label{sec:oldham-spatial}

The U-joint angle map leaves its spatial forces undetermined. A mirrored
Oldham pair supplies a separate determinate parallel-axis control. Take
offset $a=21/500\,\mathrm m$, combined middle mass $m=1/5\,\mathrm{kg}$,
middle inertia $I_m=1/500$ and output inertia
$I_o=1/250\,\mathrm{kg\,m^2}$. Orthogonal slots have half-stroke
$3/50\,\mathrm m$, pad arm $b=1/50\,\mathrm m$,
bearing separation $\ell=3/100\,\mathrm m$ and overhang
$h=1/100\,\mathrm m$. Mirroring puts net pad forces in one plane;
locating bearings hold axes parallel. Angular misalignment and axial force
are excluded. Bilateral preload is declared as $100\,\mathrm N$;
contact strength, preload compliance and friction require material data.
The declared domain is $|\omega_c|\leq1$ and $|\omega_p|\leq7/3$ rad/s;
fixed output bearings do zero ideal work.

Put $u=(\cos\theta,\sin\theta)$, $v=(-\sin\theta,\cos\theta)$,
$P=a(\cos\phi,\sin\phi)$ and middle centre $M=(P\cdot v)v$,
where $\theta$ is planet orientation and $\delta=\phi-\theta$.
For constant shaft rates, differentiation and the translational and angular
free bodies give
\begin{align}
 K_L&=\frac{ma^2}{2}\left[(\omega_c-\omega_p)^2\cos^2\delta+
                         \omega_p^2\sin^2\delta\right]
             +\frac{I_m+I_o}{2}\omega_p^2,\\
 F_i&=-ma[(\omega_c-\omega_p)^2+\omega_p^2]\sin\delta\,v,\qquad
 F_o=-2ma(\omega_c-\omega_p)\omega_p\cos\delta\,u,\\
 Q_p&=ma^2\omega_c^2\cos\delta\sin\delta,\qquad
 Q_c=-ma^2[(\omega_c-\omega_p)^2+\omega_p^2]\cos\delta\sin\delta .
 \label{eq:oldham-spatial}
\end{align}
The force sum is $m\ddot M$. Input couple
$T_i=Q_p-\tau_{\rm rec}$ follows from the angular equation.
Near and far bearing forces are $-(1+h/\ell)F_i$ and $hF_i/\ell$;
their sum and bending moment close independently. The overhang moment is
$(-hF_{i,y},hF_{i,x},0)$.
The two pad resultants are $F_n/2\pm T/(2b)$ for the local resultant
$F_n$ and transmitted torque $T$. This bilateral idealization must be
checked against physical preload and contact capacity.

At $(\omega_s,\omega_c,\omega_r,\omega_p)=(7/2,1,0,-7/3)$,
$\tau_s=2$, $\tau_{\rm rec}=1$ in SI units and initial
$\theta=\phi=0$, set $\tau_o=-T_i$. The train then requires
$\tau_r=5-10\tau_o/3$, $\tau_c=-7+7\tau_o/3$;
its carrier drive additionally supplies $Q_c$. The whole boundary includes
train and linkage, so the two sides of the planet and moving-pin transfers
cancel only after their separate integrals.

\begingroup\small

| Interval, s | $W_s$, J | $W_c$, J | $W_r$, J | $W_{\rm rec}$, J | Independent $\Delta K$, J |
|-----------------|-----------------|-------------------------------|------:|------------------|--------------------|
| $[0,3\pi/40]$ | $21\pi/40$ | $-7\pi/20-2499/5000000$ | $0$ | $-7\pi/40$ | $-2499/5000000$ |
| $[0,3\pi/5]$ | $21\pi/5$ | $-14\pi/5$ | $0$ | $-7\pi/5$ | $0$ |

: Each work is the integral of its specified shaft product. The second interval returns the linkage store; the first does not.

\endgroup

The train alone has steady $673/72\,\mathrm J$ under its declared effective
unit inertias; this control treats planet spin as that train coefficient and
adds the new middle/output terms in $K_L$ once. Evaluation at the two ends,
rather than an assumed periodic energy, gives the last column.
The exact residual is zero and no event occurs. These slot and bearing
forces do not determine Cardan-cross forces.

Physical stator mounting also changes a brake law. For a massless viscous
receiver with $D=1/2\,\mathrm{N\,m\,s}$, shaft rate
$\omega_p=-7/3$ and stator rate $\omega_f$, inward powers to the receiver
are $D(\omega_p-\omega_f)\omega_p$ and
$-D(\omega_p-\omega_f)\omega_f$, with exported heat
$-D(\omega_p-\omega_f)^2$. On $[0,1]\,\mathrm s$ the three works
are $(49/18,0,-49/18)\,\mathrm J$ for $\omega_f=0$ and
$(35/9,5/3,-50/9)\,\mathrm J$ for $\omega_f=1$.
A real reference drive must supply the second mounting.

The zero-cycle support result also depends on the load history. In the
massless fixed-phase joint control take
$\cos\beta_1=4/5$, $\cos\beta_2=3/5$, $\omega_p=2$,
$\omega_c=1$ and $\psi=t$ on $[0,\pi]\,\mathrm s$.
For $k=3/4$,
$\chi=k/(\cos^2\psi+k^2\sin^2\psi)$.
A passive variable torque demand $\mathcal T=1/\chi$ gives
$P_p=2$, $P_c=1/\chi-1$ and $P_{\rm rec}=-(1+1/\chi)$.
Since $\int_0^\pi\chi^{-1}dt=25\pi/24$, the works are
$(2\pi,\pi/24,-49\pi/24)\,\mathrm J$.
The empty store at both endpoints gives zero residual.
The nonzero support work is derived for this load; the constant-load cycle
null retains its separate scope. Unequal joint angles require a different
axis/support arrangement from the equal-angle parallel-offset baseline.

## Locking and release with actual endpoint states
\label{sec:clutch}

A coaxial sphere inside an annular carrier isolates the locking question
without imposing an orbital rolling constraint. Let
$I_b=2/5$, $I_c=3/5\,\mathrm{kg\,m^2}$ and viscous clutch
$D=1\,\mathrm{N\,m\,s}$. Holding $\omega_c=1\,\mathrm{rad/s}$
with the ball initially at rest gives
$\omega_b=1-e^{-5t/2}$. On $[0,1]\,\mathrm s$, independently integrating
drive $D(1-\omega_b)$, ball transfer $D(1-\omega_b)\omega_b$ and
heat $D(1-\omega_b)^2$ gives
\begin{equation}
 W_d=\frac25(1-e^{-5/2}),\quad
 \Delta K_b=\frac15(1-e^{-5/2})^2,\quad
 H=\frac15(1-e^{-5})\qquad(\mathrm J).
 \label{eq:clutch-fixed}
\end{equation}
The ball store follows independently from its final rate.
With a free undriven carrier initially at rate one, the same torque laws
instead give
$\omega_c=3/5+2e^{-25t/6}/5$,
$\omega_b=3/5-3e^{-25t/6}/5$ and
$H=3(1-e^{-25/3})/25\,\mathrm J$ at one second.
Weighted momentum is conserved, the initial kinetic store is
$3/10\,\mathrm J$, and both final spin stores must be retained.
A finite removal of torque preserves velocity; an impulsive release requires
its own contact and transfer law.

A finite actuator model adds strain $q$, thermal excess $H$ and gate
voltage $v_g$. Declare
\begin{align}
 T_c&=Kq+D(\omega_c-\omega_b),&\dot q&=\omega_c-\omega_b,\\
 I_c\dot\omega_c&=T_d-T_c,&
 I_b\dot\omega_b&=T_c-\omega_b/10,\qquad
 T_d=2(\Omega_d-\omega_c),\\
 \frac1{100}\dot v_g&=(V_g-v_g)/10,&
 \dot H&=2(\Omega_d-\omega_c)^2+D(\omega_c-\omega_b)^2
                  +(V_g-v_g)^2/10-H/2 .
 \label{eq:clutch-finite}
\end{align}
The independently defined store is
$I_c\omega_c^2/2+I_b\omega_b^2/2+Kq^2/2+H+v_g^2/200$.
External powers are
$T_d\Omega_d$, $\dot Kq^2/2$, $V_g(V_g-v_g)/10$,
$-\omega_b^2/10$ and $-H/2$.
Multiplying the separate laws gives their sum as the store derivative.
The stiffness actuator is physically distinct from the gate supply.

Use one-second stages with smooth cosine ramps
$r(t)=(1-\cos\pi t)/2$ on each local $0\leq t\leq1$:
prepare $(\Omega_d,K,D,V_g)=(r,r/5,1/10,1)$;
lock with $(1,1/5,2,1)$;
release with $(1,(1-r)/5,2(1-r),0)$;
and reduce the drive with $(1-r,0,1/2,0)$.
Start all states at zero. Each actual final store is evaluated from the
resulting state; finite damping does not specify an exact reset.
The equations define a conditional finite comparison, with no decimal
trajectory asserted here. A stiffness actuator's efficiency, real release
law and temperature dependence require acquisition. Both shaft channels,
spring state, gate and stiffness supplies, heat export and thermal endpoints
belong to that comparison.


## Simple train and four observation frames

Let the sun, planet, internal ring, and carrier have indices $s,p,r,c$.
All axes are initially parallel to $+z$, with positive right-hand rates.
For common module $m_0$, radii $r_j=m_0Z_j/2$ satisfy
$a=r_s+r_p=r_r-r_p$ and $Z_r=Z_s+2Z_p$. Rolling at each mesh gives
\begin{equation}
 \omega_p=\omega_c-\frac{Z_s}{Z_p}(\omega_s-\omega_c)
 =\omega_c+\frac{Z_r}{Z_p}(\omega_r-\omega_c),\quad
 Z_s(\omega_s-\omega_c)+Z_r(\omega_r-\omega_c)=0.
 \label{eq:rolling}
\end{equation}
This carrier-relative construction is consistent with [Culpepper (2002)][gear].
Three equally spaced planets additionally require $(Z_s+Z_r)/3$ integral
and adequate clearance. Configuration I uses $(24,18,60)$ and $m_0=1/500$ m,
so $(r_s,r_p,r_r,a)=(3/125,9/500,3/50,21/500)$ m and the phase quotient is 28.

![Schematic pitch contacts and external shaft ports. Only one planet is drawn. Force arrows indicate positive tangential and radial components; their signed values follow the free bodies.](figures/gear-ports.pdf){#fig:gear width=93%}

\FloatBarrier

Figure \ref{fig:gear} locates the forces and shaft ports.
For $q=3$ equally loaded planets, tangential forces on one planet are $F_s,F_r$,
and its pin reaction is $R_t\mathbf e_\theta+R_r\mathbf e_r$.
With zero pin couple, Newton–Euler equations, independently of energy, give
\begin{align}
 F_s&=\frac{\tau_s-I_s\dot\omega_s}{qr_s},&
 F_r&=F_s+\frac{I_p\dot\omega_p}{r_p},&
 R_t&=m_pa\dot\omega_c-F_s-F_r,\\
 \tau_r&=I_r\dot\omega_r+qr_rF_r,&
 \tau_c&=I_c\dot\omega_c+qaR_t,& R_r&=-m_pa\omega_c^2.
 \label{eq:forces}
\end{align}
These radial forces belong to the tangential pitch-contact idealization.
Tooth pressure angles would add radial reactions. Constant rates give
$(\tau_s,\tau_r,\tau_c)=\tau_s(1,5/2,-7/2)$ in configuration I.

The complete train contains gears, carrier, and pins. Only its three shaft
ports cross the mechanical boundary in this rolling model. A planet
subboundary also has the separately oriented powers
\begin{equation}
 P_{sp}^f=F_sr_s(\omega_s-\Omega),\quad
 P_{rp}^f=F_rr_r(\omega_r-\Omega),\quad
 P_{cp}^f=R_ta(\omega_c-\Omega).
 \label{eq:internal}
\end{equation}
Each opposite mesh or pin side has the opposite product. Here $\Omega$ is
$0,\omega_c,\omega_s$, or $\omega_r$ for the four specified observations.
Their coordinate reconstructions do not physically remount any load. The
measured division among shaft, mesh and pin transfers must retain each
side; a shaft work difference cannot be assigned to a pin [OP-EPI-02].

Define $J_c=I_c+qm_pa^2$, $J=I_s+I_r+J_c+qI_p$ and
\begin{equation}
 K^0=\frac12(I_s\omega_s^2+I_r\omega_r^2+J_c\omega_c^2+qI_p\omega_p^2),
 \quad H=I_s\omega_s+I_r\omega_r+J_c\omega_c+qI_p\omega_p,
 \quad E^f=K^0-\Omega H.
 \label{eq:frame}
\end{equation}
The relative kinetic energy is $K^f=K^0-\Omega H+J\Omega^2/2$;
$E^f$ includes effective centrifugal potential $-J\Omega^2/2$.
This effective energy and the physical ground energy are distinct stores.
The familiar rotating-velocity law is documented in [MIT (2022)][frames].

\begin{theorem}[Frame work and its path division]
For the specified rigid train, $\sum_j\tau_j=\dot H$ and
\begin{align}
 \dot K^0&=\sum_j\tau_j\omega_j,&
 \dot E^f&=\sum_j\tau_j(\omega_j-\Omega)-\dot\Omega H,\\
 W_j^0-W_j^f&=\int\Omega\tau_jdt,&
 \int\Omega\dot Hdt+\int H\dot\Omega dt&=[\Omega H]_{t_0}^{t_1}.
 \label{eq:frame-work}
\end{align}
\end{theorem}
\noindent\textit{Proof.}
Sum \eqref{eq:forces} after multiplying the spin and translation equations
by their own rates. The opposite contact products cancel using
\eqref{eq:rolling}; summing moments uses both equalities defining $a$.
Differentiating \eqref{eq:frame}, subtracting each shaft product, and
integrating the product derivative of $\Omega H$ gives the remaining
identities. $\square$

The effective-field term separates as Euler power
$-\dot\Omega(H-J\Omega)$ and explicit potential-time term
$-J\Omega\dot\Omega$. Each is integrated before combining them.
They are coordinate terms, not physical motor or heat supplies. Reconstructing
these transient frame balances within independent uncertainty is the
physical comparison [OP-EPI-01].
For a genuine rotating support its physical torque–rate work is additional.

For exact rational examples choose $I_s=I_r=qI_p=J_c=1\,\mathrm{kg\,m^2}$,
$m_p=1$ kg, and $I_c=248677/250000\,\mathrm{kg\,m^2}>0$.
Flywheels may supply these inertias; no uniform-disc mass law is assumed.
Let $(\omega_s,\omega_r,\omega_c,\omega_p)=(7/2,0,1,-7/3)$ rad/s
and $\tau_s=2$ N m on $[0,1]$ s. Direct state evaluation gives
$H=13/6$, $K^0=673/72$, $E^c=517/72$ in SI units at **both** endpoints.

| Separately integrated work, J | Ground | Carrier |
|-------------------------------------|----------------:|----------------:|
| Sun shaft | $7$ | $5$ |
| Ring shaft | $0$ | $-5$ |
| Carrier shaft | $-7$ | $0$ |
| One sun contact into planet | $7/3$ | $5/3$ |
| One ring contact into planet | $0$ | $-5/3$ |
| One pin into planet | $-7/3$ | $0$ |

: Configuration I in steady operation. Only the first three entries belong to the complete external shaft sum. Each complete residual is zero.

Preparation instead prescribes $\omega_j(t)=\omega_{j*}t$ and
$\tau_s(t)=2t$ on $[0,1]$ s from rest. Equations \eqref{eq:forces} give
$\tau_r=5t-595/36$ and $\tau_c=673/36-7t$. For any frame
$\Omega=\Omega_*t$, each shaft integral is
\begin{equation}
 W_j^f=(\omega_{j*}-\Omega_*)\left(\frac{a_j}{3}+\frac{b_j}{2}\right),
 \quad (a_s,a_r,a_c)=(2,5,-7),\quad
 (b_s,b_r,b_c)=(0,-595/36,673/36).
 \label{eq:ramp}
\end{equation}
The units of $a_j,b_j$ here incorporate the one-second ramp.
Every internal integral follows \eqref{eq:internal} with the affine forces
in \eqref{eq:forces}; explicitly $\int_0^1 (A t+B)t\,dt=A/3+B/2$.

| Observation | $(W_s,W_r,W_c)$, J | Effective-field work, J | $E(0),E(1)$, J |
|---------------------|--------------------------------------|-----------------------|-------------------------|
| Ground and held ring | $(7/3,0,505/72)$ | $0$ | $0,673/72$ |
| Carrier | $(5/3,475/72,0)$ | $-13/12$ | $0,517/72$ |
| Sun | $(0,3325/144,-2525/144)$ | $-91/24$ | $0,127/72$ |

: Preparation works and independent endpoints. Every complete sum equals its store change. The ground and ring frames coincide only for this held-ring path.

For a distinct history set $H=(13/6)t$ and
$\Omega=t+b t(1-t)$. With $d=\omega_s-\omega_c$ one has
$H=4\omega_c-(11/15)d$, so choose $\omega_c=\Omega$ and
$d=(15/11)(4\Omega-H)$. Equation \eqref{eq:rolling} determines all other
rates; the ring moves during preparation when $b\ne0$ and reaches the same
held endpoint. The shaft and field differences are
$(13/6)(1/2+b/6)$ and $(13/6)(1/2-b/6)$ J. Thus $b=0,1$ give respectively
$(13/12,13/12)$ and $(13/9,13/18)\,\mathrm J$. The same endpoint total $13/6$ J follows by
integration by parts, not by presuming an equal division or a held ring
throughout a nonproportional preparation. Measuring this history-dependent
shaft/field division is a separate comparison [OP-EPI-04].

For a locked approach retain $\omega_c=1$, put $\omega_s=1+\epsilon$,
and obtain $\omega_r=1-2\epsilon/5$, $\omega_p=1-4\epsilon/3$.
At fixed $\tau_s=2$ the one-second ground shaft works are
$(2+2\epsilon,5-2\epsilon,-7)$ J. At
$\tau_s=2\epsilon$ they are $\epsilon$ times that triple.
Their exact limits are $(2,5,-7)$ and $(0,0,0)$ J. Carrier-frame works
vanish at the locked endpoint in both controls. The independent kinetic
endpoints are evaluated by \eqref{eq:frame}; a steady interval has identical
states at its ends, not necessarily zero energy. Fixed-drive and scaled-drive
approaches require their own finite uncertainty bounds [OP-EPI-12].

## Rotor, stator, phase, and load

Let $x=\theta_p-\phi$, where $\dot\phi=\omega_c$, and specify
$\theta_o=\phi+F(x)$. The output rate is
$\omega_o=\omega_c+\chi(\omega_p-\omega_c)$, $\chi=F'(x)$.
For the same rotor path two stator counts obey
$N_o^0-N_o^c=\Delta\phi/(2\pi)$. Physical stator remounting under load
requires a fresh trajectory, not substitution into the unloaded path.

For a Hooke joint define the continuous angle lift
$H_\beta(x)=\operatorname{atan2}(\sin x,\cos\beta\cos x)$.
The two-joint Z path is
$F=H_{\beta_2}(H_{\beta_1}(x)+\gamma+\pi/2)+\pi/2$,
up to a constant. Equal angles and carrier phasing $\gamma=0$ give $F=x$;
quarter-turn phasing gives
\begin{equation}
 \tan F=\frac{\tan x}{\cos^2\beta},\qquad
 \chi=\frac{\cos^2\beta}{\cos^4\beta\cos^2x+\sin^2x},\qquad
 F(x+\pi)=F(x)+\pi.
 \label{eq:hooke}
\end{equation}
An arbitrary finite readout retains $[F(x)-x]_{t_0}^{t_1}/(2\pi)$.
Ground phasing prescribes $\gamma=-\phi$ in the full map and introduces
its own phase actuator; it supplies a mean carrier-relative count with
endpoint ripple. The paired-stator identity does not prohibit differential
instruments that report other relative observables.

These maps cover the eleven specified ideal mountings: equal-angle correct
and quarter-turn Hooke paths against ground and carrier stators; the
kinematic ground-phased Hooke path with ground stator; constant-ratio offset
paths against both stators; and bevel ratios one and two against both
stators. Oldham's orthogonal sliding coordinates are $a\cos x,a\sin x$.
A Schmidt path can share the angle map without sharing its force system.

For configuration II the linkage contains input inertia $I_R$, orbiting mass
$m_R$, output inertia $I_o$, and massless joint members. An imposed output
torque $\tau_L$ and drag $d_0\operatorname{sgn}(\omega_o-\omega_\sigma)$
give
\begin{equation}
 \mathcal T=I_o\dot\omega_o-\tau_L+d_0\operatorname{sgn}(\omega_o-\omega_\sigma),
 \quad \tau_d=I_R\dot\omega_p+\chi\mathcal T,\quad
 \tau_u=(1-\chi)\mathcal T.
 \label{eq:link}
\end{equation}
The five physical work channels are the separate integrals of
$\tau_d\omega_p$, $\tau_u\omega_c$, $\tau_L\omega_o$,
$-d_0\operatorname{sgn}(\omega_o-\omega_\sigma)\omega_o$, and
$m_Ra^2\dot\omega_c\omega_c$. Their sum differentiates
$K_L^0=(I_R\omega_p^2+m_Ra^2\omega_c^2+I_o\omega_o^2)/2$.
The stator reaction has power
$+d_0\operatorname{sgn}(\omega_o-\omega_\sigma)\omega_\sigma$;
including it gives mechanical conversion
$D=d_0|\omega_o-\omega_\sigma|$. Thermal storage changes the larger
boundary as derived below.

For constant input rates, constant load, and unchanged drag sign, the
Hooke support-cycle integral over $T_b=\pi/|\omega_p-\omega_c|$ is zero:
$\int(1-\chi)dt=0$ and its inertial part is proportional to
$[\chi-\chi^2/2]$ at equal phases. In a massless control set
$(\omega_p,\omega_c)=(3,1)$, $\tau_L=-1$, $d_0=0$.
On $[0,\pi/2]$ s the Hooke drive, support, and receiver works are
$(3\pi/2,0,-3\pi/2)$ J. The bevel map $F=2x$ instead gives
$(3\pi,-\pi/2,-5\pi/2)$ J. Both ideal endpoint stores are zero.
In the carrier frame the bevel works are $(2\pi,0,-2\pi)$ J.
A whole-cycle support null cannot be inferred for a partial cycle. Actual
Hooke support work is the first measurement [OP-EPI-06]; the different
bevel support path needs its own work account [OP-EPI-07].

For unequal angles with correct phasing,
$\tan F=(\cos\beta_2/\cos\beta_1)\tan x$.
Choose these cosines as $3/5,4/5$ respectively, in the order
$\cos\beta_2=3/5$, $\cos\beta_1=4/5$. With $x=t$, $\omega_c=1$,
$\mathcal T=1$, and $[0,\pi/4]$ s, the support work is
$\pi/4-\arctan(3/4)>0$ J, against zero for equal angles.
These deliberately large articulations are mathematical controls;
buildability and clearance require separate geometry. Under carrier
acceleration, the rotor-pin integral for $m_Ra^2=1$ and $\omega_c=t$
is $1/2$ J. For an independently moving phase coordinate $\gamma$,
virtual displacement adds torque
$\tau_\gamma=\mathcal T\,\partial\theta_o/\partial\gamma$;
its work is $\int\tau_\gamma\dot\gamma dt$. A unit torque through
$\gamma=t$ supplies 1 J. None is supplied by a count alone. Their combined physical lead-out,
carrier acceleration and phase-reference works remain to be determined
[OP-EPI-31].

The actual Cardan force and bending system requires its bearing constraints,
member stiffnesses, and application-point motions. A finite control with
$F_x=1$ N, $\dot x=1$ m/s over one second transfers 1 J; a fixed support
transfers zero at the same force. The same rule applies to a bending couple.
It specifies a force/displacement discrimination, not the unknown force in
an unspecified double Cardan device. Full transverse forces and bending
couples, including their application-point motion, are the acquisition
target [OP-EPI-30].

For a stator comparison reproducing the finite scale of
[Nilre and Herlin (2026)][main], take $\omega_p=-14\pi/3$,
$\omega_c=2\pi$, $d_0=1/50$ and duration $7/2$ s. The separate relative
drag integrals are $Q_0=49\pi/150$ and $Q_c=7\pi/15$ J, giving
$Q_c-Q_0=7\pi/50$ J. This is a change of physical mounting, not a
coordinate dependence of the heat produced by one mounting. The actual
loaded readout and its finite endpoint corrections require identification
[OP-EPI-05].

## Attaching a receiver changes the free bodies

Attach three identical unity-ratio, ground-stator lead-outs to configuration I,
with $\tau_L=+1$ N m on the negative-speed outputs and zero drag.
The steady linkage requires $\tau_d=-1$, $\tau_u=0$.
The planet equation becomes
$F_r=F_s+(I_p\dot\omega_p+\tau_d)/r_p$;
the carrier equation also includes
$q(\tau_u+m_Ra^2\dot\omega_c)$. The resulting steady torques are
$(2,-5,0)$ N m. Separate one-second external works are
\begin{equation}
 (W_s,W_r,W_c)=(7,0,0)\ \mathrm J,\qquad
 W_{L,j}=-7/3\ \mathrm J\quad(j=1,2,3).
 \label{eq:loaded}
\end{equation}
The shared axle transfers $+7/3$ J to each linkage and $-7/3$ J to its
planet. Both endpoint stores are
$673/72+3[(I_R+I_o)(7/3)^2+m_Ra^2]/2$ J for the stated added inertias.
They agree because the actual endpoint rates agree. The carrier work changes
from $-7$ to zero, a $+7$ J comparison. Adding a receiver to an unchanged
unloaded force table would miss that change.
The full joint, bearing, phase-driver, and thermal balance still requires
those independent physical ports and states. The corresponding
complete loaded-train work remains a physical measurement [OP-EPI-33].

# Additional mechanical boundaries

## Compound circulation and a distinct two-sun geometry

In configuration III two coaxial members $A,B$ engage rigidly connected
planet sections $P_A,P_B$ carried by $C$. Let $s_X=-1$ for an external
mesh, $+1$ for an internal mesh, and
\begin{equation}
 a=\frac{m_0}{2}(Z_A-s_AZ_{pA})=\frac{m_0}{2}(Z_B-s_BZ_{pB}),\quad
 h_X=s_X\frac{Z_{pX}}{Z_X},\quad R=\frac{h_A}{h_B}.
 \label{eq:compound}
\end{equation}
Rolling gives $\omega_X-\omega_C=h_X(\omega_P-\omega_C)$.
The planet spin equation
$s_Ar_{pA}F_A+s_Br_{pB}F_B=0$, together with shaft and carrier free bodies,
gives $(\tau_A,\tau_B,\tau_C)=\tau_*(1,-R,R-1)$.
This is a massless quasistatic model with empty endpoint stores.

Three shaft powers and opposite sides of the two contacts and pin give
nine component powers, namely signed copies of
$p_X^f=\tau_X(\omega_X-\Omega)$.
Define $D_0=\max_X|\tau_X\omega_X|>0$. Then
\begin{equation}
 \mathcal C_f=\frac{\max_X|p_X^f|}{D_0},\quad
 \mathcal C_0=1,\quad
 \mathcal C_C=\begin{cases}1/|R-1|,&A\text{ held},\\
 |R|/|R-1|,&B\text{ held}.
 \end{cases}
 \label{eq:ratio}
\end{equation}
Each work is separately $p_X^fT$, with its opposite side integrated as
$-p_X^fT$ before combining. Choose $\omega_C=1$, $\tau_*=1$, $T=1$ in SI units.
Five pitch-compatible tooth sets give the following exact values.

| $(Z_A,Z_{pA},Z_{pB},Z_B)$ | $(s_A,s_B)$ | $R$ | $\mathcal C_C$, $A$ held | $\mathcal C_C$, $B$ held |
|------------------------------------|--------------------|-----------------|-----------------------|-----------------------|
| $(24,18,18,60)$ | $(-1,+1)$ | $-5/2$ | $2/7$ | $5/7$ |
| $(20,22,20,62)$ | $(-1,+1)$ | $-341/100$ | $100/441$ | $341/441$ |
| $(30,20,19,31)$ | $(-1,-1)$ | $62/57$ | $57/5$ | $62/5$ |
| $(62,20,21,63)$ | $(+1,+1)$ | $30/31$ | $31$ | $30$ |
| $(100,58,59,101)$ | $(+1,+1)$ | $2929/2950$ | $2950/21$ | $2929/21$ |

: Compound controls. Ground ratios are one in all cases. The other frames follow by putting $\Omega=\omega_A$ or $\omega_B$ in equation \eqref{eq:ratio}. Multiple-planet phasing is a separate assembly condition; a single stepped planet suffices for these kinematic controls.

At $R=1$ with either coaxial member held, $D_0=0$; the ratio is undefined.
No finite resolution on the denominator establishes an infinite physical
ratio. Approaching that geometry at finite tooth numbers is a sequence of
specified comparisons. Their frame-dependent power ratios require
synchronized torque and speed measurements with a resolved denominator
[OP-EPI-08].

A Ravigneaux arrangement has independent long and short planet spins,
not the single $P$ of \eqref{eq:compound}. To exhibit the distinction,
use two sun planes and one long/short pair with teeth
$(Z_A,Z_B,Z_R,Z_S,Z_L)=(30,60,90,15,15)$.
With $u_j=\omega_j-\omega_C$, its four independent rolling equations are
\begin{equation}
 30u_A+15u_S=0,\quad 15u_S+15u_L=0,\quad
 60u_B+15u_L=0,\quad 90u_R-15u_L=0.
 \label{eq:ravigneaux}
\end{equation}
At module $1/30$ m the short and long centres can lie on the same radial
line at $3/4$ and $5/4$ m; their separation is $1/2$ m, the sum of their
pitch radii. Sun planes are axially separated. This is pitch geometry,
not a tooth-strength or packaging design.
With $\omega_C=1$, $\omega_R=0$, rates are
$(\omega_A,\omega_B,\omega_S,\omega_L)=(-2,5/2,7,-5)$.
The independent reduced constraints are $u_A+2u_B=0$ and $u_A-3u_R=0$.
Their massless contact reactions have multiplier torque vectors
$(1,2,0,-3)$ and $(1,0,-3,2)$ on $(A,B,R,C)$, as follows by resolving
each contact's equal and opposite force. Choosing $\tau_A=\tau_B=1$
gives $\tau_R=-3/2$, $\tau_C=-1/2$.
The separate one-second ground shaft works are $(-2,5/2,0,-1/2)$ J;
the carrier works are $(-3,3/2,3/2,0)$ J. Both sum to zero, and the
shaft ratio is $6/5$ against its ground denominator $5/2$ W.
Internal contact powers require these four meshes, not the earlier nine-side
set. Empty massless stores close this bounded model only.

Helical thrust or a nonparallel joint adds vector contact and support ports.
For instance an imposed axial force 1 N through 1 m over one second adds
1 J, whereas holding that coordinate gives zero. Its existence and sign in
a given gear require that gear's contact geometry, compliance, and measured
trajectory. The two-sun example supplies no such missing law. Other geometry and
contact directions retain their own energy partition [OP-EPI-21].

## Contact changes, reversals, and unequal loading

A compliant gap has overlap $\delta$, stored energy
$U=k[\max(\delta,0)]^2/2$, and, during compression contact,
$F=k\delta+c\dot\delta$. Keep the damper active only on its declared
contact branch; separating and tensile branches need their own force law.
For the spring/damper subboundary, input is $F\dot\delta$ and heat export
is $-c\dot\delta^2$. At $\delta=0$ the spring store is continuous even
when damping makes power jump. The control $\delta=t$, $k=2$, $c=1$
on $[0,1]$ s has
\begin{equation}
 W_{\rm contact}=\int_0^1(2t+1)dt=2\ \mathrm J,\quad
 W_h=-1\ \mathrm J,\quad U(0)=0,\quad U(1)=1\ \mathrm J.
 \label{eq:contact}
\end{equation}
At onset input power changes from 0 to 1 W, while $\Delta U$ across the
instant itself and impulse work are zero. Ramps approaching contact are
separate intervals; the actuator imposing $\delta$ has the opposite work. Actual re-engagement
power jumps require the finite contact law and event-side measurements
[OP-EPI-10].

For an impulsive alternative take two freely translating effective masses
$m_1,m_2$ and relative incoming speed $v_-=v_1^--v_2^->0$.
A declared restitution coefficient $e\in[0,1]$ gives
$J=(1+e)\mu v_-$, $\mu=m_1m_2/(m_1+m_2)$, from impulse momentum
and $v_+=-ev_-$. The separate contact-side works under a resolved
regularization with no other impulse are
\begin{equation}
 W_1=\frac{m_1}{2}[(v_1^+)^2-(v_1^-)^2],\quad
 W_2=\frac{m_2}{2}[(v_2^+)^2-(v_2^-)^2],\quad
 W_1+W_2=-\frac{\mu}{2}(1-e^2)v_-^2.
 \label{eq:impact}
\end{equation}
These follow directly by integrating $m\dot v\,v$, not by multiplying a
force impulse by one arbitrarily chosen event velocity.
For unit masses, $(v_1^-,v_2^-)=(1,0)$ and $e=1/2$, final velocities
are $(1/4,3/4)$, $J=3/4$ N s, works $(-15/32,9/32)$ J, and kinetic
stores $1/2,5/16$ J. The contact receives $3/16$ J. If contact and its
thermal store are included, that conversion is internal; if its heat is
exported, the external heat work is $-3/16$ J. Do not also add the two
internal contact works to that larger boundary.
A finite pulse with the specified restitution can measure these transfers;
it cannot realize a zero-time impulse. Physical contact regularization
and its energy destination remain independent questions [OP-EPI-22].

For a full compliant train write actual contact coordinates
$\delta_l(q)$, $U=\sum_l k_l\max(\delta_l,0)^2/2$, and apply each force
through its geometric gradient. The rigid no-slip constraints must be
released where that compliance acts. Multiplying the full Newton equations
by all body velocities gives
$\dot K+\dot U=\sum P_{\rm ext}-\sum_l c_l\dot\delta_l^2$ on each
active contact interval. In a coaxial observation add
$-\dot\Omega H$ to the effective energy $K+U-\Omega H$.
An explicit full-train control includes all three planets and both contacts
on each. Keep configuration I's inertias, hold the sun, ring, and planet
spin angles at zero, and prescribe $\theta_c=t^2/2$ on $[0,1]$ s.
Define the two linear pitch-compliance coordinates on each planet by
$\delta_s=a\theta_c-r_s\theta_s-r_p\theta_p-g$ and
$\delta_r=a\theta_c-r_r\theta_r+r_p\theta_p-g$.
Let $g=a/8$, $k=2/a^2$, and $c=1/a^2$ in SI units. All six contacts
engage at $t=1/2$ s; during contact they have
$\delta=a(t^2-1/4)/2$, $\dot\delta=at$, and
$F=(t^2+t-1/4)/a$. Equal opposite planet spin torques leave
$\omega_p=0$ without a planet drive. Resolving each contact gradient gives
$\tau_s=-3r_sF$, $\tau_r=-3r_rF$, and
$\tau_c=1+6aF$ after engagement; before it, $(\tau_s,\tau_r,\tau_c)=(0,0,1)$.
This is an exact lumped linear pitch-contact model, not a claim about
finite-deflection tooth geometry.

Separate integration on the gap and contact intervals gives
\begin{equation}
 W_c^0=99/32,\quad W_s^0=W_r^0=0,\quad
 \sum_{l=1}^{6}W_{h,l}=-7/4,\quad
 (K+U)(0)=0,\quad (K+U)(1)=43/32
 \quad\mathrm J.
 \label{eq:full-contact}
\end{equation}
Each heat work is $-7/24$ J; each spring endpoint is $9/64$ J and
final carrier kinetic energy is $1/2$ J. In carrier observation,
$(W_s^c,W_r^c,W_c^c)=(83/112,415/224,0)$ J, field work is $-1/2$ J,
and effective endpoints are $0,11/32$ J. At engagement damping makes
finite contact powers jump; coordinates, velocities, and stores remain
continuous and impulse work is zero. These independently evaluated stores
close both balances. Clearance in a lead-out, changing active tooth contacts,
unequal loading, and actual force laws remain separate physical questions. Their
full accelerating-train remainder is not fixed by this contact control
[OP-EPI-23].

With unequal planet fractions $(1/2,1/3,1/6)$, a steady total 7 J sun-contact
transfer divides into $(7/2,7/3,7/6)$ J rather than three $7/3$ J values.
The fractions specify a load-sharing law; they are not inferred from an
aggregate balance. A pin couple $M=1/10$ N m on a planet with
$\omega_p-\omega_c=-10/3$ rad/s gives pair work $-1/3$ J in one second.
Its two separately integrated sides are $M\omega_p$ and $-M\omega_c$.
Bearing heat or elastic torsion then needs an independently chosen law.
Each planet's force and couple channels must therefore be observed. The
load-sharing and pin-couple partition is a local measurement [OP-EPI-24].

For a reversal, $\omega=1-2t$, $\tau=1$ on $[0,1]$ s gives
$W_{[0,1/2]}=1/4$ J and $W_{[1/2,1]}=-1/4$ J.
Net work is zero while $\int|P|dt=1/2$ J. A separate Coulomb drag of
unit magnitude converts $\int|\omega|dt=1/2$ J; treating its sign as
constant would give the wrong zero. A unit inertial rotor has equal endpoint
kinetic energies $1/2$ J on this prescribed reversal, and its inertial
actuator torque $\dot\omega=-2$ supplies works $-1/2,+1/2$ J on the two
halves. Any concurrent applied constant torque and brake require their
own compensating drive. The examples are separate effort laws, not a claim
that torque one alone produces that trajectory. Signed and absolute works
through an actual reversal need independently calibrated channels
[OP-EPI-28].

## Radial motion and vector observation

For a centre at radius $r$, planar Newton equations give
$F_r=m(\ddot r-r\omega_c^2)$ and
$F_t=m(r\dot\omega_c+2\dot r\omega_c)$.
Both $F_r\dot r$ and $F_tr\omega_c$ are physical work channels.
With $m=1$, $r=1+t$, $\omega_c=1$ over one second, their works are
$-3/2$ and $+3$ J. Ground kinetic energy changes from $1$ to $5/2$ J;
carrier effective energy changes from $0$ to $-3/2$ J.
This radial-guide control requires compliant or variable contact geometry
before it can represent an actual radially moving planet.

In any rotating observation,
$\mathbf F_{\rm Cor}=-2m\symbf{\Omega}\times\mathbf v^f$ has
$\mathbf F_{\rm Cor}\cdot\mathbf v^f=0$.
At fixed radius, $\mathbf v^f=r(\omega_c-\Omega)\mathbf e_\theta$,
so the Coriolis force is generally nonzero outside ground and carrier
observations. Radial motion adds a tangential component; it does not add
net Coriolis power. This distinction follows from the vector product itself. Radial
support work and changed contact geometry still need identification
[OP-EPI-26].

For observations rotating about a fixed common origin in three dimensions,
\begin{equation}
 E^f=K^0+U-\symbf{\Omega}\cdot\mathbf H,\quad
 P_j^f=\mathbf F_j\cdot(\mathbf v_j-\symbf{\Omega}\times\mathbf r_j)
       +\mathbf M_j\cdot(\symbf{\omega}_j-\symbf{\Omega}),
 \quad P_{\rm field}=-\dot{\symbf{\Omega}}\cdot\mathbf H.
 \label{eq:vector}
\end{equation}
Here $U$ is rotationally invariant internal potential, and all vectors and
time derivatives in the equation are resolved in an inertial basis.
The result follows from $\sum(\mathbf r\times\mathbf F+\mathbf M)=\dot{\mathbf H}$
and the kinetic-energy identity, including the full inertia tensor in the
relative kinetic and centrifugal terms. A translating origin would add
linear-momentum terms and is outside this formula.
For a free spherical rotor of unit inertia with
$\symbf{\omega}=(1,0,2)$ and observation
$\symbf{\Omega}=(t,0,0)$, $K^0=5/2$ J at both endpoints, physical
work is zero, field work is $-1$ J, and effective energy changes from
$5/2$ to $3/2$ J. Dropping the transverse momentum predicts zero field
work. A symmetric axial train can have zero transverse momentum; the
rotor example distinguishes the vector laws without asserting that every
train has this nonzero component. The nonparallel-axis energy comparison
requires the full observed vector momentum [OP-EPI-27].

# Windings, returns, and finite dynamic correspondence

## Coordinate zero versus an attached branch

In a tapped pair, currents enter winding 1 at $a$ and winding 2 at $b$,
with returns $c$ and $a$. Thus
\begin{equation}
 (v_1,v_2)=(V_a-V_c,V_b-V_a),\qquad
 (I_a,I_b,I_c)=(i_1-i_2,i_2,-i_1).
 \label{eq:terminals}
\end{equation}
A common $V_j\mapsto V_j+g(t)$ leaves the complete winding voltages
unchanged. Its terminal contributions change by $gI_j$, whose sum is
zero by current conservation. Each changed work is separately
$\int gI_jdt$; deleting a return changes that sum.

A physical attachment instead has voltage $v_b$ across its own resistor
$R_b$ and capacitor $C_b$. On a prescribed ramp $v_b=t$ with
$R_b=C_b=1$ over one second, its source current is $i_b=t+1$.
For the attachment boundary, direct integration gives
\begin{equation}
 W_b=\int_0^1 t(t+1)dt=5/6\ \mathrm J,\quad
 W_h=-\int_0^1t^2dt=-1/3\ \mathrm J,\quad
 E_b(0)=0,\quad E_b(1)=1/2\ \mathrm J.
 \label{eq:bond}
\end{equation}
Adding a parallel constant-current receiver of 1 A over the same ramp gives
another $1/2$ J of receiver delivery and raises source work to $4/3$ J.
More generally $W_b=C_b/2+1/(3R_b)$ J for the unit ramp; a pure voltage
coordinate change gives no added branch work or capacitor store.
The driver holding that voltage must be included in the larger circuit;
without it the attached branch changes the voltage trajectory.
Ground-bond impedance, probe common-mode paths, interwinding capacitance,
and chassis capacitance are distinct branches with their own endpoints. Their
physical attachment work is the return question [OP-TRF-01].

## A regular winding model and its seven ports

Configuration IV has reciprocal inductance
\begin{equation}
 \mathsf L=\begin{pmatrix}L_1&M\\M&\rho^2L_1\end{pmatrix},\quad
 M=sk\rho L_1,\quad s=\pm1,\quad 0\leq k<1,\quad
 E_m=\tfrac12i^T\mathsf Li,\quad E_C=\tfrac12Cv_o^2.
 \label{eq:L}
\end{equation}
Here $L_1,C,\rho$ are positive. The determinant is
$\rho^2L_1^2(1-k^2)>0$. An exact decomposition is
$E_m=kL_1(i_1+s\rho i_2)^2/2+(1-k)L_1i_1^2/2+(1-k)\rho^2L_1i_2^2/2$.
The distinction between finite magnetic storage and the ideal transformer
is standard in [Haus and Melcher (1989), Section 9.7][magnet].

Let $\eta=1$ for tapped and $0$ for isolated connections, whose returns
remain physically distinct. A source $u$ behind $R_s>0$, a core shunt
$G_c$, and output load/probe conductances $G_L,G_P$ give, by Kirchhoff laws,
\begin{align}
 v_a&=\frac{u-R_s(i_1-\eta i_2)}{1+R_sG_c},&
 I_s&=i_1-\eta i_2+G_cv_a,\\
 \mathsf L\dot i&=(v_a,v_o-\eta v_a)^T-\operatorname{diag}(R_1,R_2)i,&
 C\dot v_o&=-i_2-(G_L+G_P)v_o.
 \label{eq:circuit}
\end{align}
The boundary includes windings, output capacitor, and the source, copper,
and core resistors. The source, receiver, probe, and immediate heat
reservoirs are external. Its seven separate powers are
\begin{equation}
 (uI_s,-R_sI_s^2,-R_1i_1^2,-R_2i_2^2,-G_cv_a^2,-G_Lv_o^2,-G_Pv_o^2).
 \label{eq:circuit-ports}
\end{equation}
Each negative resistor product is its voltage times outward current or,
under immediate export, $-T_b\dot S_{\rm out}$.
Multiplication of \eqref{eq:circuit} by $i^T$ and $v_o$ derives
$\dot E_m+\dot E_C=\sum P_j$. This does not assume that either store is
constant. Equation \eqref{eq:integrator} gives each work from its own
quadratic form, and endpoints use \eqref{eq:L} on the propagated state.

Use $L_1=1/25$ H, $\rho=1$, $k=19/20$, $s=+1$, $C=1/500$ F,
$R_s=1/5\,\Omega$, $R_1=R_2=1/10\,\Omega$, $G_c=1/100$ S.
A finite crossed comparison retains all combinations
\begin{equation}
 \begin{gathered}
 G_L\in\{1/10,2/5\},\quad G_P\in\{0,1/10\},\quad \omega\in\{0,2\pi\},\\
 x(0)\in\{(0,0,0),(0,0,1)\},\qquad u(t)=\cos(\omega t)\ \mathrm V.
 \end{gathered}
 \label{eq:crossed}
\end{equation}
Conductances are in siemens and states in amperes, amperes, volts.
On $[0,1]$ s this specifies 16 regular initial-value problems for each
chosen connection. Preparation of the charged state is its own interval.
For every choice, set $x=(i_1,i_2,v_o)$ and construct $A$ directly from
\eqref{eq:circuit}, adding $\dot c=-\omega s$, $\dot s=\omega c$ with
$(c,s)=(1,0)$. All seven predictions are the closed forms
$W_j=\mathcal I(Q_j,A,y_0,1)$, and both endpoint stores are specified by
\eqref{eq:L}; this is an exact finite family, not a numerical trajectory.
Changing the load or source at a finite event keeps $i,v_o$ continuous
when a current path remains. Reinitialize the source coordinates on the
correct event side and integrate the next interval separately.

A simpler probe branch displays an explicit nonzero contrast. A capacitor
$C=1$ F initially at 1 V discharges with source disconnected through
$G_L=1$ S. With no probe its receiver work at $T=1$ is
$-(1-e^{-2})/2$ J and endpoint store $e^{-2}/2$ J.
With $G_P=1$ S they become $-(1-e^{-4})/4$ J and $e^{-4}/2$ J;
the probe has its own work $-(1-e^{-4})/4$ J. These follow by separately
integrating $-G_jv^2$, $v=e^{-(G_L+G_P)t}$. The winding comparison in
\eqref{eq:crossed} still requires its magnetic states and actual source.

Moving the tapped receiver return requires another current law. Keep the
capacitor across $b$–$c$ and let $h=1$ return the receiver to $a$,
$h=0$ to $c$. With $G=G_L+G_P$, $v_L=v_b-hv_a$,
\begin{equation}
 v_a=\frac{u-R_s(i_1-i_2)+R_shGv_b}{1+R_s(G_c+hG)},\quad
 I_s=i_1-i_2+G_cv_a-hGv_L,\quad C\dot v_b=-i_2-Gv_L.
 \label{eq:return}
\end{equation}
The two winding equations use voltages $(v_a,v_b-v_a)$.
Both receivers have their own separately prepared trajectories and
$-G_Lv_L^2$ work. At $u\ne0,x=0$, return $a$ has nonzero initial receiver
power and return $c$ zero. At $u=0,x=(0,0,V)$ the return-$a$ voltage is
$V(1+R_sG_c)/(1+R_s(G_c+G))$, smaller in magnitude than $V$.
Continuity preserves each strict comparison on a finite following interval.
There is therefore no preparation-independent ordering of the two works.
Their numerical values for a specified duration remain the separate matrix
primitives, not a ratio of voltage integrals. The crossed physical load,
probe, drive and preparation comparison remains open [OP-TRF-06].

## Opening, commutation, and separate constrained limits

Physical commutation can connect two receiver branches, $G_a$ across
$b$–$a$ and $G_o$ across $b$–$c$, during overlap. Replace the last equation
of \eqref{eq:return} by
$C\dot v_b=-i_2-G_a(v_b-v_a)-G_ov_b$ and use
$v_a=[u-R_s(i_1-i_2)+R_sG_av_b]/[1+R_s(G_c+G_a)]$.
The two receiver powers are separately $-G_a(v_b-v_a)^2$ and $-G_ov_b^2$.
A finite piecewise-constant selector, with duration $1/10$ s in each
of the states $(G_a,G_o)=(1,0),(1,1),(0,1)$ S, has exact matrix
works on all three intervals. An open-gap alternative uses $(0,0)$ in
its middle interval and needs its own propagated states. Binary $h$
is not continuously interpolated to represent these connections.

![Schematic tapped receiver branches during commutation. Winding copper and core-loss elements are suppressed in this connection drawing and retained in the equations. The bridge at the capacitor crossing is not a junction. The two inductors are magnetically coupled.](figures/return-branches.pdf){#fig:returns width=76%}

\FloatBarrier

Figure \ref{fig:returns} keeps the two receiver branches distinct.
The switch/controller boundary adds $v_{\rm ctrl}i_{\rm ctrl}$,
its own electric and thermal states, and any mechanical actuation.
Actual winding opening also adds clamp, arc, and displacement-current paths;
a source command of zero with $R_s$ still connected is a different event.
As a finite clamp control, an isolated $L=1$ H inductor prepared at 2 A
drives a constant opposing clamp voltage 1 V over $[0,1]$ s.
Its law $\dot i=-1$ gives
\begin{equation}
 W_{\rm clamp}=-\int_0^1(2-t)dt=-3/2\ \mathrm J,\qquad
 E_L(0)=2\ \mathrm J,\quad E_L(1)=1/2\ \mathrm J.
 \label{eq:clamp}
\end{equation}
The clamp receiver gets $3/2$ J. Releasing at current 1 A into a declared
parallel capacitor with zero initial voltage permits a subsequent LC
interval; simply deleting that current is not a specified transfer.
A switch arc with constant voltage 2 V on the same initial inductor instead
reaches zero current in one second and receives 2 J. These are two different
finite laws, each with its own $vi$ integral and endpoint.

Singular models must be written before their finite approaches:

| Exact condition | Constrained law and prepared-state issue | Exact finite contrast |
|------------------------------|-------------------------------------------------|------------------------------------|
| $k=1$ | $q=i_1+s\rho i_2$, $L_1\dot q=v_1-R_1i_1$; $v_2-R_2i_2=s\rho(v_1-R_1i_1)$ | $L_1=\rho=1$, zero copper and $v_1=v_2=1$ give $q=t$, $E_m(1)=1/2$ J; a zero-store ideal transformer gives $0$ |
| $C=0$ | $i_2+Gv_o=0$; no independent capacitor state | $C=\epsilon$, $v_o=1$ gives $E_C=\epsilon/2$; $v_o=\epsilon^{-1/2}$ gives $1/2$ J |
| $R_s=0$ | $v_a=u$; source current follows KCL | A capacitor ramp $v=t$ has $W_s=C/2+R_sC^2$ and heat $-R_sC^2$ J on one second |
| Exact output short | $v_o=0$; nonzero prepared voltage is incompatible without an edge law | A resistor across $C=1$, $V=1$ for $R\ln2$ seconds exports $3/8$ J and leaves $1/8$ J |
| $\rho=0$ | $L_2=M=0$; winding 2 becomes $v_2=R_2i_2$, or $v_2=0$ if also $R_2=0$ | With $L_1=1$, $i_1=0$, $i_2=1/\rho$ the finite pair retains $E_m=1/2$ J |

: Configuration IV boundary models. The units of the explicit unit controls are SI. An algebraic constraint with incompatible preparation needs a named parasitic or supply path; it cannot receive an assigned impulse from this table.

For the perfect-coupling ramp, imposing $i_2=0$ gives $i_1=t$;
the separately integrated primary input is $1/2$ J and secondary input
zero. Thus the example includes its effort allocation as well as $q$.
For $C=0$ or zero turns ratio, bounded-state approaches and scaled prepared
states have different stores. These examples give no universal joint limit.

Opening an energized physical winding requires its switch, arc and clamp
laws [OP-TRF-02]. Perfect coupling, vanishing capacitance and other
constrained limits are separate models with separate admissible preparations
[OP-TRF-04].

## Ideal terminal matching and finite independent stores

Two ideal transformers with common secondary nodes $P,C$ satisfy
$V_X-V_C=h_X(V_P-V_C)$ and $j_X=-h_Xi_X$ for $X=A,B$.
KCL gives $j_A+j_B=0$ and $i_C=-(i_A+i_B)$, hence
$(i_A,i_B,i_C)=i_A(1,-R,R-1)$.
With a dimensional scale $\alpha$, the rotational mobility mapping is
\begin{equation}
 V=\alpha\omega,\qquad I=\tau/\alpha,\qquad VI=\tau\omega,
 \qquad C=J/\alpha^2.
 \label{eq:map}
\end{equation}
No factor $2\pi$ is omitted if rates were originally in revolutions per
second. The nine mechanical powers equal signed terminal products
$(V_X-\alpha\Omega)i_X$; complete winding powers instead use $V_X-V_C$.
Consequently the maximum complete-winding ratio is $\mathcal C_C$ and
that of the three external plus four winding ports is
$\max(1,\mathcal C_C)$. For $R=-341/100$ with $B$ held and observation
fixed to $A$, the mapped ratio is $341/100$ but the complete-port ratio is
one. Their exact difference is $-241/100$.
For $R=2929/2950$ with $A$ held, the winding and carrier ratios are
$2950/21$ while the ground terminal ratio is one. These compare explicitly
different observables; each corresponding signed work remains identical
under the ideal map. Constant voltage on an ideal transformer is not a
claim about indefinitely sustainable excitation of a finite core.

A dynamic circuit needs node capacitors and elastic counterparts to magnetic
states. For incidence matrix $B$, positive diagonal $\mathsf C$,
positive definite $\mathsf L$, and nonnegative $\mathsf R$, independently
specify the two models
\begin{align}
 \mathsf C\dot v&=I_{\rm ext}-Bi,&
 \mathsf L\dot i&=B^Tv-\mathsf Ri,\\
 \mathsf J\dot\omega&=\tau_{\rm ext}-Bf,&
 \dot z&=B^T\omega-\mathsf Mf,&f&=\mathsf Kz,\\
 \mathsf J&=\alpha^2\mathsf C,&
 \mathsf K&=\alpha^2\mathsf L^{-1},&\mathsf M&=\mathsf R/\alpha^2.
 \label{eq:dynamic}
\end{align}
Substitution of $v=\alpha\omega$, $i=f/\alpha$,
$z=\mathsf Li/\alpha$ proves a power-preserving correspondence for
compatible initial states and constant $\alpha\ne0$. Its inverse is
$\omega=v/\alpha$, $i=\alpha\mathsf L^{-1}z$; the same map applies
at every continuous event boundary. Singular matrices or time-dependent
scales require separate consistency and modulation-power laws.
Capacitor energy maps to inertia, magnetic
energy to elastic energy $z^T\mathsf Kz/2$, and resistor loss to
$f^T\mathsf Mf$. Each source, receiver, and loss is independently integrated
with \eqref{eq:integrator}; the stores are independently evaluated.
For a compound pair use
$\mathsf L_X=L_0\bigl(\begin{smallmatrix}h_X^2&kh_X\\kh_X&1\end{smallmatrix}\bigr)$
and incidence columns $e_A-e_C,e_P-e_C,e_B-e_C,e_P-e_C$.
A rational finite control has $L_0=1$, $k=1/2$, every retained node
capacitance one, each resistance one, zero initial state, a unit current
source at $A$, and a unit conductance receiver at $B$ over one second.
Together with any specified geometry in configuration III these coefficients
fully determine every closed matrix work. A rigid gear and a three-terminal
winding pair do not acquire these extra degrees of freedom by a voltage
rename; the dynamic correspondence is to the declared elastic model.

A physical accelerating electrical reference needs supplied compensation.
For a capacitor between $A$ and $R$, write $w=V_A-V_R$,
$C=J/\alpha^2$, $V_R=\alpha\Omega$, and
\begin{equation}
 C\dot w=I_d+I_e,\qquad I_d=\tau/\alpha,\quad I_e=-C\dot V_R,
 \qquad (P_d,P_e)=(wI_d,wI_e).
 \label{eq:reference}
\end{equation}
This realizes $w=\alpha(\omega-\Omega)$ only with compatible initial data
and its two floating-source supply ports. For $C=J=\alpha=1$, $\tau=0$,
$\Omega=2t$, zero initial states, $w=-2t$, $I_e=-2$:
$W_d=0$, $W_e=2$ J, $E_C(0)=0$, $E_C(1)=2$ J.
Disabling compensation gives $W_e=0$, $w=0$, and $E_C(1)=0$.
A common coordinate shift on the unchanged physical capacitors also leaves
their physical energy unchanged. It therefore misses the independent
relative-kinetic quantity $-\Omega H+J\Omega^2/2$.

A separate reference driver $C_d=1/200$ F, $R_d=3/4\,\Omega$ has
$I_r=C_d\dot V_R=1/100$ A and command $u_r=2t+3/400$ V.
Its independently integrated works are $W_r=403/40000$ J and heat
$-3/40000$ J, with stores $0,1/100$ J. Floating-source return currents
cancel at $R$ for this cell; their nonzero powers still require supplies.

For a finite actuator with current response time $\tau_a>0$, prescribe
$\tau_a\dot j+j=-Ca$, $C\dot w=j$, and actual actuator effort
$e=w+R_aj+L_a\dot j$, with zero initial states and $V_R=at$.
The exact solution and separate works on $[0,T]$ are
\begin{align}
 j&=-Ca(1-e^{-t/\tau_a}),&
 w&=-a[t-\tau_a(1-e^{-t/\tau_a})],\\
 W_C&=\tfrac12Ca^2[T-\tau_a(1-b)]^2,&
 Q_a&=R_aC^2a^2[T-2\tau_a(1-b)+\tfrac12\tau_a(1-b^2)],\\
 W_{a,s}&=W_C+Q_a+\tfrac12L_aC^2a^2(1-b)^2,& b&=e^{-T/\tau_a}.
 \label{eq:lag}
\end{align}
The three terms in $W_{a,s}=\int ejdt$ are obtained by integrating $wj$,
$R_aj^2$, and $L_aj\dot j$ separately. Actuator output work is $-W_C$,
heat work $-Q_a$, and its final independent store is $L_aj(T)^2/2$.
For $C=1$, $a=2$, $T=1$, $\tau_a=1/10$, $R_a=L_a=1$ in SI units,
$E_C(1)=(9+e^{-10})^2/50$ J. Its difference from 2 J is strictly negative
because $0<\tau_a(1-e^{-T/\tau_a})<T$. Separate actuator and driver
balances have zero exact residual even when their state correspondence fails.

![Exact reference-cell response from equation \eqref{eq:lag}, with $C=1$ F, $a=2$ V/s, and $\tau_a=1/10$ s. The plotted quantities are the stated closed forms, with their exact one-second endpoints.](figures/reference-response.pdf){#fig:response width=89%}

\FloatBarrier

Figure \ref{fig:response} shows the exact finite tracking departure.
Finite sensors, converter losses, command limits, and a finite rail need
additional constitutive states; their calibration is not supplied by
\eqref{eq:dynamic}. Existing bounded smooth-model correspondence and event
results do not establish unrestricted hardware duality. A nonzero reference
jump $\Delta V$ imposed in time $\delta$ through fixed $R_d,C_d>0$ has
\begin{equation}
 Q_d=R_dC_d^2\int_0^\delta\dot V_R^2dt
 \ \geq\ \frac{R_dC_d^2(\Delta V)^2}{\delta}.
 \label{eq:jump}
\end{equation}
Cauchy–Schwarz proves the bound, with equality for a linear ramp. It diverges
as $\delta\to0$ for this driver; finite slow comparisons do not realize
that event. With $L_0=\epsilon^{-1}$ and $k=1-\epsilon^2$, the pair's
common and differential magnetic eigenvalues scale differently. A prepared
common current proportional to $\sqrt\epsilon$ retains finite energy
while the current vanishes. For example $(h i_1,i_2)=(\sqrt\epsilon/2,
\sqrt\epsilon/2)$ gives $E_m=(2-\epsilon^2)/4$ J, tending to $1/2$ J.
Zero common preparation gives zero instead. Thus convergence of selected
port works or small differential voltage does not determine convergence of
all winding states and stores. Fixed-effort clamps and unchanged passive
source/load circuits are different limiting initial-value problems.

The ideal terminal map leaves physical inertial, magnetic and controller
states to be identified before claiming a loaded dynamic correspondence
[OP-TRF-09]. Complete physical-port ratios also require the actual return
and supply ports [OP-TRF-11]. The finite-reference actuator's separately
predicted departure is a bounded model result; its physical supply and
tracking accuracy remain measurable [OP-TRF-12].

# A tapped secondary with two switched receiving branches
\label{sec:switched-secondary}

Murray's SERPS Figure 11 supplies a concrete switched-return architecture:
an isolated primary, a secondary tap, and two resistor--capacitor branches
selected on opposite waveform polarities [Murray (2017)][serps].
The following finite component values are declared model choices.
Figure \ref{fig:switched-secondary} names every persistent winding section
and branch. The primary return $O$ is electrically separate from secondary
reference $B$. A selector changes an attachment; it does not discard an
energized winding section.

![Schematic of the isolated primary and two-section secondary with four selectors. The positive RC branch ends at B; the negative branch ends at A. Each switch is a finite conductance in the model, with separately supplied gate state. Winding polarities, leakage and mutual coupling are specified by the inductance matrix. The dashed magnetic connection is not a conductor between primary and secondary.](figures/switched-secondary.pdf){#fig:switched-secondary width=100%}

\FloatBarrier

The four switches connect $A-X_+$, $T-X_+$, $T-X_-$ and $B-X_-$.
Receiver resistors join $X_+$ to $Q_+$ and $X_-$ to $Q_-$.
The positive cell is $Q_+-B$ and the negative cell is $Q_--A$.
For a one-second sinusoidal drive, the nominal commands are:

| Quarter | Selected connection | Intended branch operation |
|----------------|--------------------------|----------------------------------|
| Positive rising | $A-X_+$ | Charge through full secondary |
| Positive falling | $T-X_+$ | Return through lower section |
| Negative increasing magnitude | $B-X_-$ | Charge through full secondary with opposite orientation |
| Negative falling magnitude | $T-X_-$ | Return through upper section |

: The connected state and capacitor voltage determine actual current direction; the clock alone does not establish it.

For an ideal positive charging interval,
$v_s=Ri+v_C$ and $C\dot v_C=i$.
On return, $v_C=Rj+fv_s$ and $C\dot v_C=-j$,
where $j$ enters the winding and $f$ is the tap fraction.
The condition $fv_s<v_C<v_s$ permits both directions under the
respective connections. For $R=C=1$ in SI units, a constant connected
voltage $v_s$ gives $v_C=v_s+(v_0-v_s)e^{-t}$ on $[0,T]$.
With $a_0=v_0-v_s$, separate integration gives
\begin{align}
 W_s&=-v_sa_0(1-e^{-T}),&
 Q_R&=\frac{a_0^2}{2}(1-e^{-2T}),\\
 \Delta E_C&=\frac12\{[v_s+a_0e^{-T}]^2-v_0^2\}.
 \label{eq:tap-interval-control}
\end{align}
Units are joules when the displayed constants use volts, ohms, farads and
seconds. Substitution verifies $W_s-Q_R=\Delta E_C$.
The negative branch has its own orientation and prepared voltage.
Its full and tapped connected voltages are $-v_s$ and $-(1-f)v_s$;
the positive branch uses $v_s$ and $fv_s$. For a constant selected voltage
$v_\alpha$, actual source return requires $v_\alpha(v_\alpha-v_C)<0$.
Selecting a tap does not enforce that inequality. The same exponential
solution applies separately to either sign and either fraction. For
$v_\alpha=0$, a prepared cell still heats the resistor while source work
is zero; for $v_0=v_\alpha$, all currents and works vanish.
$v_0=v_s$ gives zero current; zero preparation can instead give nonzero
charging current. Finite leakage prevents assigning an instantaneous winding
current reversal to a physical tap event.

## Persistent states and finite commutation
\label{sec:serps-finite}

Let $v=(V_A,V_T,V_{X+},V_{Q+},V_{X-},V_{Q-})$ relative to $B$.
Use three winding currents in primary, upper-secondary and lower-secondary
order, and incidence columns $B_w=(0,e_A-e_T,e_T)$.
With turns vector $N=(1,\sigma(1-f),\sigma f)$, define
\begin{equation}
 L=(1-\kappa)\operatorname{diag}(N_j^2)+\kappa NN^T,\qquad
 0<f<1,\quad 0\leq\kappa<1 ,
 \label{eq:serps-L}
\end{equation}
with unit henry scale. The tap fraction $f$ and magnetic coupling $\kappa$
are independent. Positive leakage makes $L$ positive definite.
For $f=\kappa=1/2$, $\sigma=1$,
$L=\left(\begin{smallmatrix}1&1/4&1/4\\1/4&1/4&1/8\\1/4&1/8&1/4\end{smallmatrix}\right)\mathrm H$.
Each receiving resistor is $1\,\Omega$, each cell $1/10\,\mathrm F$,
and each node has parasitic $1/50\,\mathrm F$ to $B$:
\begin{equation}
 C_n=\frac1{50}I+\frac1{10}e_{Q+}e_{Q+}^T
                  +\frac1{10}(e_{Q-}-e_A)(e_{Q-}-e_A)^T .
 \label{eq:serps-C}
\end{equation}
All selector paths have $R_{\rm on}=1/20\,\Omega$ and
$R_{\rm off}=10000\,\Omega$.
With source resistance $1/5\,\Omega$ and each winding resistance
$1/20\,\Omega$, the independent circuit equations are
\begin{equation}
 L\dot i=B_w^Tv+e_pU-R_ti,\qquad
 C_n\dot v=-B_wi-G(t)v-i_{\rm cl},\quad
 R_t=\operatorname{diag}(1/4,1/20,1/20).
 \label{eq:serps-laws}
\end{equation}
Every resistor or switch with incidence $a_j$ contributes
$g_j a_ja_j^T$ to $G$. Clamps across $A-B$, $T-B$, and each cell use
$i_{\rm cl,j}=5\,\operatorname{sgn}(w_j)\max(|w_j|-2,0)$ in amperes.
Each gate is a $1/10000\,\mathrm F$ capacitor supplied through
$20\,\Omega$. Prescribed selector commands and the gate circuit are separate
model laws; actual semiconductor coupling and actuator cost need identification.

For finite edges use $s(\xi)=3\xi^2-2\xi^3$ on $0\leq\xi\leq1$
to interpolate conductance between its off and on values.
Specify opening before closing for a gap, or closing before opening for
overlap. Each path has its own width and edge endpoints.
One initialized commutation uses $i=(1/10,1/5,-1/10)\,\mathrm A$
and $V_{Q+}=V_{Q-}=3\,\mathrm V$, with other nodes zero;
the clamp law therefore participates. The separate zero-state history
drives two one-second periods with $U=\sin(2\pi t)\,\mathrm V$,
then sets source and gates to zero and connects $1/5\,\mathrm S$
node bleeders for one second. Its actual final states remain.
Finite positive $L,C_n$ give continuous states and zero impulse at these
events, even when a commanded coefficient or power jumps.

The reactive store is $(i^TLi+v^TC_nv)/2$ plus all gate stores.
For a boundary including thermal matter $H$, source $Ui_p$ and gate-supply
products enter; receiver powers $-(V_{X+}-V_{Q+})^2$ and
$-(V_{X-}-V_{Q-})^2$ and bath $-H/2$ leave.
Copper, source resistor, selector, clamp and gate-resistor products enter
$\dot H$ as internal conversion. An electrical-only boundary instead exports
those losses and excludes $H$. Both endpoints are evaluated independently
under the chosen convention.

On a fixed linear interval the exact primitive \eqref{eq:integrator}
computes each work independently. A smooth edge uses its fundamental matrix
$\Phi(t,t_0)$, defined by
$\dot\Phi=A(t)\Phi$, $\Phi(t_0,t_0)=I$, with the forcing convolution.
The separate integral
$\int y_0^T\Phi^TQ_j(t)\Phi y_0\,dt$ defines that edge's work.
Where a clamp changes branch, its guard and event sides must also be retained.
This conditional exact formulation preserves the finite-event question
without assigning a numerical trajectory or a unique zero-width limit.
Removing leakage or parasitics imposes additional constraints and can exclude
the chosen initial state.

## A parallel/series bank is another connection graph

The patent's Figure 19 specifies a parallel/series network block without
resolving its individual cell selectors [Murray (2017)][serps]. A declared
finite realization uses cells $X_1-Y_1$ and $X_2-Y_2$, charge selector
$A-X_1$, injection selector $T-X_1$, parallel links $X_1-X_2$ and
$Y_1-Y_2$, and series link $Y_1-X_2$. Its $1\,\Omega$ receiver joins
$Y_2-B$. This receiver attachment differs from the later hidden-state
experiment's $X_1-Y_2$ attachment.

Take $C_1=1/10\,\mathrm F$, $C_2=1/10$ or $3/20\,\mathrm F$,
with the same node parasitics, finite selector resistances, windings,
clamps and gate laws as above. Command charge and both parallel links
during the first and third quarters, injection and series during the
second and fourth. The series-to-parallel return at half a second retains
the actual cell voltages. Zero preparation and a separately initialized
unequal-cell case with $(v_1,v_2)=(1,1/2)\,\mathrm V$ require their own
source, switch, receiver and endpoint expressions. Those expressions
follow from the new incidence matrices and finite-edge maps; the
initialized case supplies no preparation work by itself.

An isolated pair gives a useful exact control. For
$(C_1,C_2)=(1,2)\,\mathrm F$, initial $(v_1,v_2)=(1,0)\,\mathrm V$
and exchange resistance $1\,\Omega$,
$v_1=1/3+2e^{-3t/2}/3$ and $v_2=1/3-e^{-3t/2}/3$.
On $[0,1]\,\mathrm s$, the independent heat integral is
$(1-e^{-3})/3\,\mathrm J$ and the capacitor endpoints are
$1/2$ and $1/6+e^{-3}/3\,\mathrm J$.
Positive resistance gives continuous voltages without an impulse.
Its isolated single-path zero-resistance heat limit is unique;
several competing paths need their own partition laws.
This result does not determine the transformer-connected bank's work.

## Clocked cycles, magnetic limits, and physical service
\label{sec:periodic}

For the linear fixed-clock graph, compose interval maps to obtain
$x(T)=Mx(0)+b$. A periodic state satisfies $(I-M)x_*=b$.
Existence, uniqueness and attraction are different tests: respectively
$b\in\operatorname{range}(I-M)$, invertibility of $I-M$, and
$\rho(M)<1$. With $M=I,b=0$ every state is fixed;
$M=I,b\ne0$ has none; $M=2I$ has a unique unstable fixed state.
The remaining physical question is whether a declared clocked realization
stays within magnetic and controller limits [OP-TRF-13].

\begin{theorem}[Clocked contraction]
For the above network with inactive clamps, fixed positive-definite $L,C_n$,
strictly positive winding resistance and uniformly grounded positive
conductance, each periodic forcing and clock has one attracting periodic
electrical state.
\end{theorem}
\noindent\textit{Proof.}
The difference of two forced solutions obeys the homogeneous laws.
Multiplication by its own currents and voltages gives
$\dot E=-i^TR_ti-v^TG(t)v$.
The declared positive resistances and connected off paths imply
$\operatorname{diag}(R_t,G(t))\succeq
\eta\operatorname{diag}(L,C_n)$ for some $\eta>0$ on the compact clock
period. Hence $\dot E\leq-2\eta E$ and the period map contracts its energy
norm by at most $e^{-\eta T}<1$. The affine map has one attracting fixed
point. The same estimate covers continuous finite edges. $\square$

Gate RC states have their own affine fixed points. A thermal law
$\dot H=D(t)-H/2$ has the period relation
$H(T)=e^{-T/2}H(0)+\int_0^T e^{-(T-t)/2}D(t)\,dt$.
An insulated thermal state with positive conversion does not repeat merely
because voltages do. Repeated flux endpoints also leave continuous peak flux
and material admissibility to be checked.

A state-triggered controller needs its own map. One example switches at
$V_{Q+}=1/100\,\mathrm V$ upward and $1/200\,\mathrm V$ downward.
For a guard with normal $n$,
continuous state and vector fields $f^-,f^+$, its transverse-event variation
contains $S=I+(f^+-f^-)n^T/(n^Tf^-)$.
This formula requires $n^Tf^-\ne0$; grazing, simultaneous guards and changed
event order require separate treatment. A clocked contraction theorem
does not supply full-wave hybrid attraction.

Two material extensions illustrate the needed constitutive information.
With positive leakage $D_L$ and inductance scale $L_m=1\,\mathrm H$, let
$\lambda=D_Li+L_m\kappa I_s\tanh(N^Ti/I_s)N$.
Integrating $i^Td\lambda$ gives
\begin{equation}
 E_m=\frac12i^TD_Li+
 L_m\kappa\left[I_s q\tanh(q/I_s)-I_s^2\log\cosh(q/I_s)\right],
 \quad q=N^Ti .
 \label{eq:soft-core}
\end{equation}
Here $q$ is a current coordinate. At $I_s=1/2\,\mathrm A$, a $4\,\mathrm V$ sinusoidal drive defines
a finite amplitude comparison against the fresh linear model.
This reversible saturating law has no remanence or hysteresis state.
A separate temperature law
$R_w=(1/20)(1+H/(100\,\mathrm J))\,\Omega$, for the stated thermal scaling,
changes the trajectory through heating. Neither extension inherits the
constant-matrix theorem without a new proof.

Compare complete service only after fixing its definition: for example total
receiver heat on $[0,3]\,\mathrm s$, both zero-state preparations, source
$\sin(2\pi t)$ on $[0,2]$ and zero afterward, and the actual finite bleeder
reset. A full-secondary baseline retains both secondary sections and selects its
load on a declared descending branch of the service equation before cost
comparison. If several branches exist, their selection is part of the contract. Retain each endpoint, even if the selected service
is equal. Gross source draw and return, net source work, gate work and
useful delivery are separate integrals. A source model supplies one finite
ordering; an exact general efficiency ordering is not established by the
formulation here. Matched reset states or their explicit costs are additional
requirements for a closed-cycle comparison.

## The generator boundary
\label{sec:generator}

Enclosing the generator makes capacitor-to-generator electrical return
internal. Prime-mover shaft work, field excitation and controller supplies
remain external, with rotor, magnetic, field and thermal stores at both ends.
The physical prime-mover comparison requires the actual flux/coenergy law
and independently established motion and excitation [OP-TRF-14].

A bounded ideal converter control shows the signs. Choose
$\omega=2\pi\,\mathrm{rad/s}$, $e=\sin(2\pi t)\,\mathrm V$ and
$i=\pm\sin(2\pi t)+\tfrac12\cos(2\pi t)\,\mathrm A$
on $[0,2]\,\mathrm s$, with converter torque $ei/\omega$.
Let rotor inertia be $1/100\,\mathrm{kg\,m^2}$,
drag $D=1/1000\,\mathrm{N\,m\,s}$, and a separate unit-inductance
unit-resistance field carry $1\,\mathrm A$ under $1\,\mathrm V$.
Separate products give electrical delivery $\pm1\,\mathrm J$,
shaft input $\pm1+\pi^2/125\,\mathrm J$, field input $2\,\mathrm J$,
and drag/field heat exports $-\pi^2/125,-2\,\mathrm J$.
Rotor and field stores remain $\,\pi^2/50$ and $1/2\,\mathrm J$ at both
independently evaluated ends. The imposed reciprocal converter and
decoupled field are explicit assumptions. Their positive or negative shaft
input does not determine a physical machine's complete-cycle ordering.

Finite disconnected preparation is also explicit. A unit $RL$ field driven
by constant voltage $U$ from zero has $i=U(1-e^{-t})$,
$W_s=U^2[T-1+e^{-T}]$, resistor heat
$U^2[T-2(1-e^{-T})+(1-e^{-2T})/2]$, and store
$U^2(1-e^{-T})^2/2$. Setting its source to zero through the resistor
gives $i=i_0e^{-t}$, heat $i_0^2(1-e^{-2T})/2$ and a nonzero finite
endpoint. A rotor accelerated by constant torque $J\omega_*/T$ with
zero drag receives $J\omega_*^2/2$ by its own torque--rate integral.
These separate paths clarify what remains to be specified when actual
field and armature dynamics are coupled.

## State and observation correspondence
\label{sec:switched-correspondence}

For the fixed linear charging topology, the selected outputs
$(i_p,V_A,V_T,V_{Q+},V_{Q-}-V_A)$ and known component laws give an
observability matrix $[H;HA;\ldots;HA^8]$ of rank nine for the nine
electrical states. This can be seen directly with inactive clamps.
The measured last output and $V_A$ give $V_{Q-}$. The two cell-node laws give
\begin{equation}
 V_{X+}=V_{Q+}+\frac3{25}\dot V_{Q+},\qquad
 V_{X-}=V_{Q-}+\frac3{25}\dot V_{Q-}-\frac1{10}\dot V_A,
 \label{eq:observable-node-recovery}
\end{equation}
with the coefficients in seconds for the stated resistor and capacitance
values. All six node voltages are now known. Put $r=C_n\dot v+Gv$;
the $A,T$ node laws then give $i_u=-r_A$ and $i_l=i_u-r_T$.
These two components need only the already observed node derivatives.
Together with measured $i_p$, they recover all nine states, proving the
rank statement. This is structural reconstruction from ideal traces.
Temperature-independent elements leave $H_{\rm thermal}(0)=0$ or
$1\,\mathrm J$ electrically indistinguishable while their thermal
difference at time $T$ is $e^{-T/2}\,\mathrm J$.
A fixed-topology rank test gives neither a noise bound nor a switched
observation certificate. Individual cell and material observations still
belong to the full endpoint account. Even the nonnegative cell pairs
$(1,1)$ and $(0,2)\,\mathrm V$ share a $2\,\mathrm V$ series terminal
with unit-cell stores of $1$ and $2\,\mathrm J$.

The analogous mechanical ambiguity is already present in unit-inertia
states $(\omega_c,\omega_p)=(0,1)$ and $(10,11)\,\mathrm{rad/s}$:
their relative rate is one, but their kinetic stores are $1/2$ and
$221/2\,\mathrm J$. Absolute unwrapped motion and signed effort must
be observed together. An encoder count is $2\pi/N$ radians for $N$
counts per turn; pulse totals without reversal direction lose signed work.
For a $1\,\mathrm F$ rail at $1000\,\mathrm V$, a positive
$1/1000\,\mathrm V$ endpoint error changes the inferred energy by
$2000001/2000000\,\mathrm J$, from the exact expression
$Cv\delta v+C(\delta v)^2/2$. Small relative voltage error therefore
does not guarantee a small absolute energy error. A full low-energy rig
target of $1/100\,\mathrm J$ needs independently bounded channels,
endpoint covariance, event timing and bandwidth; it is not established
by naming the instruments.

A finite mechanical counterpart can be constructed with
$J=\alpha^2C_n$, $z=\lambda/\alpha$,
$K=\alpha^2L^{-1}$ and $i=Kz/\alpha$.
Six rotors supply node inertias; two differential flywheels supply the
capacitor terms between nodes. Three positive modal springs realize $K$.
At $\alpha=1$,
$K=\left(\begin{smallmatrix}3/2&-1&-1\\-1&6&-2\\-1&-2&6\end{smallmatrix}\right)$
and $LK=I$. Its independent equations are
$J\dot\omega=-B_wKz-G\omega-\tau_{\rm cl}$ and
$\dot z=B_w^T\omega-R_tKz+b_{\rm anchor}$.
An anchored drive supplies the primary forcing; every dashpot, gate rotor
and thermal port must map as well. Substitution proves state, power and
constitutive-store correspondence for the declared laws. The rigid
planetary train has two independent speeds, whereas this circuit has six
independent capacitive node coordinates. A bijection with that unchanged
rigid train is impossible. The added rotors, differentials, springs and
actuators are distinct physical hardware.

# Signed states and a reconnection experiment
\label{sec:signed-bank}

## Four quantities that an instrument must distinguish

An oriented charge, its absolute value, its energy and its work have
different units and different laws. Fix each capacitor's physical plate
orientation before defining $q_j=C_jv_j$. Reversing a sensor changes its
reported sign; reconnecting plates changes the incidence matrix and can
change the conserved quantities. On a fixed isolated two-cell exchange,
KCL gives $\dot q_1=-i$, $\dot q_2=i$, so $Q=q_1+q_2$ is constant.
For $C_*=C_1C_2/(C_1+C_2)$ and $d=v_1-v_2$,
\begin{equation}
 E_C=\frac{Q^2}{2(C_1+C_2)}+\frac12 C_*d^2,
 \qquad A_q=|q_1|+|q_2| .
 \label{eq:signed-quantities}
\end{equation}
Neither expression is a signed port work. With a resistor $R$,
$d=d_0e^{-t/(RC_*)}$ and its separately integrated heat is
$C_*d_0^2(1-e^{-2T/(RC_*)})/2$. The absolute charge sum is nonincreasing:
when the signs agree its derivative is zero; when they oppose,
$\dot A_q=-2|i|$ until a charge reaches zero. This sign argument depends
on the resistor law and the declared orientations.

An inductor permits a different exact result. With initial charges $(Q,0)$
and zero current,
\begin{equation}
 q_1=\frac{Q(C_1+C_2\cos\omega t)}{C_1+C_2},\quad
 q_2=\frac{QC_2(1-\cos\omega t)}{C_1+C_2},\quad
 i=\frac{QC_2\omega\sin\omega t}{C_1+C_2},\quad
 \omega^2=\frac1{LC_*}.
 \label{eq:signed-LC}
\end{equation}
For $(C_1,C_2,L)=(1,19,20/19)$ in SI units and $Q=10\,\mathrm C$,
the states at $0$ and $\pi\,\mathrm s$ are $(10,0,0)$ and $(-9,19,0)$.
Thus $Q=10\,\mathrm C$, $A_q$ grows from $10$ to $28\,\mathrm C$,
and total reactive energy is $50\,\mathrm J$ at both ends.
Integration of $-v_1i$, $v_2i$ and $Li\dot i$ separately gives
$-19/2$, $19/2$ and $0\,\mathrm J$. No external work enters this
isolated boundary. The inductor's nonzero intermediate store is essential.

A driven lossy winding has no corresponding universal winding-only linear
invariant. If $a^Ti$ were conserved for all inputs and states in
$L\dot i=bU-Ri$, it would require both $a^TL^{-1}b=0$ and
$a^TL^{-1}R=0$. Invertible positive $L,R$ force $a=0$.
At every topology change the applicable invariant must be derived anew.

## The same terminal history can hide four joules

Connect two equal cells in series through a receiver $R_L$.
For cell voltages $v_1,v_2$, set $s=v_1+v_2$ and $d=v_1-v_2$.
The common current gives
\begin{equation}
 \dot s=-\frac{2s}{R_LC},\qquad \dot d=0,\qquad
 E_C=\frac C4(s^2+d^2),\qquad
 W_L=-\frac{Cs_0^2}{4}(1-e^{-4T/(R_LC)}).
 \label{eq:hidden-series}
\end{equation}
With $C=1\,\mathrm F$, preparations $(1,1)$ and $(3,-1)\,\mathrm V$
both give $s_0=2\,\mathrm V$ and the same entire terminal history.
Their independently evaluated initial stores are $1$ and $5\,\mathrm J$;
the unobserved difference $d=0$ or $4\,\mathrm V$ retains a $4\,\mathrm J$
energy separation at every time. Preparation II contains a reversed cell.

![Two equal series cells can have the same terminal voltage and different internal energy. A later parallel connection exposes the difference mode only through its declared finite paths; the individual cell orientations remain fixed.](figures/hidden-bank.pdf){#fig:hidden-bank width=94%}

\FloatBarrier

Reconnecting corresponding plates through a finite resistance can expose
that difference mode. If a receiver and selector resistance are in series,
the receiver receives the fraction $R_L/(R_L+R_s)$ of the converted
difference energy, with finite-time factor
$1-e^{-2T/((R_L+R_s)C_*)}$. The selector receives the complementary
fraction. Residual cell energy remains at finite $T$.
This calculation specifies neither the preparation work nor the useful
delivery in a different switched graph.

## A finite switched observation map
\label{sec:binary-observation}

The bounded reconnection question concerns identification of two known
preparations by a loaded cell probe [OP-TRF-15]. The formulation below proves
a continuous precommutation bound and states the remaining separation
condition for binary discrimination. Recovering arbitrary cell signs,
energies or temperatures is a different inverse problem.

Use nodes $(A,T,X_1,Y_1,X_2,Y_2)$ relative to $B$,
unit-farad cells across $X_1-Y_1$ and $X_2-Y_2$, and
$1/50\,\mathrm F$ parasitics at every node.
A $1\,\Omega$ receiver joins $X_1-Y_2$.
Selectors join $A-X_1$, $T-X_1$, $X_1-X_2$, $Y_1-Y_2$,
$Y_1-X_2$ and the probe path $X_1-Y_1$.
Use the winding matrix \eqref{eq:serps-L} with $f=\kappa=1/2$,
each winding resistance $1/20\,\Omega$, source resistance $1/5\,\Omega$,
and zero source voltage during operation.
The five ordinary selectors have on/off resistances
$1/20$ and $10000\,\Omega$; the probe has $10$ and $10^6\,\Omega$.
Cell and terminal clamps have slope $5\,\mathrm S$ above
$4\,\mathrm V$ magnitude. Gate capacitance and resistance remain
$1/10000\,\mathrm F$ and $20\,\Omega$.

The initial node vectors are
\begin{equation}
 v^{\rm I}_0=(0,0,2,1,1,0),\qquad
 v^{\rm II}_0=(0,0,2,-1,-1,0)\quad\mathrm V .
 \label{eq:bank-preparations}
\end{equation}
Both terminal voltages $V_{X_1}-V_{Y_2}$ are $2\,\mathrm V$;
both parasitic stores are $3/50\,\mathrm J$, independently of the
$1$ or $5\,\mathrm J$ cell store. Initial winding currents are zero.
Starting with every selector off, the series conductance rises to its on
value during $[0,1/100]\,\mathrm s$, then stays on until $t=1/4\,\mathrm s$.
During the next $1/100\,\mathrm s$, conductance edges open it
and close both parallel selectors and the probe. Each edge interpolates
its two conductances with $s(\xi)=3\xi^2-2\xi^3$, $0\leq\xi\leq1$;
the charge and injection selectors stay off. All six gate voltages start
at zero and obey their independent RC laws under the corresponding unit-volt
on commands. At $t=1\,\mathrm s$,
source and gates are turned off and $1/5\,\mathrm S$ node bleeders
operate until $t=2\,\mathrm s$. All final states remain in the account.
Finite off conductance means that the two earlier terminal histories
need not agree exactly as they do in \eqref{eq:hidden-series}.

Let $x$ collect winding and node states, and append the probe filter
$\dot z=(V_{X_1}-V_{Y_1}-z)/(1/50\,\mathrm s)$ with zero initial
filter state. On each prescribed clamp branch the augmented linear or
affine equations have a fundamental matrix. Their ordered composition
defines the switched observation $z(t)=\mathcal O_t(x_0)$.
It includes the probe conductance in the physical state equations;
filtering is not a license to omit probe work.

One certificate condition can be proved without evaluating this switched
observation. In the declared node order let
$c_1=e_{X_1}-e_{Y_1}$, $c_2=e_{X_2}-e_{Y_2}$,
$\ell=e_{X_1}-e_{Y_2}$ and
$C_b=I/50+c_1c_1^T+c_2c_2^T$ in farads.
The two initial reactive stores are $53/50$ and $253/50\,\mathrm J$.
Zero source voltage and nonnegative resistive conversion imply that neither
reactive store increases, independently of retained heat or gate work.
Since $c_k^TC_b^{-1}c_k=100/101\,\mathrm F^{-1}$, both cell voltages
remain below 4 V, so their clamps are inactive. Terminal clamps, if active,
remain monotone dissipative laws.

Put $d=v^{\rm II}_0-v^{\rm I}_0=(0,0,0,-2,-2,0)^T\,\mathrm V$.
It has zero load, winding and series-link voltage. Only the finite off
paths force its departure from a constant hidden difference before
$t_c=1/4\,\mathrm s$. If $G$ is the prestage nodal conductance,
$b_d=Gd$ is constant even while the series link closes.
For the error $w=(i^{\rm II}-i^{\rm I},v^{\rm II}-v^{\rm I}-d)$
between trajectory II and trajectory I translated by $d$, use
$\|w\|_{L,C_b}^2=w_i^TLw_i+w_v^TC_bw_v$.
The translated cells have magnitude below $3/2+2<4$ V, because trajectory
I's reactive store is at most $53/50\,\mathrm J$. The translated terminal
clamps are unchanged. Incremental dissipation and Cauchy--Schwarz therefore
give the norm bound $t\sqrt{b_d^TC_b^{-1}b_d}$ from zero initial difference.
Consequently
\begin{equation}
 \sup_{0\leq t\leq t_c}|\ell^T(v^{\rm II}-v^{\rm I})|
 \leq\frac{\sqrt{1030251}}{2020000}\,\mathrm V
 <\frac1{1000}\,\mathrm V<\frac1{10}\,\mathrm V .
 \label{eq:bank-preterminal-bound}
\end{equation}
To check the constant, direct inversion gives
\begin{align}
 \ell^TC_b^{-1}\ell&=\frac{5100}{101}\,\mathrm F^{-1},\\
 b_d^TC_b^{-1}b_d&=\frac{20201}{252500000000}\,\mathrm{J/s^2}.
 \label{eq:bank-bound-constants}
\end{align}
Multiply their product by $t_c^2$. This covers every prestage time and
both sides of its finite edge, without selecting clamp events from observations.

For an exact conditional certificate, calculate
$z_j=\mathcal O_{7/20}(x_0^j)$ and form the two uncertainty intervals
$I_j=[z_j-u_z,z_j+u_z]$, $u_z=1/20\,\mathrm V$.
If $|z_{\rm II}-z_{\rm I}|>2u_z$ and the precommutation terminal
difference is bounded by $1/10\,\mathrm V$ throughout its window,
these readings distinguish the two specified preparations.
Since the two candidate cell energies are known exactly, correct binary
classification meets a $1/100\,\mathrm J$ energy target in the
exact-coefficient model. Equation \eqref{eq:bank-preterminal-bound} proves
the preterminal requirement. The postconnection separation inequality is
not evaluated here. For the unshifted difference
$\delta i=i^{\rm II}-i^{\rm I}$, $\delta v=v^{\rm II}-v^{\rm I}$,
the quadratic form $D=(\delta i^TL\delta i+\delta v^TC_b\delta v)/2$
is nonincreasing and $D(0)=102/25\,\mathrm J$, hence
$|\delta(V_{X_1}-V_{Y_1})|\leq\sqrt{816/101}\,\mathrm V$.
The positive filter kernel bounds
$|\delta z(7/20)|\leq\sqrt{816/101}(1-e^{-35/2})\,\mathrm V$;
this upper bound supplies no positive lower separation. The finite
discrimination result therefore remains conditional on the stated inequality.
Physical acquisition must bound component drift, probe loading, gain,
bandwidth, polarity, timing and preparation uncertainty before adopting
these decision intervals. Unknown analog preparations require a new
uncertainty analysis rather than a two-label classifier.

## Paired work includes the chargers and the retained states
\label{sec:paired-bank-work}

The same receiver and clock define a bounded paired-work comparison
[OP-TRF-16]. More prepared energy alone fixes no sign for the difference
of that receiver's work. The work is determined by the loaded trajectory
and every connected conversion path.

Preparation is physical. Disconnect windings and selectors and charge the
six-node capacitance matrix $C_b$ from zero during $[-1,0]\,\mathrm s$
using six independent $1\,\Omega$ Thevenin sources.
For constant source vector $u$, $C_b\dot v=u-v$, whence
$v(0)=(I-e^{-C_b^{-1}})u$.
The positive matrix $C_b$ makes the charge map invertible, so each vector
in \eqref{eq:bank-preparations} has its own specified finite $u$.
Each source work is $\int u_j(u_j-v_j)dt$;
each resistor exports $-\int(u_j-v_j)^2dt$.
The endpoint is independently $v(0)^TC_bv(0)/2$.

During operation evaluate separately, for each preparation,
\begin{equation}
 W_L^j=-\int_0^2(V_{X_1}^j-V_{Y_2}^j)^2dt,\qquad
 W_{\rm probe}^j=-\int_0^2g_{\rm probe}(t)
                   (V_{X_1}^j-V_{Y_1}^j)^2dt .
 \label{eq:paired-bank-works}
\end{equation}
Source, selector, clamp, gate and bath products have their own integrals.
With thermal matter retained, all internal resistive conversions enter
$\dot H=D-H/2$; the bath work is $-\int H/2\,dt$.
The total endpoint includes winding, cell, parasitic, gate and thermal
stores. For each event retain the same continuous state on both sides
and both one-sided powers. Finite positive parameters give zero impulse.

On linear intervals the independent quadratic primitive
\eqref{eq:integrator} evaluates these works; finite edges use their
ordered fundamental matrix and separate quadratic integrals.
Those expressions define the work difference; its sign has not been
evaluated here. For each source-free reactive boundary, its independently
derived dissipative identity bounds the receiver export by its own initial
store. Thus $-53/50\leq W_L^{\rm I}\leq0$ J and
$-253/50\leq W_L^{\rm II}\leq0$ J, so
$-253/50\leq W_L^{\rm II}-W_L^{\rm I}\leq53/50$ J.
This rigorous enclosure contains both signs and determines no ordering.
The $4\,\mathrm J$ cell difference supplies no narrower sign conclusion.
A physical ordering comparison requires a separated prediction and a smaller
combined uncertainty, with actual reset endpoints retained. Equal useful
service and a closed-cycle generator ranking require additional comparisons.

## An all-time sign and magnitude certificate
\label{sec:sign-certificate}

A finite topology change can be treated without inferring sign events
from sampled states. Retain the LC path in \eqref{eq:signed-LC} with
$(C_1,C_2,L)=(1,19,20/19)$ and add a $1\,\Omega$ shunt across cell 1
only on $[a,b]=[\pi/2,\pi/2+1/10]\,\mathrm s$.
On the full window $[0,2]\,\mathrm s$, write its conductance as $g=0$
or $1\,\mathrm S$. The equations and independent energy are
\begin{equation}
 \dot q_1=-i-gq_1,\quad \dot q_2=i,\quad
 \dot i=\frac{19q_1-q_2}{20},\qquad
 E=\frac{q_1^2}{2}+\frac{q_2^2}{38}+\frac{10i^2}{19}.
 \label{eq:shunted-LC}
\end{equation}
Here $\dot E=-gq_1^2$ and $\dot Q=-gq_1$.
The old conserved charge is therefore not conserved during the shunt.
For initial state $(10,0,0)$, Cauchy--Schwarz gives, at every time,
$A_q^2\leq40E_C\leq40E\leq2000\,\mathrm C^2$.
The identically zero initial state remains zero. This is a conservative
bound for these preparations and components, not a universal multiplier.

Before $a$, \eqref{eq:signed-LC} gives
$(q_1,q_2,i)(a)=(1/2,19/2,19/2)$ in SI units.
$q_2=0$ has its initial tangency at $t=0$; both charges are positive
on $(0,a]$. Energy bounds give $|i|<10$ and $|q_2|<44$.
On the shunt interval, putting $\tau=t-a$, the integrating-factor
solution of $\dot q_1+q_1=-i$ gives
$|q_1|\leq1/2+10\tau\leq3/2$.
Also $17/2\leq q_2\leq21/2$ and
$|\dot i|\leq39/20$, hence $i\geq1861/200>9$.
Thus $\dot q_1<0$ throughout this interval.
While $q_1\geq0$, it satisfies $-21/2<\dot q_1\leq-9$.
Consequently its unique zero obeys
\begin{equation}
 \frac{\pi}{2}+\frac1{21}<t_*<\frac{\pi}{2}+\frac1{16}.
 \label{eq:certified-charge-zero}
\end{equation}
Before that zero $\dot A_q=-q_1<0$; after it,
$\dot A_q=2i+q_1>0$. The zero is a magnitude cusp with distinct
one-sided derivatives, not a differentiable minimum.

After $b$, the energy bound also gives $|q_1|\leq10$ and
$|\dot i|<117/10$.
Since $2-b<2/5$, $i>1861/200-117/25=37/8>0$ to the final time.
Therefore $q_1$ stays negative, $q_2$ stays positive, and there are no
further charge zeros. At $a,b$ states are continuous; the appropriate
one-sided vector fields give the switched derivatives.
This covers every time, both preparations, the tangency, persistent zeros,
single crossing, cusp and both switch sides.

The independent shunt work is $W_h=-\int_a^bq_1^2dt$.
On each constant-$g$ interval set $x=(q_1,q_2,i)^T$ and
$x(t)=e^{A_g(t-t_0)}x(t_0)$ from \eqref{eq:shunted-LC}; the quadratic
primitive evaluates $W_h$ separately from the two endpoint energies.
Multiplying the three independent equations verifies their equality
$E(2)-E(0)=W_h$. If the resistor is enclosed, its heat store replaces
that export and total retained energy is constant. The finite shunt
interval does not specify an actual switch's ignition, parasitic or
sensor law.


# Other prepared states and switching paths

## A passive two-store circuit has several different limits

Configuration V first uses a parallel $R_C,C$ section in series with a
parallel $R_L,L$ section. Its terminal impedance is
\begin{equation}
 Z(s)=\frac{R_C}{1+sR_CC}+\frac{sLR_L}{R_L+sL}.
 \label{eq:two-store}
\end{equation}
KCL in each section and KVL in their series connection derive this formula.
At $s=1\,\mathrm{s}^{-1}$ with untargeted components equal to one in SI
units, $C=\epsilon$, $R_C=1$ gives $Z=1/(1+\epsilon)+1/2$;
$C=R_C=\epsilon$ in their respective units gives
$Z=\epsilon/(1+\epsilon^2)+1/2$.
At $\epsilon=1/10$ these are $31/22$ and $121/202\,\Omega$;
the limits are $3/2$ and $1/2\,\Omega$. This Laplace-domain comparison
is a terminal-law statement, not a work measurement or a physical component
with infinite or zero value.

The exact zero/infinite topologies have distinct hypotheses. A zero capacitor
removes its capacitive branch, retaining $R_C$; infinite capacitance constrains
its voltage to a constant only for bounded current and a declared prepared
voltage. A zero inductor enforces zero branch voltage, while infinite
inductance constrains current for bounded voltage. Zero resistance shorts
its section; infinite resistance removes that resistor. Incompatible
prepared charge or flux needs a physical regularization, not substitution
into \eqref{eq:two-store}.

Close the terminal by a zero-voltage source, retaining finite positive
components. For capacitor voltage $v$ and inductor current $i$, KCL gives
\begin{equation}
 C\dot v=-(R_C^{-1}+R_L^{-1})v+i,\qquad L\dot i=-v,
 \quad E=\tfrac12Cv^2+\tfrac12Li^2.
 \label{eq:prepared-two-store}
\end{equation}
The complete store boundary excludes the two thermal reservoirs and the
terminal source. Its powers are $0$, $-v^2/R_C$, and $-v^2/R_L$.
For $C=L=R_C=R_L=1$, prepared $(v,i)=(1,0)$ gives
$v=(1-t)e^{-t}$, $i=-te^{-t}$. On $[0,1]$ s,
\begin{equation}
 W_C^{h}=W_L^{h}=-\frac{1-e^{-2}}4\ \mathrm J,\quad
 E(0)=\frac12\ \mathrm J,\quad E(1)=\frac{e^{-2}}2\ \mathrm J.
 \label{eq:prepared-works}
\end{equation}
The sum of absolute physical heat works is $(1-e^{-2})/2$ J;
the zero-state control gives zero for every work and store. This prepared
experiment retains the original two-section topology. Other nondimensional
coscalings require their own positive component paths, compatible endpoints,
and individually resolved source and heat works.

Two explicitly different clamp regularizations illustrate why zero-state
transfer functions do not fix prepared switching work. A unit capacitor
at 1 V discharged through resistance $R=\epsilon$ for
$T=\epsilon\ln2$ exports $3/8$ J and retains $1/8$ J.
A lossless auxiliary inductor $L=\epsilon^2$ attached instead gives
$v=\cos(t/\epsilon)$, $i=\sin(t/\epsilon)/\epsilon$.
At $T=\pi\epsilon/2$ capacitor energy is zero, inductor energy $1/2$ J,
and each capacitor/inductor interface work is respectively $-1/2,+1/2$ J;
external heat work is zero. Both follow exact finite equations and the two
endpoint laws. Neither is the unique instantaneous fate of the initial
charge. The finite component and time choices, their peak currents, and
all additional switch or clamp paths remain part of the experimental claim.

These finite paths do not select a unique prepared singular limit
[OP-LR21-01]. Smooth zero-state forcing also leaves the work of an actual
prepared-state switch unspecified [OP-LR21-02].

## Hidden prepared energy and its observability

A transformer-coupled series $R,C$ branch in parallel with $G_0$ has
\begin{equation}
 Y(s)=G_0+\frac{n^2sC}{1+sRC},\qquad
 v_C(t)=V_0e^{-t/(RC)},\qquad
 I_{\rm terminal}(t)=-\frac{nV_0}{R}e^{-t/(RC)}
 \label{eq:hidden}
\end{equation}
on a zero-voltage terminal preparation release, with the indicated current
positive into the passive input. The internal resistor current has magnitude
$|V_0|e^{-t/(RC)}/R$. At $n=0$ the transformer is interpreted as the
decoupled boundary topology, not an invertible zero-ratio transformer.
There is no terminal hidden-mode current, but $E_C=CV_0^2e^{-2t/(RC)}/2$.

Choose $C=1/1000000$ F, $R=100\,\Omega$, $V_0=1$ V,
$T=RC\ln2=\ln2/10000$ s. The source work is zero, initial store
$1/2000000$ J, final store $1/8000000$ J, and heat work
$-3/8000000$ J by direct integration of $-v_C^2/R$.
An empty mode predicts zero internal current and zero heat; a prepared hidden
mode predicts initial internal current $1/100$ A and the stated heat.
A branch voltage/current observation resolves the difference even when the
terminal observation cannot. Calorimetric resolution at that energy would
need its own demonstrated uncertainty; branch electrical measurement avoids
presuming it.

For a known single nonzero $n$, a certified terminal current bound $u_I$ at
release implies
\begin{equation}
 |V_0|\leq Ru_I/|n|,\qquad E_C(0)\leq\frac{CR^2u_I^2}{2n^2}.
 \label{eq:hidden-bound}
\end{equation}
For $n=1/100$, $u_I=1/1000000$ A, and the preceding $R,C$, this upper
bound is $1/20000000000$ J. It grows without bound as sensitivity $n$
approaches zero. Known gain, loading, and bandwidth are hypotheses of the
bound. A noisy or nonideal transformer requires their independently bounded
transfer law and additional stores.

Multiple modes introduce a further obstruction: two equal $R,C,n$ branches
prepared at $+V,-V$ have cancelling terminal release currents but total
energy $CV^2>0$. With the preceding $C,R,n$ and $V=1$ V this is
$1/1000000$ J, exceeding the single-mode bound despite exact terminal
cancellation. All their initial opposite branch currents are observable
separately. More generally, if boundary observations are $y(t)=He^{At}x_0$,
an energy bound from them exists on a preparation subspace only if no
nonzero energy-bearing direction lies in its observation nullspace, with
a quantitatively bounded inverse on the retained subspace. Internal branch
measurements remove this nullspace in the two-mode example. More modes,
nearly coincident time constants, nonideal couplings, and correlated noise
require their own finite observability and error bounds; a single terminal
noise threshold cannot establish them.

Near-cancelled or unobserved modes require branch-state observations with
their own uncertainty [OP-LR23-01]. Exact decoupling leaves prepared
hidden energy and any later reconnection as separate physical questions
[OP-LR23-02].

## Common current is a physical preparation

Take two lossless inductors $L_1=1$ H, $L_2=19$ H connected through a
capacitor $C=20/19$ F. The oriented equations are
$L_1\dot i_1=-v$, $L_2\dot i_2=v$, $C\dot v=i_1-i_2$.
For initial $(i_1,i_2,v)=(10+u,u,0)$, define
$c=i_1+19i_2=10+20u$ and $d=i_1-i_2=10\cos t$. Then
\begin{equation}
 i_1=\frac{c+19d}{20},\quad i_2=\frac{c-d}{20},\quad
 v=\frac{19}{2}\sin t,\quad
 E=\frac{c^2}{40}+\frac{19d^2}{40}+\frac{Cv^2}{2}
 =50+10u+10u^2\ \mathrm J.
 \label{eq:common}
\end{equation}
The equality follows by substitution of the state, not an assumed constant
store. The operating boundary has no external ports; the capacitor and two
coil works integrate separately as changes of their explicit quadratics.
On $[0,\pi]$ s, $(W_1,W_2,W_C)=(-19c/20,+19c/20,0)$ J, so their sum
is zero. For $u=0$, this pair is $(-19/2,+19/2)$ J; for $u=-1/2$ it
is $(0,0)$; for $u=-1$ it is $(+19/2,-19/2)$.

For actual preparation, disconnect the operating capacitor and independently
ramp both coil currents from zero as $i_1=(10+u)t$, $i_2=ut$ on
$[0,1]$ s. With ideal lossless windings the two imposed source voltages are
$10+u$ and $19u$ V. Their independently integrated works are
$(10+u)^2/2$ and $19u^2/2$ J. Add winding resistance $R_j$ and each source
work additionally contains $R_jI_{j*}^2/3$, with separate negative heat work
of that magnitude. A reversed controlled ramp supplies the explicit reset;
passive relaxation is another path.

Over $-1\leq u\leq1/2$, completing the square gives
$E=95/2+10(u+1/2)^2$ J, hence the stated range $[95/2,115/2]$ J.
At $u=0$ initial fluxes are $(10,0)$ Wb and final fluxes $(-9,19)$ Wb;
at $u=-1/2$ they are $(19/2,-19/2)$ and $(-19/2,19/2)$ Wb.
Thus physical sign changes and absolute sums vary with preparation while
the differential trajectory is the same. A differential pickup that rejects
$c$ sees the same drive but retains its own backaction, load, and stores;
its full coupled model is needed for the loaded comparison. Translating a
reported flux origin alone changes none of the preparation works above.

The common-current preparation and pickup backaction therefore need their
own source and load measurements [OP-LR42-02].

## Commuting endpoints with noncommuting work partitions

Two capacitors $C_1,C_2$ exchange charge through one of two finite conducting
channels $A,B$. The store boundary contains both capacitors; the active
channel's heat reservoir is external. With $d=v_1-v_2$,
$\bar v=(C_1v_1+C_2v_2)/(C_1+C_2)$, and
$C_e=C_1C_2/(C_1+C_2)$, KCL gives
\begin{equation}
 \dot d=-\frac{G}{C_e}d,\quad \dot{\bar v}=0,\quad
 E=\tfrac12(C_1+C_2)\bar v^2+\tfrac12C_ed^2,\quad
 W_h=-\int_0^T Gd^2dt=-\tfrac12C_ed_0^2(1-e^{-2GT/C_e}).
 \label{eq:sharing}
\end{equation}
Each stage is a finite $d\mapsto d/2$ map when $T=C_e\ln2/G$.
The two maps commute. Their heat integrals retain the incoming $d$ and
therefore the stage order.

For $C_1=C_2=2$ F, $(v_1,v_2)=(1,0)$ V, $G_A=G_B=1$ S,
each stage lasts $\ln2$ s. Independently evaluated total stores are
$1$, $5/8$, and $17/32$ J before, between, and after the stages.
Final voltages are $(5/8,3/8)$ V in both orders.

| Channel work into capacitor boundary, J | $A$ then $B$ | $B$ then $A$ |
|----------------------------------------|-----------------------:|-----------------------:|
| $W_A$ | $-3/8$ | $-3/32$ |
| $W_B$ | $-3/32$ | $-3/8$ |
| Total work | $-15/32$ | $-15/32$ |
| Final store | $17/32$ | $17/32$ |

: Equal endpoints do not determine the channel partition. Both controls have zero residual and no impulse at either finite switching edge.

![Exact excess-energy decay during two finite charge-sharing stages. The continuous state is the same for both orders, while the channel receiving the larger heat transfer changes. The plotted curve is equation \eqref{eq:sharing}.](figures/charge-sharing.pdf){#fig:sharing width=89%}

\FloatBarrier

Figure \ref{fig:sharing} separates the unchanged state curve from the changed
heat recipient. Unequal-capacitance controls retain the common store. With $(C_1,C_2)=(1,2)$ F,
$C_e=2/3$ F, the same voltage preparation and half-difference maps give
channel works $-1/4,-1/16$ J and endpoints $1/2,3/16$ J.
With $(C_1,C_2)=(2,1)$ F those works agree but endpoints are $1,11/16$ J.
Changing preparation to $(1,-1)$ V in the equal-capacitance case multiplies
the excess store and both channel works by four, with common store zero.
Thus orientation and capacitance ratios must accompany a work claim.

Actual arc ignition, restrike, clamp release, winding capacitance, and
switch supply laws are not determined by \eqref{eq:sharing}. A finite
released winding/capacitor model can instead be written as
$L\dot i=-v$, $C_p\dot v=i-\sum_lG_l(v,t)v$ with branch powers
$-G_l(v,t)v^2$. Each proposed switch, arc, and clamp law is a separate
$G_l$, with its own heat or receiver destination. Constant positive
coefficients give exact matrix primitives; specified threshold switching
uses event-side states and separate intervals. A constant-current or
constant-voltage clamp uses its actual effort–flow law instead of this
conductance representation.

For a connected perfectly coupled pair with
$\mathsf L=aa^T$, $a=(\sqrt{L_1},\sqrt{L_2})$, and capacitor incidence
$b=(1,-1)^T$, the equations
$\mathsf L\dot i=bv$, $C\dot v=-b^Ti$ impose
$n^Tb\,v=0$ for $n=(-\sqrt{L_2},\sqrt{L_1})$.
At $L_2/L_1=19$ this requires $v=0$ and $i_1=i_2$ on a smooth solution.
The prepared state $(10,0,0)$ is incompatible; a putative terminal voltage
impulse also has $n^Tb\int vdt=0$ and cannot select the null-current jump.
Named parasitic paths can select finite releases, but different paths retain
their different works. Other orientations require their own nullspace
calculation.

Finite values $C_p=1/100,1/1000,1/10000$ F and durations
$1/50,1/200$ s are separate realizable comparisons, conditional on their
bandwidth and current envelopes. For explicit wider ratios, retain
$(v_1,v_2)=(1,0)$ V and both half-difference stages, but use
$(C_1,C_2)=(1/2000,1)$ F or $(1,1/2000)$ F. The final stores are
respectively $21/1334000$ and $10667/21344$ J; both export $5/21344$ J
in total, from initial stores $1/4000$ and $1/2$ J. Each stage lasts
$\ln2/2001$ s at conductance 1 S. These finite ratios $1/2000$ and $2000$
probe beyond the preceding range, conditional on their own measurement
bounds; they do not certify a continuous limiting surface.
At fixed prepared voltage, $C_p\to0$
removes energy; at fixed nonzero charge, $E=q^2/(2C_p)$ diverges.
At fixed $R,C$ a prescribed voltage jump obeys \eqref{eq:jump}; an RC
charge-sharing path instead has finite limiting conversion but unbounded
peak current as resistance vanishes. The exact zero-time and zero-component
models remain mathematical questions separate from these finite tests.

Actual release, ignition, restrike and parasitic paths need independently
identified laws before their channel partition is known [OP-LR48-03].
Finite ratios and finite edges test specified approaches, while other
orientations and continuous limiting surfaces remain unproved
[OP-LR48-05].

## Different connections need not commute
\label{sec:three-store-reset}

Another scalar control has two independent $1\,\mathrm F$ cells initially
at $(1,-1)\,\mathrm V$. Each selectable channel contains a separate
$1\,\Omega$ shunt across each cell, so its two laws are $\dot v_j=-v_j$.
Operating a channel for $\log2\,\mathrm s$ halves both voltages.
Two successive channels therefore end at $(1/4,-1/4)\,\mathrm V$ and
$1/16\,\mathrm J$ from an initial $1\,\mathrm J$.
The independent two-resistor integrals give heats $3/4$ then $3/16\,\mathrm J$;
reversing the channel order interchanges their recipients. These are
shunts across individual cells; the earlier exchange resistor instead has
time constant $C_e/G$. Stating the connections prevents a factor-of-two
ambiguity in the duration of a half-difference map.

The scalar difference-mode maps above commute. With three stores a
connection change can alter the final state as well as the recipient
of heat. Take three $1\,\mathrm F$ cells with initial charges
$q=(1,0,-1)^T\,\mathrm C$.
Channel $A$ joins cells 1 and 2 through $1\,\Omega$; channel $B$
joins 2 and 3. Each operates for $(\log2)/2\,\mathrm s$.
For incidence $a$, KCL is $\dot q=-aa^Tq$ and its heat is
$\int(a^Tq)^2dt$. The two exact maps are
\begin{equation}
 M_A=\begin{pmatrix}3/4&1/4&0\\1/4&3/4&0\\0&0&1\end{pmatrix},\qquad
 M_B=\begin{pmatrix}1&0&0\\0&3/4&1/4\\0&1/4&3/4\end{pmatrix}.
 \label{eq:three-reset-maps}
\end{equation}
Their ordered products and separately integrated channel heats give:

| Order | Final charges, C | Heat in $A$, J | Heat in $B$, J |
|----------------|---------------------------|----------------|----------------|
| $A$ then $B$ | $(3/4,-1/16,-11/16)$ | $3/16$ | $75/256$ |
| $B$ then $A$ | $(11/16,1/16,-3/4)$ | $75/256$ | $3/16$ |

: Each final store is $133/256\,\mathrm J$, evaluated from $q^Tq/2$; each total heat is $123/256\,\mathrm J$, from an initial $1\,\mathrm J$.

Indeed $M_BM_A-M_AM_B\ne0$.
Equal energy here follows from the symmetric preparation; it does not
restore equal final state. Finite resistor maps do not reset the cells
exactly to zero. This bounded noncommuting extension leaves the physical
partition under other connections and switch laws open [OP-LR48-02].

## A damped electrical and mechanical preparation
\label{sec:damped-correspondence}

A reciprocal port map extends beyond lossless oscillators.
For a series circuit $\dot q=i$, $L\dot i=V-q/C-Ri$ and
a mass--spring--dashpot $\dot x=v$, $m\dot v=F-kx-bv$, set
\begin{equation}
 q=\beta x,\quad i=\beta v,\quad V=F/\beta,\quad
 L=m/\beta^2,\quad 1/C=k/\beta^2,\quad R=b/\beta^2.
 \label{eq:damped-map}
\end{equation}
Then $Vi=Fv$, $Ri^2=bv^2$, $q^2/(2C)=kx^2/2$ and
$Li^2/2=mv^2/2$. Substitution proves the state and port correspondence
without assigning a balance residual as a missing work.
Actual collision/contact laws and a manufactured realization remain
unidentified [OP-LR50-01].

For $L=C=m=k=1$, $R=b=1/5$ and $\beta=1$ in SI units,
start at zero and apply effort $+1$ on $[0,1]$, $0$ on $[1,2]$,
then $-1$ on $[2,3]\,\mathrm s$.
The common state matrix is
$A=\left(\begin{smallmatrix}0&1\\-1&-1/5\end{smallmatrix}\right)$.
On each interval the exact forced exponential determines its endpoint;
the independent integrals $\int ui\,dt$ and $-\int i^2/5\,dt$
are given by \eqref{eq:integrator} after adjoining a constant state.
The two physical models therefore have identical signed works and
stores on each finite interval. The third endpoint is retained;
opposite drive is not an assumed exact reset.

A physical common-motion preparation also has a source.
Over $t\in[-1,0]\,\mathrm s$, put $s=t+1$ and prescribe
$x=(3/10)(s^3-s^2)\,\mathrm m$, $v=\dot x$,
$F=\ddot x+\dot x/5+x$ in the same unit model.
Integration of the force and dashpot products gives
\begin{equation}
 W_F=\frac{237}{5000}\,\mathrm J,\qquad
 W_b=-\frac3{1250}\,\mathrm J,\qquad
 E(-1)=0,\quad E(0)=\frac9{200}\,\mathrm J .
 \label{eq:physical-common-preparation}
\end{equation}
The endpoints $(x,v)=(0,0),(0,3/10)$ are evaluated independently.
Changing an observer coordinate alone performs none of this preparation.

# A shared output, supplied timing and finite observation
\label{sec:shared-fixture}

Multiple switched branches can deliver to one magnetic receiver, but their
currents must solve the newly connected circuit. The following model keeps
six isolated input cores and a seventh output core. Each input channel has
two polarity branches; all twelve branch windings and one output winding
share the output core. This is a declared extension of the switched-return
concept in Murray's patent [Murray (2017)][serps]. Its six-channel topology,
finite values and supplied controls are specified here. The patent's output
combination examples do not identify this graph or its material laws.

| Question | Proved result | Defining restriction |
|--------------------------------|----------------------------------------------|-------------------------------------------|
| Simultaneous return and delivery | Continuous component and work margins | Prepared 5 ms transition; initially energized output |
| Repetition of the supplied assembly | Positive thermal increment prevents full-state return | Insulation and one timing revolution in the specified period range |
| Accuracy of inferred initial energy | Exact $1/100$ J worst-case error on two states | Loaded 10 s probes, a 5 ms window and $1/10$ A per-trace error |

: Three separate questions. The fixed electrical fixture and the supplied-machine extension have different boundaries and state spaces.

## The complete finite electrical fixture

For $j=1,\ldots,6$, the primary reference $O_j$, secondary reference $B_j$,
four gate references $D_{jk}$ and receiver reference $B_o$ are physically
separate. A reference elimination in the equations does not bond them.
There is no postulated chassis or interwinding capacitance. Those additional
physical paths would change the model. Figure \ref{fig:shared-output}
defines the main connections; the following tables include every remaining
electrical path.

![Schematic of one indexed channel and the shared output. Instantiate the channel six times with separate primary and secondary returns. Both branch windings in every channel couple to the single output core; dashed magnetic connections are not conductors. $U_j^{\rm w}$ and $D_j^{\rm w}$ label the upper and lower secondary windings. Dots and arrows specify persistent winding orientations. The component tables specify every finite selector, gate, clamp, parasitic, bleeder and loaded probe omitted from the main paths.](figures/shared-output.pdf){#fig:shared-output width=100%}

Let $p_j$ be primary-node voltage relative to $O_j$ and
$(A_j,T_j,X_{+j},Q_{+j},X_{-j},Q_{-j})$ the six secondary voltages
relative to $B_j$. Winding currents are positive along the following
ordered terminal pairs. The negative cell keeps voltage $Q_{-j}-A_j$
throughout; its physical orientation is not changed by a selector.

| Element | Ordered terminals or connection | Declared value |
|---------------------|--------------------------------------|--------------------------|
| Primary, upper and lower windings | $p_j-O_j$, $A_j-T_j$, $T_j-B_j$ | Copper $1\,\Omega$ each |
| Two output-core branch windings | $X_{+j}-Q_{+j}$, $X_{-j}-Q_{-j}$ | Copper $1\,\Omega$ each |
| Four selectors | $A_j-X_{+j}$, $T_j-X_{+j}$, $T_j-X_{-j}$, $B_j-X_{-j}$ | Conductance $g_{jk}$ below |
| Positive and negative cells | $Q_{+j}-B_j$, $Q_{-j}-A_j$ | $1\,\mathrm F$ each |
| Secondary parasitics and bleeders | Each of the six secondary nodes to $B_j$ | $1\,\mathrm F$ and $1/10\,\mathrm S$ each |
| Source and its resistor | $U_j$ relative to $O_j$, through $R_s$ to $p_j$ | $U_j=1\,\mathrm V$, $R_s=1\,\Omega$ |
| Primary-node capacitor | $p_j-O_j$ | $1\,\mathrm F$ |
| Four secondary clamps | Across $A_j-B_j$, $T_j-B_j$ and each cell | Threshold $5\,\mathrm V$, slope $1\,\mathrm S$ |
| Each independent gate | Command $c_{jk}$ through $R_g$ to $z_{jk}$, capacitor to $D_{jk}$ | $R_g=1\,\Omega$, $C_g=1/1000\,\mathrm F$ |

: One channel's complete paths, repeated with separate returns.

The output winding is oriented $v_o-B_o$, with current $i_o$ into its
positive terminal and copper $1\,\Omega$. A $1\,\Omega$ receiver,
$1\,\mathrm F$ capacitor and the same clamp law each join $v_o$ to $B_o$.
Seven physical probes load $p_1,\ldots,p_6,v_o$: a $10\,\Omega$ resistor
joins each node to a probe node $y_j$ or $y_o$, with $1\,\mathrm F$
from that probe node to the corresponding local return. There is no probe
supply. Each probe has its own resistor heat and capacitor store.

\FloatBarrier

Order currents as six primary/upper/lower triples, then the twelve branch
currents, then $i_o$. Let $n=(1,1/2,1/2)^T$ and $s=\mathbf1_{13}$.
The inductance blocks and joint magnetic store are
\begin{equation}
 L_j=(I_3+nn^T/4)\,\mathrm H,\qquad
 L_o=(I_{13}+ss^T/4)\,\mathrm H,\qquad
 L=\operatorname{diag}(L_1,\ldots,L_6,L_o),\quad E_m=\tfrac12i^TLi.
 \label{eq:shared-inductance}
\end{equation}
Each core has positive unit leakage and positive common inverse reluctance;
the fractional entries describe effective turn ratios. This construction
proves positivity within a lumped model, not a manufactured geometry or
material rating. The input tap fraction $1/2$ is separate from its coupling.
There are 31 persistent winding currents.

Order the 50 voltage coordinates as the six secondary sextuples, six
primary nodes, $v_o$, six source probes and the output probe. Let $e_a$
select a named node and let $a_e=e_a-e_b$ select an oriented terminal pair,
with the eliminated local return represented by zero. Each physical
capacitor contributes $C_ea_ea_e^T$. Thus
\begin{equation}
 C=\left[I_{50}+\sum_{j=1}^6
 \{e_{Q_{+j}}e_{Q_{+j}}^T+
 (e_{Q_{-j}}-e_{A_j})(e_{Q_{-j}}-e_{A_j})^T\}\right]\,\mathrm F.
 \label{eq:shared-capacitance}
\end{equation}
The identity includes secondary, primary, output and probe capacitances;
the two additional terms per channel are its physical cells. In particular
$L\succeq I_{31}\,\mathrm H$ and $C\succeq I_{50}\,\mathrm F$.

Let $B$ collect the oriented winding-incidence columns in the first table
and the output column $e_o$. Let $G_0$ contain all bleeder, receiver and
probe conductance terms $g_ea_ea_e^T$, plus the six primary diagonals
$e_{p_j}e_{p_j}^T/R_s$. If $a_{jk}$ are the four selector incidences,
$G(z)=G_0+\sum_{j,k}g_{jk}a_{jk}a_{jk}^T$ and
$d(U)=\sum_j e_{p_j}U_j/R_s$. With clamp incidences $a_c$, set
$h(w)=(1\,\mathrm S)\operatorname{sgn}(w)\max(|w|-5\,\mathrm V,0)$.
Kirchhoff and component laws then give
\begin{align}
 L\dot i&=B^Tv-R_wi,\qquad R_w=I_{31}\,\Omega,\\
 C\dot v&=-Bi-G(z)v+d(U)-\sum_c a_ch(a_c^Tv),\\
 C_g\dot z_{jk}&=(c_{jk}-z_{jk})/R_g,\qquad
 g_{jk}=\tfrac1{10}\,\mathrm S+\tfrac9{10}\,\mathrm S\,
                   z_{jk}/(1\,\mathrm V).
 \label{eq:shared-fixture-laws}
\end{align}
The current at source $j$ is $I_j=(U_j-p_j)/R_s$, including its
capacitor and probe branches; it need not equal the primary winding current.
These definitions specify the full graph without discarding an energized
winding at a tap change.

Set $T_*=1/200\,\mathrm s$ and $t_e=1/800\,\mathrm s$. Every channel's
command changes from $(1,0,0,0)\,\mathrm V$ to $(0,1,0,0)\,\mathrm V$
at $t_e$. Gates start at the former values. With
$\tau_g=R_gC_g=1/1000\,\mathrm s$, after the command
$z_1=e^{-(t-t_e)/\tau_g}\,\mathrm V$,
$z_2=(1-e^{-(t-t_e)/\tau_g})\,\mathrm V$, $z_3=z_4=0$.
All selector conductances remain between $1/10$ and $1\,\mathrm S$.
The off paths remain finite; this is a simultaneous overlapping RC
transition, not ideal opening, six phase-shifted histories or a bank
reconnection. The gate/channel relation is a declared controlled law;
identifying an actual switch or cam remains a separate task.

All clamp laws are continuous and globally Lipschitz. The known gates,
invertible $L,C$, and affine growth bound give a unique global electrical
solution. Currents, capacitor voltages and gates are continuous at $t_e$;
command and power can jump, but no impulse or state reset occurs.

For the boundary retaining internal thermal energy $H$, let
$\dot H=D-H/\tau_h$, $\tau_h=2\,\mathrm s$. Here $D$ sums winding,
source-resistor, selector, bleeder, clamp, probe and gate-resistor heating.
For example, source heating is $(U_j-p_j)^2/R_s$ and clamp heating is
$(a_c^Tv)h(a_c^Tv)\geq0$. Receiver heat is outside. Integrate each
external product independently, splitting at $t_e$:
\begin{align}
 W_j&=\int_0^{T_*}U_j I_jdt,&
 W_{gjk}&=\int_0^{T_*}c_{jk}(c_{jk}-z_{jk})/R_g\,dt,\\
 W_L&=\int_0^{T_*}v_o^2/R_L\,dt,&
 Q_b&=\int_0^{T_*}H/\tau_h\,dt,\\
 E(t)&=\tfrac12i^TLi+\tfrac12v^TCv+
                \tfrac12C_g\sum z_{jk}^2+H(t),&
 r_E&=E(T_*)-E(0)-\sum_jW_j-\sum_{j,k}W_{gjk}+W_L+Q_b .
 \label{eq:shared-works}
\end{align}
Multiplying the independently specified electrical laws gives their
reactive-store derivative. At each source use
$p_jI_j=U_jI_j-R_sI_j^2$, and add the gate and caloric equations.
This proves $r_E=0$ for the declared model. Each winding's terminal work
$\int(b_w^Tv)i_wdt$ and its opposite node transfer are retained before
internal cancellation. Mutual magnetic energy is not assigned uniquely
to individual windings. An electrical-only boundary instead excludes $H$
and exports the separately integrated $D$; it must not also export the
same retained heat a second time.

## A prepared transition with continuous current margins
\label{sec:shared-feasibility}

Does this connected transition admit simultaneous source return and receiver
delivery within specified component limits throughout a nonzero interval?
The following prepared family answers that bounded question [OP-TRF-18].
Its nominal store is $392079/8000\,\mathrm J$, evaluated by components in
\eqref{eq:shared-initial-store}; the receiver is already energized.
The claim is simultaneous signed behavior of the connected graph over
$T_*=1/200\,\mathrm s$. Preparation, reset and repeated service have
different intervals and endpoint requirements.
In every channel the nominal initial data are
\begin{equation}
 \begin{gathered}
 (i_p,i_u,i_d)=(-1,1/5,1/10)\,\mathrm A,\quad
 (i_+,i_-)=(1,1)\,\mathrm A,\quad p_j=2\,\mathrm V,\\
 (A,T,X_+,Q_+,X_-,Q_-)=(1,1/2,4/5,7/10,1/5,1/10)\,\mathrm V,\quad
 i_o=-1\,\mathrm A,\quad v_o=1\,\mathrm V .
 \end{gathered}
 \label{eq:shared-preparation}
\end{equation}
All probes and $H$ start at zero; gates have the already specified values.
The admitted family varies every plant electrical coordinate independently
by at most $1/1000$ A or V, keeping probes, gates and $H$ fixed.
Preparation work is outside this operation interval.

\begin{theorem}[Finite shared-output witness]
Every preparation in this family has $I_j<-1/2\,\mathrm A$,
$i_{\pm j}>1/2\,\mathrm A$ and $v_o>1/2\,\mathrm V$ throughout
$[0,T_*]$. Every component current has magnitude below $2\,\mathrm A$,
every component voltage below $3\,\mathrm V$, every winding linkage
below $10\,\mathrm{Wb\,turn}$ and every common-core flux below
$7\,\mathrm{Wb}$. The receiver work exceeds $1/1000\,\mathrm J$.
\end{theorem}
\noindent\textit{Proof.}
Normalize currents by 1 A, voltages by 1 V and time by 1 s. In the
unclamped domain the 81-coordinate electrical vector $x$ obeys
$\dot x=A(t)x+b$. The incidence calculation in Appendix
\ref{sec:shared-bounds} gives $\|A(t)\|_\infty\leq61/10$ and
$\|b\|_\infty\leq1$ over the entire gate range. Use the looser bounds
$K=32$, $\beta=2$, $\rho=1/1000$, $\|x_0\|_\infty=2$ and
$T=1/200$. The integral equation bounds the displacement by
\begin{equation}
 \|x(t)-x_0\|_\infty\leq
 \rho+\frac{[K(2+\rho)+\beta]T}{1-KT}
 =\frac{331}{840}=:d_* .
 \label{eq:shared-box}
\end{equation}
This follows from $\int_0^t e^{Ks}ds\leq T/(1-KT)$, not an expansion
of the trajectory. Every relevant terminal difference is below
$2+2d_*=1171/420<3<5$ V. A first clamp crossing is therefore impossible,
which justifies continuation over the whole interval. Since the nominal
source node is 2 V, branch currents are 1 A and output is 1 V, the signed
margins are $1-d_*=509/840$ in the respective units. Hence
\begin{equation}
 W_L\geq\frac1{200}\left(\frac{509}{840}\right)^2\mathrm J
       =\frac{259081}{141120000}\,\mathrm J
       >\frac1{1000}\,\mathrm J .
 \label{eq:shared-service-bound}
\end{equation}
Winding currents are below $1+d_*<2$ A. The largest absolute sum of
inductance coefficients is $17/4$ H, giving linkage below
$19907/3360\,\mathrm{Wb\,turn}$. The output common flux is
$\Phi_o=(1/4\,\mathrm H)s^Ti_o^{\rm block}$ in the stated turn scale,
and is bounded by $15223/3360\,\mathrm{Wb}$; input-core bounds are smaller.
These are declared model limits, not material saturation ratings.

Capacitor currents require the derivative equation, not only the state
box. Reusing the sharper $K=61/10$, $\beta=1$ gives displacement
$\eta=134/1939$. Appendix \ref{sec:shared-bounds} bounds every physical
capacitor's $C_ea_e^T\dot v$; the largest is
$187351/96950\,\mathrm A<2\,\mathrm A$. Its separate resistor,
selector, probe, source, receiver and gate bounds are also below 2 A.
The changing full-winding selector has
$A_j-X_{+j}\geq(1/5-2\eta)\,\mathrm V=599/9695\,\mathrm V$,
so its current stays at least $599/96950\,\mathrm A>0$ during the edge.
All bounds hold at both event sides and at every intervening time.
$\square$

The nominal initial store is independently
\begin{equation}
 E_m(0)=\frac{40507}{1600}\,\mathrm J,\quad
 E_C(0)=\frac{2369}{100}\,\mathrm J,\quad
 E_g(0)=\frac3{1000}\,\mathrm J,
 \qquad E(0)=\frac{392079}{8000}\,\mathrm J .
 \label{eq:shared-initial-store}
\end{equation}
The receiver and magnetic states are already energized. For
$D_*=T_*-t_e=3/800\,\mathrm s$, independent integration of the six
rising gate sources, six falling gate resistors and the remaining zero
gates gives
\begin{equation}
 \sum W_{gjk}=\frac3{500}(1-e^{-15/4})\,\mathrm J,
 \qquad Q_g=\frac3{500}(1-e^{-15/2})\,\mathrm J .
 \label{eq:shared-gate-work}
\end{equation}
Each gate endpoint is evaluated from its exponential voltage, and their
store change equals the difference of these two independently integrated
terms. No residual defines either term.

For the electrical endpoints, the fundamental matrix of the connected
equations gives $x(t)=F(t,0)x(0)+\int_0^tF(t,s)b(s)ds$, composed across
the command with the identity state map. Substitute this state separately
in every integral in \eqref{eq:shared-works} and in its quadratic endpoint
store; the thermal endpoint follows its own convolution. These exact
expressions define the remaining works without assigning numerical
trajectories. In particular the proved source and receiver margins, the
gate integral and $Q_b\geq0$ imply
\begin{equation}
 E(T_*)-E(0)\leq\left[\frac3{500}(1-e^{-15/4})
       -\frac{6\cdot509}{840\cdot200}
       -\frac{259081}{141120000}\right]\mathrm J<0.
 \label{eq:shared-store-decrease}
\end{equation}
The endpoint store remains defined by the physical state in
\eqref{eq:shared-works}; this inequality follows from the independently
derived dynamics and port bounds. It is not an inferred preparation cost.
The exact identities and enclosures involve no numerical integration error;
the other finite-history integrals are left unevaluated and physical model
uncertainty remains unmeasured.

As a separate coupling control, set output mutual inductances to zero while
retaining their diagonal self-inductances and the same initial currents,
voltages, sources, receiver and gates. Its initial store becomes
$284079/8000\,\mathrm J$, instead of $392079/8000\,\mathrm J$.
The receiver winding is then magnetically independent and initially
energized; its current must be solved from the changed equations. This is
neither a separate loaded-transformer bank nor an equal-store efficiency
comparison. With all plant states and sources zero, plant and receiver
work remain zero, while initialized gates and their supplies still exchange
energy. Neither control supplies a full-wave cycle. Staggered commands,
longer intervals, singular component limits, other preparations and
material behavior require their own analyses.

## Insulation prevents full-state return
\label{sec:shared-machine}

Can the supplied assembly return its complete state after a timing-shaft
revolution in $T\in[1/2,2]\,\mathrm s$? For the insulated laws below,
that question has a negative answer [OP-TRF-19]. It is a different contract
from the preceding fixed-clock finite witness.

The boundary encloses the electrical fixture, six field-excited generators,
a generator shaft and an independently supplied timing shaft with its cams,
controller, sensors and gates. Its complete constitutive specification is in
Appendix \ref{sec:machine-specification}. Here the decisive retained state
is caloric energy $H$: insulation gives $\dot H=D_m$, with all internal
conversion nonnegative and timing-bearing conversion
$b_t\Omega^2$, $b_t=1/10\,\mathrm{N\,m\,s/rad}$. The timing angle obeys
$\dot\theta=\Omega$. The other 125 coordinates include electrical and
controller states and both shaft angles and speeds.

Take the section $\theta=0\pmod{2\pi}$ with $\Omega>0$, returning after
one positive timing revolution. Both shaft speeds must lie in
$[\pi,4\pi]\,\mathrm{rad/s}$, period in $[1/2,2]\,\mathrm s$,
winding/field currents below $10\,\mathrm A$ in magnitude and node
voltages below $10\,\mathrm V$. Angles return modulo $2\pi$; every
electrical, speed, relative-phase, controller and thermal state must also
return. The caloric law and the timing-bearing product give, for every
admitted history,
\begin{equation}
 H(T)-H(0)\geq b_t\int_0^T\Omega^2dt
 \geq\frac{b_t}{T}\left(\int_0^T\Omega dt\right)^2
 =\frac{4\pi^2b_t}{T}\geq\frac{\pi^2}{5}\,\mathrm J>0.
 \label{eq:shared-no-cycle}
\end{equation}
The middle step is Cauchy--Schwarz and uses the separately integrated
bearing power. Thus no full-state return fixed point, and hence no
attracting full-state cycle, exists in this domain. No initial thermal
preparation removes the positive drift. Two trajectories differing only
in initial $H$ keep that difference exactly under these laws. This proof
does not infer instability from a unit multiplier.

The conclusion concerns return of this full state, including $H$.
Electrical/shaft attraction with thermal drift, or operation with a heat bath,
has a different endpoint condition. The supplied-machine equations and
return-map variation remain in Appendix \ref{sec:machine-specification};
no cycle multipliers are assigned where there is no fixed point.

## A complete electrical history with insufficient energy accuracy
\label{sec:shared-observation}

Can complete electrical-port records identify initial electrical energy
uniformly within $1/250\,\mathrm J$ for the following two known
preparations? The specified probes and error set exclude that target
[OP-LR23-03]. Return to the electrical fixture and its original fixed clock;
the mechanical assembly and its cycle question are absent.

The first preparation is \eqref{eq:shared-preparation}. The second adds
$1/10\,\mathrm V$ to $Q_{+1}$ and subtracts it from $Q_{+2}$.
All other states, inputs, probes and gates are identical; $H(0)=0$ is
independently known. This pair is separate from the smaller feasibility
neighborhood. Every individual cell and parasitic, joint magnetic state,
gate and probe capacitor contributes to the initial electrical store.
The two changed nodes each have a cell and a unit parasitic, so direct
evaluation yields
\begin{equation}
 E_0=\frac{392079}{8000}\,\mathrm J,\qquad
 E_1=\frac{392239}{8000}\,\mathrm J,\qquad
 E_1-E_0=\frac1{50}\,\mathrm J .
 \label{eq:shared-energy-pair}
\end{equation}
The common baseline cancels the linear cross terms. With preparation
radius $1/10$, the same continuation bound gives maximum terminal
difference $127/42\,\mathrm V<5\,\mathrm V$, so both trajectories
remain unclamped. The smaller family's 3 V component bound is not invoked.

Observe all six exact source voltages and reported source currents
$\widehat I_j=(U_j-y_j)/R_s$, the receiver channels $y_o,y_o/R_L$,
all 24 gate command/current pairs and the event time on $[0,T_*]$.
The actual passive probe satisfies
$(10\,\mathrm s)\dot y_j=p_j-y_j$, $y_j(0)=0$; the receiver probe
obeys the same law with $p_j$ replaced by $v_o$.
Thus, for constant $U_j$, the reported current is a filtered current with
known initial value, not instantaneous $I_j(0)$. The two receiver channels
are redundant under the known load law.

Each reported source-current record permits any additive error function
bounded pointwise by $1/10\,\mathrm A$. There is no independence
assumption in time or across channels. Output, supply, driver, event-time,
gain, offset, coefficient and initial-sensor errors are fixed at zero for
this mathematical comparison. The 10 s response and loading are component
choices, not measured calibration. Heat export is integrated in the balance
but is not an observed channel here. “Complete electrical ports” therefore
does not mean calorimetric observation or instantaneous unfiltered records.

\begin{theorem}[Uniform energy-error obstruction]
For this two-state experiment the smallest possible worst-case absolute
initial-energy error is $1/100\,\mathrm J$. In particular the requested
$1/250\,\mathrm J$ target is impossible.
\end{theorem}
\noindent\textit{Proof.}
The connected electrical difference obeys the homogeneous linear equations
through both the plateau and finite edge. Its independent quadratic form
and derivative are
\begin{equation}
 D=\tfrac12\delta i^TL\delta i+\tfrac12\delta v^TC\delta v,
 \qquad \dot D=-\delta i^TR_w\delta i-\delta v^TG(z)\delta v\leq0,
 \qquad D(0)=\frac1{50}\,\mathrm J .
 \label{eq:shared-difference}
\end{equation}
Each primary node has a unit capacitor, so
$|\delta p_j|\leq\sqrt{2D(0)/(1\,\mathrm F)}=1/5\,\mathrm V$.
The passive filter has zero initial difference and a nonnegative impulse
response. With $\tau=10\,\mathrm s$ and $R_s=1\,\Omega$, direct
integration of its kernel gives
\begin{equation}
 |\delta\widehat I_j(t)|\leq\tfrac15(1-e^{-t/\tau})\,\mathrm A,
 \qquad
 \sup_{0\leq t\leq T_*}|\delta\widehat I_j(t)|
 <\tfrac1{10000}\,\mathrm A<\tfrac15\,\mathrm A .
 \label{eq:shared-probe-window}
\end{equation}
Here $T_*/\tau=1/2000$ and $1-e^{-x}<x$ for $x>0$.
The response is therefore strongly attenuated on this 5 ms window relative
to the stipulated $1/10$ A error on each trace. The final weaker bound is
sufficient for the overlapping-record construction below.

Swapping channels 1 and 2 commutes with $L,C,B$ in their corresponding
coordinates, all permanent connections and each synchronous selector
coefficient. It also fixes the input forcing. The initial difference changes
sign under this permutation; uniqueness therefore keeps it antisymmetric.
The output winding, receiver and its probe are invariant coordinates,
so their differences are identically zero throughout. Gate histories are
identical. This is a property of the connected flow across the entire
finite edge, not a fixed-topology rank assertion or a static cell sum.

Choose the midpoint of the two reported source-current histories and the
common output and gate records. Each of the two explanations needs error
at most $1/10\,\mathrm A$, so both are admitted. For its consistent-state
set $\mathcal S(y)$, this record has exact energy width $1/50\,\mathrm J$.
Every estimate must err by at least half that width for one of its endpoints.
For any other admitted record the two-state set is either a singleton or
the same pair. Its energy-interval midpoint attains worst-case error at
most $1/100\,\mathrm J$, proving equality. $\square$

Exact source traces can distinguish more than this finite-error record.
A longer history, tighter errors, additional cell/flux probes, observed heat
or unknown coefficients defines another experiment, with its own physical
loading and consistent-state set. The conditional binary cell-probe criterion
in Section \ref{sec:binary-observation} uses a different loaded graph and
response time; its postconnection separation remains to be proved. The
present obstruction depends on its specified filters, window and error set,
while exact receiver indistinguishability follows separately from symmetry.
Neither treatment supplies a universal state/sign reconstruction claim or
evidence of a missing physical energy transfer.

## Finite comparisons for the shared assembly

For an identified implementation of the finite transition, hold the input
waveforms, command time and individual initial capacitor/winding states,
then observe simultaneous complete source, receiver and gate terminal
products. The predicted sign margins are $509/840$ A and V. To establish
the stricter $1/2$ thresholds from those model values, total current or
voltage error must be below $89/840$ in the corresponding units; for
receiver service it must be below
$(259081/141120000-1/1000)\,\mathrm J$. Actual observations instead use
their measured lower bounds. Independently justified model error is part
of those bounds, not calibrated from a small balance residual. The finite
1 ms gate response requires verified timing and bandwidth; synchronous
voltage/current acquisition alone does not establish that adequacy.

Observe cell and magnetic endpoints independently, including the initially
energized receiver, all probes, gates and thermal state. Winding terminal
integrals and an identified flux/material law are needed to reconstruct
magnetic state; unit model flux limits are not physical core ratings.
Resolve actual clamp, switch, gap and return paths. A source return with
positive receiver work is compatible with the proved decreasing prepared
store; a complete measured remainder requires every boundary term in
\eqref{eq:shared-works} and propagated uncertainty.

For the machine assembly, synchronized torque and encoder observations at
the common prime-mover and timing shafts resolve their effort--rate
products. Field, sensor, controller and gate supplies are separate electrical
observations. Thermal endpoints and exported heat distinguish insulated
drift from a cooled return. Under the stated insulated bearing law the
lower bound is $\pi^2/5\,\mathrm J$ per admitted revolution. A finite
thermal uncertainty smaller than a proposed separation is necessary to
test it. A cooled or temperature-dependent apparatus needs its own law;
that comparison leaves the proved insulated obstruction resolved.

For energy identification, the existing error set cannot meet the stated
target regardless of estimator choice. An added observation can discriminate
the known pair if its two predicted responses differ by more than twice
its independently bounded error. Establish those responses from the new
loaded graph, including probe work and disturbance, before using that
criterion. Alternatively, bound the energy width of its entire consistent
state set by $2\epsilon_E$. This condition concerns the energy target;
full state reconstruction is stronger.

A switched/bypass performance comparison additionally fixes useful receiver
service and actual preparation, operation, relaxation and reset paths.
Integrate prime-mover and every auxiliary supply separately; match endpoints
or retain their differences and explicit reset costs. The finite witness,
insulated obstruction and observation theorem do not supply that ordering.
Ordinary synchronized electrical, torque/encoder and thermal instruments
provide the relevant observables, but their calibration, loading and
bandwidth must resolve the particular difference. No apparatus data or
unmeasured physical remainder are assigned by these model results.

# Material, thermal, sensor, and supply boundaries

## Conversion is different from heat already exported

For a fixed physical mesh, opposing sliding forces convert
$D=\mu N|v_{\rm slip}|$. Both contact points receive the same observation
velocity subtraction, so $v_{\rm slip}$ and $D$ are invariant.
For $\mu=1/2$, $N=2$ N, $|v_{\rm slip}|=1$ m/s over one second,
the mechanical conversion is 1 J in every observation; at $\mu=0$ it is
zero. Bearings use relative angular speed, for example
$D_b=b(\omega-\omega_b)^2$, while a declared quadratic drag effort gives
windage conversion $D_w=c|\omega-\omega_a|^3$. Lubricant churning needs
its own measured constitutive law and moving-fluid boundary. None follows
from the ideal rolling equation.

A thermal body with heat capacity $C_T$, excess temperature $\theta$ above
a fixed ambient $T_a>0$, and conductance $H_T$ obeys
\begin{equation}
 C_T\dot\theta=D-H_T\theta,\qquad E_T=C_T\theta,\qquad
 P_{\rm amb}=-H_T\theta=-T_b\dot S_{\rm out}.
 \label{eq:thermal}
\end{equation}
For constant $D$ and initial $\theta=0$,
$\theta=(D/H_T)(1-e^{-H_Tt/C_T})$.
Choose $D=1$ W, $C_T=H_T=2$ in SI units on one second. The independently
integrated internal conversion, external heat, and store change are
$+1$, $-e^{-1}$, and $1-e^{-1}$ J. Immediate export would predict
$-1$ J and zero thermal change. In the combined mechanical/thermal
boundary the conversion cancels between the two subsystems; only ambient
heat crosses the combined boundary.
For repeated identical heating intervals the exact map is
$\theta_{n+1}=e^{-H_TT/C_T}\theta_n+(D/H_T)(1-e^{-H_TT/C_T})$.
No equality of initial and final temperatures is assumed. If copper
resistance varies with temperature, specify $R(T)$ independently and
integrate $R(T)i^2$ on the actual path; a fixed-temperature law cannot
identify that feedback.

Coulomb conversion is invariant under a change of observation for the same
physical contact; the actual friction law still requires identification
[OP-EPI-13]. Bearing drag, windage, churning and retained heat require
their own ports and endpoint observations [OP-EPI-25].

## Magnetic material states and finite settling

A normalized but dimensionally scaled magnetic mode in configuration VI
has flux $\phi$, material state $m$, and energy
\begin{equation}
 E_m=\frac{\phi^2}{2}+\frac{a\phi^4}{4}+\frac{h(\phi-m)^2}{2},\quad
 i=\frac{\partial E_m}{\partial\phi}=\phi+a\phi^3+h(\phi-m),\quad
 \dot\phi=v-Ri,\quad \dot m=\frac{h(\phi-m)}\zeta.
 \label{eq:material}
\end{equation}
Positive $a,h,\zeta$ carry the units making each term an energy or the
stated electrical variable; numerical controls set their SI coefficients
to one where specified. Differentiation from these independent laws gives
$\dot E_m=vi-Ri^2-h^2(\phi-m)^2/\zeta$.
Thus electrical input, copper heat, and material heat are distinct integrals.
Positive $a$ gives a saturation-type increasing reluctance; a single lag is
one admissible rate-dependent model, not an identified magnetic material.
A fitted average loss or loss per cycle does not specify this state law,
its reversible store or its initial memory. Bias, temperature, minor loops
and changing frequency require independently identified constitutive behavior.

For a reversible ramp, $\phi=t$, $h=0$, $R=1/5$ on $[0,1]$ s,
$i=t+at^3$, $v=1+Ri$, and initial energy zero. With $a=0$ the separate
source and copper works are $17/30$ and $-1/15$ J, giving final energy
$1/2$ J. With $a=1$ they are $3/4+92/525$ and $-92/525$ J, giving
$3/4$ J. The extra magnetic input is $1/4$ J, calculated from
$\int i\dot\phi dt$ for each path. This does not specify hysteretic loss.

For an exact periodic lag control take $a=h=\zeta=1$, $R=1/5$,
$\phi=\sin t$, $m=(\sin t-\cos t)/2$ and impose
$v=\cos t+Ri$ on $[0,2\pi]$ s. Direct integration gives
\begin{equation}
 W_s=63\pi/40\ \mathrm J,\quad W_{\rm copper}=-43\pi/40\ \mathrm J,
 \quad W_{\rm material}=-\pi/2\ \mathrm J,
 \quad E_m(0)=E_m(2\pi)=1/8\ \mathrm J.
 \label{eq:material-cycle}
\end{equation}
For the reversible $h=0$ control on the same imposed $\phi$, magnetic
cycle input and material heat are both zero; its source still supplies its
own copper integral. The lag control's initial $m=-1/2$ is a prepared
periodic state. Its preparation work is not assigned from $1/8$ J.

Finite settling can be checked exactly. Set
$m=(\sin t-\cos t)/2+\delta e^{-t}$ on the same interval. Material
conversion becomes
$\pi/2-\delta(1-e^{-2\pi})+\delta^2(1-e^{-4\pi})/2$;
magnetic electrical input is
$\pi/2-\delta(1-e^{-2\pi})/2$.
The endpoint stores, evaluated from the material state, are
$(1/2-\delta)^2/2$ and $(1/2-\delta e^{-2\pi})^2/2$ J. Their change is
$\delta(1-e^{-2\pi})/2-\delta^2(1-e^{-4\pi})/2$ J.
Measure $\int i(v-Ri)dt$, flux linkage, thermal transfer, and endpoint
material indicators over successively specified finite periods. Saturation,
remanence and hysteresis laws require independent identification; a loop
that has not returned to its initial material state is not an exactly
periodic heat measurement.

Even a memory-free sinusoid needs its actual work window. For a $1\,\mathrm F$
capacitor take $v=\cos t$ V and $i=-\sin t$ A, with $t$ expressed in seconds
and angular frequency $1\,\mathrm{rad/s}$. The full-period average power
is zero, whereas on $[0,\pi/2]\,\mathrm s$,
\begin{equation}
 W=\int_0^{\pi/2}-\cos t\sin t\,dt=-\tfrac12\,\mathrm J,
 \qquad E(\pi/2)-E(0)=0-\tfrac12=-\tfrac12\,\mathrm J .
 \label{eq:finite-window-capacitor}
\end{equation}
Each endpoint is evaluated as $Cv^2/2$. A cycle-average loss or power
cannot replace that finite signed integral or determine a material reset.

Finite magnetic constitutive behavior must be identified beyond the linear
winding law [OP-TRF-03]. Remanence, hysteresis and temperature-dependent
states in an actual material retain a separate cycle-work question
[OP-LR57-01].

## Finite sensors and biased electromechanical actuation

A sensor capacitor driven by a held unit voltage through $R=1\,\Omega$,
$C=1$ F from zero has $v=1-e^{-t}$ and source current $e^{-t}$.
On $[0,\ln2]$ s, the source work is $1/2$ J, resistor heat work
$-3/8$ J, and capacitor endpoint store $1/8$ J. Their separate products
are $1\cdot e^{-t}$ and $-e^{-2t}$.
A nonloading ideal observation assigns all three zero; this finite sensor
has both delay and supplied energy. If its resistor is inside a thermal
boundary, use \eqref{eq:thermal} instead of exporting its conversion twice.
Real probe input capacitance, transducer bias, electronics supply, and
calibrated transfer function belong to the sensor model. Noise, delayed or
nonlinear observers, and multiple feedback channels are additional states
or error processes, not consequences of this scalar control.

For the electromechanical plant, independently specify
\begin{equation}
 L\dot i=v_s-Ri-g_ev_m,\qquad \dot x=v_m,\qquad
 m\dot v_m=g_mi-cv_m-kx+F_s.
 \label{eq:transducer}
\end{equation}
Its store is $Li^2/2+mv_m^2/2+kx^2/2$. Multiplication by $i$ and $v_m$
identifies the separate controller transfer
\begin{equation}
 P_a=(g_m-g_e)iv_m,
 \quad \dot E_{\rm plant}=v_si+F_sv_m-Ri^2-cv_m^2+P_a.
 \label{eq:controller}
\end{equation}
The controller receives $-P_a$ on the opposite boundary. Reciprocal
coupling has $g_m=g_e$; unequal or reversed backaction requires a separately
supplied physical realization, not a negative store.

For an exact finite supply control use $L=m=1$, $R=c=k=0$,
$g_e=1$, $g_m=2$, $i=v_m=1$, $v_s=1$, $F_s=-2$ on one second.
The imposed motion satisfies \eqref{eq:transducer}, its store is 1 J at
both endpoints, and separate works are $W_e=1$, $W_m=-2$, $W_a=1$ J.
Let a declared bidirectional converter have efficiency $1/2$ in delivery,
so that delivering $P_a=1$ W draws 2 W and converts 1 W to heat.
A bias coil $L_b=1/2$ H, $R_b=1\,\Omega$, held at $i_b=1$ A requires
another 1 W and has store $1/4$ J at both endpoints. The source-to-controller
work is 3 J; output, converter heat, and bias heat works are each $-1$ J.
The controller therefore has zero store change by its independent states.

Realize the finite source by a rail $C_s=2$ F, $V_s(t)=\sqrt{4-3t}$ V,
with ideal regulated draw $I_s=3/V_s$ A. Its store changes from 4 to 1 J,
and its separately integrated output is $-\int V_sI_sdt=-3$ J.
The combined plant, controller, and rail endpoints are $21/4,9/4$ J;
external electrical input, receiver output, and the two heat works sum to
$1-2-1-1=-3$ J. A remaining voltage above the declared cutoff 1 V permits
this interval; beyond its endpoint the regulator law must change.
The regulated draw and conversion law are assumptions requiring their own
actuator and supply measurements.

Source-off does not imply passive decay of every controller store. For a
separate return control, a mechanical actuator delivers 1 W to a converter
with recovery efficiency $1/2$ for one second. The rail receives $1/2$ J,
converter heat receives $1/2$ J, and the actuator receives work $-1$ J.
If $C_s=2$ F and $V_s(0)=1$ V, then
$V_s(t)=\sqrt{1+t/2}$ and rail current is $1/(2V_s)$; direct integration
gives the stated positive rail work. This is an explicitly supplied return
path, not a prediction for an unidentified bias coil. The actual bias law
can make coupling coefficients depend on $i_b$ and must be solved with the
plant. A bounded algebraic controller or a positive aggregate store cannot
certify its separate coil, rail, thermal, or whole-apparatus work accuracy.

Finite sensors and thermal endpoints require measured loading, supply
work and retained states [OP-LR57-07]. The realized actuator and bias
supply must support each forward or returned controller transfer
[OP-LR59-02].

## Complete cycles and what a prescribed path establishes

For every actual apparatus keep stages $\ell$ distinct:
preparation, operation, switching, relaxation, reset, and any hold interval.
The measured statement is
\begin{equation}
 r_{\rm cycle}=E_{\rm final}-E_{\rm initial}
              -\sum_\ell\sum_j\int_{t_{\ell,0}}^{t_{\ell,1}}e_jf_jdt.
 \label{eq:cycle}
\end{equation}
A periodic thermal state, restored battery state, or emptied capacitor is
an endpoint observation, not a premise. For a source-free regular linear
relaxation, $x(T)=e^{AT}x(0)$ and the exponential is invertible. A nonzero
state cannot become exactly zero at finite $T$ by that law alone.
For a capacitor $C,V_0$ relaxed through $R$ for $T=RC\ln2$, separate heat
work is $-3CV_0^2/8$ and endpoint store $CV_0^2/8$.

A completely specified elementary 2 J receiver cycle uses a unit capacitor.
On preparation $[0,2]$ s impose $v=t$ with source current 1 A; its work is
$+2$ J and store rises from 0 to 2 J. On operation $[2,6]$ s use an
ideal controlled receiver with $v=(6-t)/2$, receiving current $1/2$ A.
Its work into the capacitor boundary is $-2$ J and store falls to zero.
On reset $[6,10]$ and hold $[10,12]$ s, $v=i=0$ and all works are zero.
Currents change finitely at the switches; capacitor voltage is continuous.
This is a prescribed, lossless current-control model. A one-half-efficient
physical preparation converter instead draws 4 J to deliver the same
2 J preparation; its independent heat work is $-2$ J. Both predict the
same receiver transfer and different measured source work.

A finite reset compares further paths. Discharging a prepared unit-energy
store to zero through a resistor sends 1 J to heat in a complete asymptotic
reset, with finite endpoints retained on every finite interval. A lossless
resonant auxiliary receives that energy in a finite quarter-period and must
return it during a specified later preparation to close its own cycle.
A one-half-efficient regenerative converter delivering the same 1 J removal
to a battery stores $1/2$ J and converts $1/2$ J to heat; drawing that
$1/2$ J back through the same efficiency returns only $1/4$ J to the plant.
Battery terminal work, chemical state, and temperature must be independently
specified; those efficiencies are illustrative laws, not battery measurements.

For the broader physical cycle questions, retain the different apparatus.
A differential three-coil pickup, rectification before or after combining
pickup signals, and a tuned receiver each have separate preparation and
reset connections. Finite paths for those systems do not establish cycles
for a local/distant-field winding arrangement, a moving or relaxing magnetic
material, or a spark-gap resonator. For the field arrangement integrate every
winding source and reset branch and include field energy endpoints. For
motion/material apparatus add force–velocity and material/thermal states.
For a spark-gap resonator retain primary, secondary, gap, clamp, and parasitic
capacitor ports on each event side. A 2 J receiver target can be held for
each comparison, but its required source work is
$2\,\mathrm J+Q_{\rm ext}+\Delta E-W_{\rm other}$, where each term is
independently observed or predicted from its specified law; this identity
is not a way to assign an unmeasured port. No unspecified source, arc,
battery, or controller law has a definite efficiency or cycle work here.

A complete transformer cycle requires all finite stages and observed reset
states [OP-TRF-05]. Prescribing a path does not establish a physical
supply's work or feasibility [OP-LR49-01]. The broader field, pickup,
moving-material and spark-gap apparatus retain their own missing laws
[OP-LR49-02].

# What must be measured
\label{sec:measurement-route}

## A sequence of physical decisions

Begin with the simplest comparison whose component laws and observations
can be identified. The budgets below are decision requirements, not achieved
instrument specifications. The detailed mechanical, electrical and preparation
comparisons that follow retain the other cases and their local questions.

| Stage | Quantity and model contrast | Decision and next step |
|------------------------|----------------------------------------------|----------------------------------------------|
| One planet receiver | Ring-held one-second carrier-work change $7/3$ J, with the specified load and motion | Identify full-turn lead-out clearance and phase first; then require total difference uncertainty below $1/10$ J as developed in the opening comparison |
| One return or probe change | The prepared RC receiver receives $(1-e^{-2})/2$ J without the probe and $(1-e^{-4})/4$ J with it | Keep preparation and interval fixed; resolve their difference with a smaller combined work uncertainty and include probe work and both endpoints |
| Two known cell preparations | Cell stores 1 and 5 J; finite preterminal contrast below $1/1000$ V | Establish the remaining loaded-probe separation before using the $1/20$ V intervals as a classifier; paired receiver-work ordering remains unevaluated |
| Shared output or supplied timing | Prepared return, insulated thermal drift, or a two-state energy-error bound | Choose one question and its complete boundary; identify the material, supply, filter and endpoint laws before extending its conclusion |

: A reading and measurement route. Later stages require their own preparations and uncertainties, rather than inheriting a verdict from an earlier apparatus.

For the first stage, a full low-speed carrier revolution resolves finite-yoke
and sleeve clearance, bearing/support positions and output phase before the
work comparison. Synchronized torque, angle and application-point motion
then distinguish the stated load response from a changed linkage trajectory.
The $7/3$ J result uses one $1\,\mathrm{N\,m}$ takeoff; the later $7$ J
control uses the separately stated total output loading. They are different
operating points with different force-sharing assumptions.

For a predicted difference $\Delta_*$, compare the measured difference with
its independently bounded interval: exclusion of $\Delta_*$ identifies a
disagreement with that specified model; inclusion leaves it compatible at
that resolution. A remaining discrepancy retains its sign, magnitude and
conditions while a follow-up separates loading, preparation, material or
instrument effects. If the interval includes both competing predictions,
reduce the dominant uncertainty or select another directly discriminating
observable before interpreting it. An unknown physical remainder supplies
no numerical alternative prediction by itself.

At each electrical boundary specify the voltage/current reference planes,
return conductors, mutual and leakage stores, probe loading and gate supplies.
The terminal product and field flux across the same interface are two
descriptions of one transfer. Parasitic, displacement and common-mode paths
need identification against dimensions and the full edge bandwidth.
The models below bound their own finite graphs; omitted physical paths remain
unidentified rather than assigned zero work. Active laws and finite unstable
histories can be investigated under their own declared operating domains.

## Independent uncertainty for work and endpoints

Record conjugate effort and flow on the same physical interval, including
all event sides. If true channels differ from recorded $\widehat e,\widehat f$
by at most $u_e,u_f$, an exact bound is
\begin{equation}
 |W-\widehat W|\leq
 \int_{t_0}^{t_1}(|\widehat e|u_f+|\widehat f|u_e+u_eu_f)dt
 +U_{\rm time}+U_{\rm band}+U_{\rm read}.
 \label{eq:uncertainty}
\end{equation}
Here the additional bounds cover integration endpoints and relative timing,
unresolved signal bandwidth, and reading reconstruction, including noise and
quantization. They are established independently of a small energy residual.
For a finite endpoint error $\delta t$ and bound $|P|\leq P_{\max}$,
the omitted endpoint work is at most $P_{\max}|\delta t|$.
If a flow channel has $|\dot f|\leq B_f$, a relative timing offset bounded
by $u_t$ contributes flow error at most $B_fu_t$ by the mean-value theorem.
Neither bound applies across an unresolved ideal impulse; use the finite
physical pulse and its actual envelopes.

For a capacitor with recorded positive $\widehat C$,
$|C-\widehat C|\leq u_C$, and $|V-\widehat V|\leq u_V$, the exact
endpoint bound is
\begin{equation}
 U_E\leq\frac{u_C}{2}(|\widehat V|+u_V)^2
       +\widehat C\left(|\widehat V|u_V+\frac{u_V^2}{2}\right).
 \label{eq:endpoint}
\end{equation}
Use the quadratic-form analogue for coupled magnetic or mechanical stores,
including covariance or interval dependence of their parameters and states.
The mutual term is not two independent inductors. Thermal endpoints require
heat capacity, temperature distribution, and heat-transfer uncertainties;
material endpoints require the stated internal-state law. A residual bound is
\begin{equation}
 U_r=U_{E_0}+U_{E_1}+\sum_jU_{W_j},\qquad
 r_E\in[\widehat r_E-U_r,\widehat r_E+U_r].
 \label{eq:residual-bound}
\end{equation}
This conservative interval needs no independence assumption. Correlation can
sharpen it only when established by calibration and propagated jointly.
For probabilistic intervals, specify the joint error law and coverage;
for certified intervals, enclose its support and nonlinear products.
General metrological treatment of inputs and correlations is described by
[JCGM (2008)][gum]; the finite product and endpoint bounds here are derived
directly and discard no second-order term.

Phase and polarity errors illustrate the size of the problem. For peak
signals $v=\cos t$, $i=\cos(t+\phi)$ over $[0,2\pi]$ s,
\begin{equation}
 W=\pi\cos\phi\ \mathrm J,\qquad
 \widehat W=\sigma(1+a)(1+b)\pi\cos(\phi+\delta)\ \mathrm J.
 \label{eq:phase}
\end{equation}
Here $\sigma=\pm1$ is channel polarity, $a,b$ are gains, and $\delta$
is relative phase including timing at the stated angular frequency.
At $\phi=\pi/2$, $\delta=\pi/6$, unit gains and correct polarity,
$W=0$, $\widehat W=-\pi/2$ J. At $\phi=0$, $a=3/100$, $b=-3/100$,
$\delta=0$, the gain error is $-9\pi/10000$ J. Reversing only current
changes $+\pi$ to $-\pi$ J. Reversing both channels does not do so.
These predictions follow by direct trigonometric integration.
A sensor voltage error $1/100$ V at a true 100 V on a 1 F capacitor gives
endpoint error $20001/20000$ J. Similar-looking endpoint voltages do not
establish cancellation of their calibration errors.

A low-pass channel's transfer, loading, time alignment, noise spectrum, and
quantization must be calibrated over the signals being integrated. In a
multi-port assembly, moving a probe across a shunt can include a different
branch: the extra current is a physical port-placement error with correlated
voltage and store consequences. Synchronizing instruments alone does not
bound it. A sensor that loads the apparatus changes its trajectory and belongs
in its constitutive comparison.

The calibrated polarity, gain, phase, timing, bandwidth and endpoint
uncertainties determine the signed residual that can be resolved
[OP-LR63-02].

## Finite comparisons and decision requirements

In the following tables, every pair gives different predictions for at least
one accessible quantity under its stated control. A zero in the first column
may be a null hypothesis about an omitted contribution, not an established
physical law. An exact alternative applies only with its explicitly stated
constitutive assumptions. For a pair separated by $\Delta>0$, require a
combined prediction-setting and observation uncertainty $U<\Delta/2$;
$U\leq\Delta/4$ is a concrete design target. This requirement is applied
to the individual comparison, never inferred from instrument names.
If the required bound is unavailable, that comparison remains unresolved.
A finite outcome can reject one of these readings on its interval; it does
not close the same question for every material, geometry, or drive.

For an unknown physical remainder, the complete-model reading is
$r_E=0$; a surviving-discrepancy reading is $r_E=\delta$ with
$|\delta|>U_r$, where sign and magnitude must be measured.
These are distinct boundary predictions but there is no justified fixed
nonzero value before measurement. To validate the observation chain at a
known scale, introduce an independently metered $1/4$ J positive input.
Omitting it predicts $r_E=+1/4$ J; including it predicts zero for the
otherwise exact control. Requiring $U_r<1/8$ J distinguishes that omission.
This calibration control is not a prediction of a physical energy anomaly.

The loaded carrier comparison has a practical conditional budget. Suppose
both torque records have $|\widehat\tau|\leq8$ N m and
$|\widehat\omega|\leq4$ rad/s, with respective pointwise errors
$1/100$ N m and $1/100$ rad/s. On two one-second observations the product
part of \eqref{eq:uncertainty} is at most $1201/5000$ J.
A total comparison bound of 1 J leaves $3799/5000$ J for the other
contributions and separates the 7 J attachment difference.
It does not establish a 1 J full-boundary residual uncertainty.

For the reference actuator, $\widehat C=1$ F, $u_C=1/100$ F,
$|\widehat w|\leq2$ V, and $u_V=1/100$ V give
$U_E\leq80501/2000000$ J at each endpoint. Two final-state observations
have total $80501/1000000$ J before setting and timing uncertainty.
A $1/10$ J comparison budget leaves $19499/1000000$ J for those effects.
It resolves $[(9+e^{-10})^2-100]/50$ J from zero: since $e^{-10}<1/100$,
its magnitude exceeds $188199/500000$ J.
For full work closure also observe actuator, sensor, driver, rail, and
thermal endpoints or their external supply products.

## Mechanical comparisons

Hold the declared rates or paths with separately metered actuators and
observe torque and angle, force and displacement, and each endpoint motion together.
The table preserves distinct contact, support, and whole-system boundaries.

| Question and held control | Reading A | Reading B and decisive observation |
|--------------------------------------|--------------------------------|--------------------------------------------------------|
| Stator mounting, same negative-speed motion | No change in conversion: $0$ | $Q_c-Q_0=7\pi/50$ J; integrate drag torque against each relative angle, retaining phase endpoints |
| Attached receiver, configuration I | Unloaded carrier work $-7$ J | Loaded $0$ J; measure sun, ring, carrier, and all three receiver works on the same motion |
| Transient frame closure | Carrier shafts alone sum to $595/72$ J | Effective change $517/72$ J with field work $-13/12$ J; reconstruct all four observations from synchronized motions and inertias |
| Location of frame difference | Held-ring work remains $0$ in both observations | Carrier-ring work $-5$ J in steady operation; integrate its independently measured reaction torque |
| History partition, same endpoints | Shaft difference $13/12$ J at $b=0$ | $13/9$ J at $b=1$; drive the distinct intermediate ring path and observe both field and shaft shares |
| Hooke support over a complete cycle | Torque-path $W_u=0$ | A specified extra unit support torque adds $\pi/2$ J over the control cycle; resolve its torque and support angle rather than assign it from the residual |
| Ratio-two bevel support | Held support flow gives $0$ | Moving support gives $-\pi/2$ J in ground; carrier reconstruction gives zero on the same cycle |
| Compound observation, close-ratio geometry | Ground $\mathcal C_0=1$ | Carrier $2950/21$; measure each signed shaft and contact side and bound the nonzero ground denominator |
| Other geometry, two-sun control | Ground shaft ratio $1$ | Carrier shaft ratio $6/5$; instrument four shafts and retain all four meshes; helical or bevel thrust requires its own force/motion observations |
| Compliant engagement | An inferred instantaneous 1 J jump from a power change | Actual instantaneous store jump $0$ despite a 1 W power jump; resolve finite contact work $2$ J, heat $1$ J, and spring endpoint $1$ J |
| Restitution control | Elastic $e=1$: kinetic loss $0$ | $e=1/2$: loss $3/16$ J; observe incoming/outgoing motion and resolved contact work, with adequate pulse bandwidth |
| Compliance with acceleration | Omitting the field leaves carrier final accounting at $27/32$ J | Including $-1/2$ J field work gives $11/32$ J effective store in the six-contact train; observe all contact states and event sides |
| Unequal planets and pin couple | Equal first-contact work $7/3$ J; zero pin-pair work | First contact $7/2$ J; the separate one-pin control gives $-1/3$ J; measure individual forces and pin torques |
| Locked approach | Drive-scaled limiting works $(0,0,0)$ | Fixed-drive $(2,5,-7)$ J; record drive and relative motion separately at each finite approach |
| Mesh friction invariance | Frame heat difference $0$ | A postulated frame-dependent extra $1/4$ J differs from zero; compare reconstructed relative-slip products on the same contact, not remounted friction bodies |
| Bearing/windage/churning with a thermal store | Immediate export 1 J, retained heat $0$ | Unit thermal control exports $e^{-1}$ J and retains $1-e^{-1}$ J; observe temperatures and ambient heat as well as mechanical conversion |
| Radial motion | Omitted radial work $0$ | Radial guide work $-3/2$ J; measure radial force and displacement with tangential support work $+3$ J |
| Nonparallel observation | Scalar-only field work $0$ | Vector control $-1$ J; reconstruct all angular-momentum components and observer motion |
| Within-interval reversal | Net signed work $0$ taken as zero traffic | Absolute transfer $1/2$ J and unit-drag heat $1/2$ J; integrate both sides of the flow zero |
| Cardan transverse and bending work | Fixed application point: $0$ | Unit force through unit displacement: $1$ J; determine actual bearing constraints and all force/couple conjugate motions |
| Unequal angles, acceleration, phase actuation | Equal-angle partial support, steady rotor pin, and absent phase drive: $(0,0,0)$ | Separate controls give $(\pi/4-\arctan(3/4),1/2,1)$ J; observe each support and phase supply on its own interval |
| Physical gear closure | Complete physical residual $0$ | $\delta$ outside its independent interval bound; validate the chain with the $1/4$ J input, then retain any actual signed discrepancy with all completed checks |

: Distinct mechanical measurement targets. The deliberate extra-torque and extra-work alternatives are explicit falsification controls, not assigned properties of unknown joints or friction laws.

A physical gear remainder has unknown magnitude and sign until the complete
boundary is measured within those independent uncertainties [OP-EPI-34].

## Electrical and correspondence comparisons

Use synchronized complete voltage/current pairs for source, receiver, probe,
reference driver, switch, and heat-conversion channels. Independently observe
winding currents, capacitor voltages, flux or identified material states,
and thermal endpoints. A specified finite waveform must fit the calibrated
channel bandwidth without clipping; opening pulses require a separate bound.

| Question and control | Reading A | Reading B and decisive observation |
|--------------------------------------|--------------------------------|--------------------------------------------------------|
| Physical reference attachment | Common coordinate shift: added work $0$ | Unit RC attachment requires $5/6$ J input, retains $1/2$ J; observe its actual return current and voltage |
| Complete transformer cycle | Passive finite relaxation called reset: final store $0$ | At $RC\ln2$, final store $CV_0^2/8$; observe preparation, receiver, switch, supplies, and all remaining states separately |
| Nonlinear magnetic/thermal state | Linear unit ramp: magnetic input $1/2$ J | Saturated ramp: $3/4$ J; observe $i(v-Ri)$ and actual material/thermal endpoints |
| Energized winding opening and return commutation | Unit-voltage clamp receives $3/2$ J | Two-volt clamp receives $2$ J; observe each clamp and switch port; the tapped overlap/gap alternatives use their separately defined matrix works |
| Finite reference realization | Ideal receiver endpoint $2$ J | Finite actuator $(9+e^{-10})^2/50$ J; compare source products, tracking, actuator stores, and finite rail state |
| Constrained winding limits | Zero-store ideal transformer at the unit ramp: $0$ | Perfect-coupling finite-magnetizing model: $1/2$ J; retain the separate capacitance, source-resistance, short, and zero-ratio controls in the constrained table |
| Crossed load, probe, frequency, and preparation | Prepared RC receiver gets $(1-e^{-2})/2$ J without the probe | With probe it gets $(1-e^{-4})/4$ J; use all 16 specified winding settings for interaction claims and each exact work primitive on its own state |
| Physical transformer closure | Complete physical residual $0$ | $\delta$ outside its independently bounded interval; the known $1/4$ J input validates detection separately from physical closure |
| Loaded dynamic mapping | Coordinate-shift-only capacitor change $0$ | Supplied compensation gives $2$ J, matching the relative kinetic control; observe the extra ports and state mapping, not solely terminal counts |
| Ideal compound terminal versus physical ratio | Complete-port ratio $1$ for $R=-341/100$, $B$ held | $A$-frame mapped ratio $341/100$; observe actual winding voltages and reconstructed terminal contributions separately |

: Electrical comparisons. Finite-model success includes every port and both state endpoints on each interval; neither an ideal ratio nor a small aggregate remainder supplies a missing dynamic map.

The corresponding physical transformer remainder requires simultaneous
port and endpoint observations, including switch, probe and supply effects
[OP-TRF-07].

## Preparation, switching, material, supply, and calibration comparisons

These comparisons retain the original apparatus classes. A general work law
can be shared; a measured outcome for one device cannot be transferred to a
different winding, field, impact, pickup, or controller arrangement.

| Question and control | Reading A | Reading B and decisive observation |
|--------------------------------------|--------------------------------|--------------------------------------------------------|
| Prepared singular-component paths | Zero-state two-section circuit: heat $0$ | Prepared state in equation \eqref{eq:prepared-two-store}: heat $(1-e^{-2})/2$ J; cross finite component scalings and observe both independent states |
| Switching work beyond smooth zero-state transfer | Resistive regularization exports $3/8$ J by its declared endpoint | Reactive quarter-period transfer exports zero heat and leaves $1/2$ J in the auxiliary; integrate all ports on each finite path |
| Nearly cancelled, multiple, or nonideal modes | One known mode: at most $1/20000000000$ J under the stated current bound | Two modes at $\pm1$ V: $1/1000000$ J despite zero terminal signal; resolve internal branches, coupling uncertainty, and observation rank |
| Exact hidden mode | Empty branch: initial energy and release heat $0$ | Prepared microfarad branch: $1/2000000$ J and $3/8000000$ J; observe branch current/voltage and retained endpoint |
| Physical common-mode preparation | $u=-1/2$: input $95/2$ J and no half-period coil exchange | $u=1/2$: input $115/2$ J and coil works $(-19,+19)$ J; observe preparation sources and flux signs, retaining differential load backaction |
| Same switching endpoint, different partition | $A$ then $B$: heat pair $(3/8,3/32)$ J | $B$ then $A$: $(3/32,3/8)$ J; measure channels separately, not only total heat or final voltages |
| Actual switch/gap and release laws | Unit clamp: $3/2$ J receiver transfer | Two-volt clamp: $2$ J; distinguish ignition, restrike, overlap, gap, and release states through their branch products and endpoint capacitances |
| Finite capacitance ratios/orientations and limiting surfaces | $(C_1,C_2)=(1,2)$ F: final store $3/16$ J | Reversed ratio $(2,1)$ F: $11/16$ J; extend to declared finite smaller parasitics and wider ratios with their actual bandwidth; no finite outcome realizes zero time |
| Controlled cycle versus physical supply | Lossless 2 J preparation requires 2 J source input | Half-efficient preparation requires 4 J; observe supplies, receiver, conversion and thermal endpoints on the complete schedule |
| Missing preparation/reset and converter laws in other apparatus | Ideal recovery of a 1 J removal stores 1 J in the receiver | Half-efficient recovery stores $1/2$ J; observe every actual source, field/mechanical, gap, battery, and reset path for that apparatus |
| Identified hysteretic material and settling | Reversible magnetic cycle input $0$ | Periodic lag control $\pi/2$ J; measure internal-state closure and copper-subtracted magnetic input over declared periods |
| Realized thermal and sensor ports | Nonloading ideal sensor input and stored energy $0$ | Finite sensor input $1/2$ J and store $1/8$ J; record sensor supply, loading, temperature, and delay before extending to other feedback structures |
| Finite electromechanical bias supply | Treating unequal backaction as supplied at zero work misses 1 J | Plant receives 1 J actuator work, controller draws 3 J including its declared losses; source-off recovery control raises rail energy $1/2$ J |
| Channel-specific uncertainty | True quadrature work $0$ | Relative phase error gives $-\pi/2$ J; inject known polarity/gain/timing changes and calibrate joint port-placement and endpoint errors separately |

: Prepared and supplied controls. The source-off rail comparison, hidden-mode control, and material loop belong to their explicitly stated systems; they do not certify wider apparatus or unmeasured constitutive laws.

A comparison closes its bounded question only when the actual domain,
connections, event law, source settings, endpoint states, and uncertainty
meet the stated conditions. A measured mismatch is retained with sign,
magnitude, interval, and completed polarity, loading, timing, endpoint,
and model checks. Missing constitutive identification or inadequate
resolution leaves the question open. A finite family of successful
comparisons does not establish universal absence of a discrepancy.

# Relation to earlier work and limits of the mathematics

The carrier-relative gear construction in [Culpepper (2002)][gear] and the
rotating-coordinate mechanics in [MIT (2022)][frames] support the starting
kinematics. The individual work differences here follow from explicit
free bodies and exact integrals. They do not turn a rotation count into a
work measurement. The magnetic terminal relations in
[Haus and Melcher (1989)][magnet] distinguish finite inductive storage from
an ideal algebraic winding relation. The physical return, clamp, and supply
comparisons require further circuit laws given here. The metrological
framework of [JCGM (2008)][gum] motivates recording input quantities and
correlations; it does not provide a numerical uncertainty for this apparatus.

The universal-joint connection of a planet's rotation and revolution axes
also appears in [Nakagawa et al. (2018)][planet-takeoff]. That prior mechanical
design motivates comparison with actual lead-out geometry; the four-shaft
force and work laws here apply to the explicitly specified axial model.
For switched systems, observability depends on the stated transitions and
available outputs [Tanwani, Shim and Liberzon (2013)][switched-observability].
The present binary and energy-error questions additionally fix physical probe
loading, bandwidth and error sets. Their bounds are derived locally, rather
than inferred from a fixed-mode rank or a general observer-existence result.

The common ground with [Nilre and Herlin (2026)][main] is the separation of
complete physical ports, observation-dependent contributions, and independent
state endpoints. The additional controls expose contact, topology,
preparation, hidden-state, material, and calibration assumptions needed for
finite comparisons. Every theorem above is conditional on its equations.
The simple rolling and axial linkage results do not settle actual Cardan
transverse reactions. The Ravigneaux pitch example does not settle helical
thrust or every nonparallel contact. Finite compliant and restitution
controls do not identify a real impact law. Ideal terminal correspondence
and the elastic dynamic map have different state spaces and different
closure domains.

Exact polynomial or trigonometric controls can locate every power zero
algebraically. A root-free interval, a tangent zero, a persistent identity,
and equality of maximum absolute powers have different roles. A complete
event description for one specified smooth constitutive model does not
supply nonlinear switch laws for another. A same-sign narrow transfer may
also carry substantial work without any interior power zero. The power
integrals and their bandwidth requirement remain independent of event counts.

Physical magnetic identification, finite-source realization, and full
cycle closure remain empirical questions. Bounded results for prepared
paths and smooth-model correspondences leave their wider domains intact.
For symbolically evaluated accounts the numerical integration residual is
exactly zero, and the complete evaluated controls have $r_E=0$ from separate
works and constitutive endpoints. Defined but unevaluated works remain
unevaluated; a proved balance identity does not assign their individual values.
Physical model residuals remain unmeasured. They include omitted joint,
contact, bearing, windage, churning, switch, arc, magnetic, dielectric,
thermal, sensor, controller, and supply behavior. No aggregate model identity
assigns the magnitude or destination of an unexplained transfer.

# Conclusion

The fourth shaft turns a readout question into a loaded-machine test.
In the ideal one-receiver control, the output takes $7/3\,\mathrm J$
and carrier work changes by the same amount while the held ring carries
torque without ground work. The free bodies determine that result.
Actual U-joints require measured spatial reactions and application-point
motions. A dimensioned Oldham model, a finite clutch and specified stator
loads establish their own transfers and show which assumptions change.

The switched electrical apparatus has equally specific connections.
Full-to-tap return changes the circuit; its winding, cell, gate and thermal
states persist through the event. A clocked contraction theorem leaves
hybrid guards and material admissibility to their own analysis.
Generator comparisons require prime-mover, field and controller work
over matched service with actual preparation and reset.

Two ideal series banks can share an entire terminal history while retaining
$1$ or $5\,\mathrm J$. The finite reconnection graph has a proved
precommutation bound; its loaded binary discrimination is conditional on
the separation inequality of Section \ref{sec:binary-observation}.
The paired receiver-work ordering remains unevaluated and is not fixed by
the hidden-energy ordering.
The LC/shunt certificate establishes every charge-sign event for its
declared window. Three-store reset changes the final state with order;
the damped correspondence gives a physical preparation whose source work
is independently calculated. These are bounded results with explicit
state and topology domains.

The shared-output extension has a continuous prepared source-return witness
with positive receiver work and a decreasing independently defined store.
Its supplied machine admits no full-state cycle under the stated insulated
thermal law. In the separate electrical fixture, loaded complete-port
records leave a $1/100\,\mathrm J$ optimal worst-case initial-energy error
over two known states. Full-wave operation, heat rejection, richer sensors
and complete-service performance each require their own model and comparison.

The remaining experiments require measured laws, resolved work differences
and independent endpoint uncertainties. A small algebraic residual supplies
none of those observations. Any positive or negative physical remainder
retains its measured value, conditions and uncertainty until its cause is
identified.

\clearpage

\appendix

# Supplied machine and timing-drive specification
\label{sec:machine-specification}

This appendix defines the complete assembly used in the insulated-return
result of Section \ref{sec:shared-machine}.

Replace each ideal source by a field-excited armature, retaining its
$R_s=1\,\Omega$ resistor and primary-node/probe capacitances. The armature
current $a_j$ leaves the generator and enters $p_j$ through $R_s$;
$V_{gj}=p_j+R_sa_j$. Six rotors share one rigid shaft with angle $\phi$,
speed $\omega$ and total inertia $J=1\,\mathrm{kg\,m^2}$. Define
$\chi_j=\phi+(j-1)\pi/3$. Field current $f_j$ enters the generator's
positive field terminal from an independent $V_f=1\,\mathrm V$ supply.
With $L_a=L_f=1\,\mathrm H$, $M=1/10\,\mathrm H$ and
$R_a=R_f=1\,\Omega$, declare the reciprocal laws
\begin{align}
 E_{gj}&=\tfrac12L_aa_j^2+\tfrac12L_ff_j^2+M\cos\chi_j\,a_jf_j,\\
 \begin{pmatrix}L_a&M\cos\chi_j\\M\cos\chi_j&L_f\end{pmatrix}
 \binom{\dot a_j}{\dot f_j}
 &=\binom{M\omega\sin\chi_j f_j-(R_a+R_s)a_j-p_j}
          {V_f-R_ff_j+M\omega\sin\chi_j a_j},\\
 \dot\phi&=\omega,\qquad
 J\dot\omega=\tau_{\rm pm}-b\omega-\sum_jM\sin\chi_j a_jf_j,
 \\
 \tau_{\rm pm}&=8\,\mathrm{N\,m},\qquad
 b=\tfrac1{10}\,\mathrm{N\,m\,s/rad}.
 \label{eq:shared-machine-laws}
\end{align}
The magnetic matrix has eigenvalues at least $9/10\,\mathrm H$.
The primary-node equation now receives $a_j$, not the former ideal-source
current $(U_j-p_j)/R_s$. Remove that source forcing and diagonal when
forming its nodal law. Fixed electrical offsets add no independent rotor
angles. Direct differentiation of the independently declared magnetic
store and substitution of the winding laws gives
\begin{equation}
 \dot E_{gj}=-V_{gj}a_j+V_ff_j-R_aa_j^2-R_ff_j^2
                      +M\omega\sin\chi_j a_jf_j .
 \label{eq:shared-machine-conversion}
\end{equation}
The opposite rotor conversion follows by multiplying its torque equation
by $\omega$. Integrate both sides of each generator/fixture and
rotor/generator interface before cancellation. Source-resistor heat is
now $R_sa_j^2$.

The timing motor has angle $\theta$, speed $\Omega$, inertia
$J_t=1\,\mathrm{kg\,m^2}$, coil $L_t=1\,\mathrm H$,
$R_t=1\,\Omega$, torque constant $k_t=1\,\mathrm{N\,m/A}$ and
the corresponding back-emf constant. Four followers, indexed $k=0,1,2,3$,
have $x_k=h\cos(\theta-k\pi/2)$, $h=1/100\,\mathrm m$,
$K_k=(k+1)\,\mathrm{N/m}$ and $d_k=1\,\mathrm{N\,s/m}$.
With $x'_k=dx_k/d\theta$ and
$b_t=1/10\,\mathrm{N\,m\,s/rad}$, the supplied laws are
\begin{align}
 L_t\dot i_t&=u-R_ti_t-k_t\Omega,\qquad \dot\theta=\Omega,\\
 J_t\dot\Omega&=k_ti_t-b_t\Omega
           -\sum_kK_kx_kx'_k-\sum_kd_k(x'_k)^2\Omega,\\
 c_{jk}&=\tfrac12[1+\cos(\theta-k\pi/2)]\,\mathrm V .
 \label{eq:shared-timing}
\end{align}
The compatible SI values of the motor constants make the electrical and
mechanical conversion products equal. Cam springs store
$\sum_kK_kx_k^2/2$; follower heat is
$\sum_kd_k(x'_k\Omega)^2$. Thus the mechanical command has actual
spring and damping reactions. The cosine commands supply the same finite
gates as above. No physical capacitance depends on cam position in this
declared model; a variable-capacitance actuator requires its own conjugate
power and constitutive store.

For relative phase $\psi=\theta-\phi$ with target zero, two actual
$1\,\Omega$, $1/100\,\mathrm F$ sensing branches have voltages
$q_\phi,q_\omega$ driven by the independent transducer ports
$v_\phi=\sin(\phi-\theta)\,\mathrm V$ and
$v_\omega=(\omega-\Omega)(1\,\mathrm{V\,s/rad})$.
They obey $C_q\dot q_\nu=(v_\nu-q_\nu)/R_q$.
The command $U_c=8\,\mathrm V+q_\phi+q_\omega$ drives a
$R_u=1\,\Omega$, $C_u=1/100\,\mathrm F$ node supplying the motor:
\begin{equation}
 C_u\dot u=(U_c-u)/R_u-i_t .
 \label{eq:shared-controller}
\end{equation}
Each transducer work is $\int v_\nu(v_\nu-q_\nu)/R_q\,dt$;
the controller supply work is $\int U_c(U_c-u)/R_u\,dt$.
Their finite states, resistor heats and capacitor endpoints are retained.
These ideal transducer and regulated-supply laws have explicit external
ports; sensor backreaction and regulation losses beyond those ports remain
unidentified.

For this assembly replace the thermal bath by insulation: $\dot H=D_m$,
where $D_m$ contains all fixture losses except external receiver heat,
armature/field copper, both bearings, followers, timing coil, controller
and sensing resistors. Coefficients are temperature-independent.
The full 126-coordinate state includes the previous electrical, gate and
thermal states, twelve armature/field currents, both shaft angles and
speeds, timing-coil current and three sensing/supply voltages. Cam
positions are functions of $\theta$, with their stores retained.

The external signed powers are $\tau_{\rm pm}\omega$, each $V_ff_j$,
all 24 gate-supply products, the two transducer products and the controller
supply product; receiver export is $v_o^2/R_L$. There is no bath port.
Add $\sum E_{gj}$, $J\omega^2/2$, $J_t\Omega^2/2$, $L_ti_t^2/2$,
the cam springs and the three controller/sensor capacitors to the fixture's
independent store. The winding, shaft, motor, spring and caloric laws prove
its signed balance after each external work is integrated separately.
Electrical return into an enclosed generator is internal, never another
external source contribution.

For a transverse return, the differential of the flow-to-section map is
$[I-fn^T/(n^Tf)]DF_T$, restricted to section tangents, with the thermal
integral's derivative retained. Here $n$ is the section normal and $f$
the full vector field at return. This factor includes the change of return
time; holding the clock fixed would omit it. Smooth cams give no selector
reset. At a transverse clamp crossing the vector field is continuous,
so its saltation matrix is the identity although its variational Jacobian
changes. Grazing, tied crossings and nontransverse returns need separate
analysis. There is no fixed point at which to assign cycle multipliers.

The admitted current bounds imply input linkage at most
$15\,\mathrm{Wb\,turn}$, output linkage $85/2\,\mathrm{Wb\,turn}$,
generator linkage $11\,\mathrm{Wb\,turn}$ and output common flux
$65/2\,\mathrm{Wb}$ at every time. These bounds on the declared linear
model do not identify a material's saturation or remanence. The obstruction
also holds in its larger linear continuation. A bath law or permission for
thermal drift changes the full-state question. Electrical/shaft attraction,
heat-rejecting operation, physical material limits and complete-service
performance retain their separate scopes.

A distinct finite initialized control on $[0,1/200]\,\mathrm s$ uses
the earlier fixture preparation, $a_j=0$, $f_j=1\,\mathrm A$,
$\phi=\theta=0$, $\omega=\Omega=2\pi\,\mathrm{rad/s}$,
$i_t=8\,\mathrm A$, $u=8\,\mathrm V$, $q_\phi=q_\omega=0$ and $H=0$.
Its independent initial store is
$(3373203/40000+4\pi^2)\,\mathrm J$. Its actual final state and each
external power integral are defined by \eqref{eq:shared-machine-laws}--
\eqref{eq:shared-controller}; no evaluated trajectory or work ordering is
assigned here. This control supplies neither an initialized cycle nor an
attraction result. Positive magnetic matrices and locally Lipschitz laws
give uniqueness up to exit from a bounded operating region, which suffices
for the preceding return obstruction.

# Component bounds for the shared output
\label{sec:shared-bounds}

This appendix supplies the finite arithmetic behind
\eqref{eq:shared-box}, using precisely the graph and coordinate order of
\eqref{eq:shared-fixture-laws}. Currents, voltages and time are normalized
by 1 A, 1 V and 1 s; the following matrix coefficients are dimensionless.
Their rates correspond to inverse seconds in physical units. The inverse
inductance blocks are
\begin{equation}
 L_j^{-1}=I_3-2nn^T/11,\qquad L_o^{-1}=I_{13}-ss^T/17.
 \label{eq:shared-inverses}
\end{equation}
Each inverse-capacitance block on $(A_j,Q_{-j})$ is
$\left(\begin{smallmatrix}2&1\\1&2\end{smallmatrix}\right)/3$;
each $Q_{+j}$ diagonal is $1/2$; all other coordinates have inverse 1.
These follow by direct multiplication, so there is no numerical inverse.
The input-block determinant is $11/8$ and output-block determinant $17/4$;
the positive identity-plus-outer-product forms separately prove full rank.

With $G_0$ excluding selectors, write
\begin{equation}
 A_0=\begin{pmatrix}-L^{-1}&L^{-1}B^T\\-C^{-1}B&-C^{-1}G_0\end{pmatrix},
 \qquad b=\binom0{C^{-1}d(U)},\qquad
 \overline A=|A_0|+
 \sum_{j,k}\begin{pmatrix}0&0\\0&|C^{-1}a_{jk}a_{jk}^T|\end{pmatrix}.
 \label{eq:shared-majorant}
\end{equation}
Absolute values act entrywise. The selector upper conductance is one in
this normalization, so $|A(t)|\leq\overline A$ throughout the finite edge,
including independently varying channel gates. Summing its coefficients
for each coordinate gives the following bounds, identical across channels.

| Coordinate | Sum of majorant coefficients |
|----------------------------------|-----------------------------:|
| Input primary current | $21/11$ |
| Upper / lower input current | $69/22$ / $49/22$ |
| Each output branch current | $83/17$ |
| Receiver winding current | $4$ |
| $A_j$, $T_j$ | $73/30$, $61/10$ |
| $X_{+j}$, $Q_{+j}$ | $51/10$, $11/20$ |
| $X_{-j}$, $Q_{-j}$ | $41/10$, $53/30$ |
| $p_j$, $v_o$ | $11/5$, $11/5$ |
| Every probe voltage | $1/5$ |

: Exact infinity-norm majorant. Its maximum is $61/10$ and $\|b\|_\infty=1$.

For each physical capacitor with incidence $a_e$ and capacitance $c_e$ in
normalized units, define
$r_e=c_ea_e^TC^{-1}[-B,-G_0]$ and
$b_e=c_ea_e^TC^{-1}d(U)$. In the state box of radius $\eta=134/1939$,
its current law and triangle inequality give
\begin{equation}
 |i_e|\leq |r_ex_0+b_e|+\eta\|r_e\|_1+
 \sum_{j,k}|c_ea_e^TC^{-1}a_{jk}|
       (|a_{jk}^Tv_0|+\eta\|a_{jk}\|_1).
 \label{eq:shared-cap-current-bound}
\end{equation}
Every selector is bounded over its entire conductance range. Restoring
amperes yields these values for each physical component, not a bound on
an equivalent capacitor that could conceal branch current.

| Physical capacitor | Current magnitude upper bound, A |
|----------------------------------|------------------------------:|
| $A_j$ parasitic | $83667/193900$ |
| $T_j$ parasitic | $8311/7756$ |
| $X_{+j}$ parasitic | $187351/96950$ |
| $Q_{+j}$ parasitic and positive cell, each | $195067/387800$ |
| $X_{-j}$ parasitic | $87417/48475$ |
| $Q_{-j}$ parasitic | $36296/48475$ |
| Negative cell, $Q_{-j}-A_j$ | $49313/83100$ |
| Primary-node capacitor | $3413/9695$ |
| Output-node capacitor | $4887/19390$ |
| Each source probe | $2073/9695$ |
| Output probe | $2207/19390$ |

: All capacitor currents remain below the declared 2 A limit.

Copper, source-resistor and receiver currents have magnitude at most
$1+\eta=2073/1939\,\mathrm A$. Each secondary bleeder is bounded by
$2073/19390\,\mathrm A$, each probe resistor by
$2073/9695\,\mathrm A$, and each selector by
$3/10+2\eta=8497/19390\,\mathrm A$. Gates, including their capacitors,
carry at most 1 A by their independent RC law. Clamps carry zero.
The coarser $d_*=331/840$ state box would give an insufficient
$10051/2800\,\mathrm A$ bound for a capacitor current; that loose
bound is not evidence of a physical violation. The sharper majorant proves
the original limits without changing the circuit, preparation or interval.

For the observation theorem, group selector terms by $k$ across all six
channels. The permutation exchanging channels 1 and 2 commutes with the
base matrix, the forcing and each of the four grouped selector matrices.
It exchanges the corresponding primary, secondary, branch and probe
coordinates and fixes the output coordinates. Since it sends the prepared
difference to its negative, the connected difference trajectory stays in
the antisymmetric subspace. This verifies the receiver identity across
both constant commands and the entire exponentially varying edge.

\clearpage

# References {-}

1. Hob Nilre and Bo C. Herlin (2026), *Frames, Returns, and Port Power:
   Four central shafts, loaded reactions, and electrical counterparts*,
   30 September 2026. [Main article][main].
2. Martin L. Culpepper (2002), *2.000 Planetary Gear Application & Derivation*,
   MIT OpenCourseWare, *How and Why Machines Work*, Spring 2002, pp. 1–5.
   [Published course notes][gear].
3. Massachusetts Institute of Technology (2022), “Non-Inertial Linear and
   Rotating Reference Frames,” Chapter 31 of *8.01 Classical Mechanics*,
   Spring 2022 chapter edition, especially Section 31.4, pp. 7–15.
   [Published chapter][frames].
4. Hermann A. Haus and James R. Melcher (1989), *Electromagnetic Fields and
   Energy*, Prentice Hall, Englewood Cliffs, NJ, Section 9.7, “Magnetic Circuits.”
   [Author text hosted by MIT][magnet].
5. Joint Committee for Guides in Metrology (2008), *Evaluation of measurement
   data — Guide to the expression of uncertainty in measurement*,
   JCGM 100:2008, especially Sections 4 and 5. DOI:
   [10.59161/JCGM100-2008E][gum].

6. James F. Murray III (2017), *Switched Energy Resonant Power Supply System*,
   US20170169941A1, published 15 June 2017, Figures 11 and 19.
   [Patent publication][serps].
7. Belden Universal, “Connecting Multiple U-Joints,” technical guidance,
   accessed 29 September 2026. [Manufacturer guidance][joints].
8. Masao Nakagawa, Dai Nishida, Toshiki Hirogaki and Eiichi Aoyama (2018),
   “Investigation of Reducing Noise and Wide Geared for a Planetary Gear
   Train Using Universal Joint (Basic Investigation of Novel Component and
   Its Evaluation under Driving Tests),” *Journal of the Japan Society for
   Precision Engineering* **84**(1), 89–96. In Japanese, with English abstract.
   DOI: [10.2493/jjspe.84.89][planet-takeoff].
9. Aneel Tanwani, Hyungbo Shim and Daniel Liberzon (2013), “Observability for
   Switched Linear Systems: Characterization and Observer Design,”
   *IEEE Transactions on Automatic Control* **58**(4), 891–904.
   DOI: [10.1109/TAC.2012.2224257][switched-observability].

[main]: https://github.com/hobnilre/physics-gear
[gear]: https://ocw.mit.edu/courses/2-000-how-and-why-machines-work-spring-2002/432880e8fab4781d81ef88470751b397_PlanetaryGearTrains.pdf
[frames]: https://ocw.mit.edu/courses/8-01sc-classical-mechanics-fall-2016/mit8_01scs22_chapter31.pdf
[magnet]: https://web.mit.edu/6.013_book/www/chapter9/9.7.html
[gum]: https://doi.org/10.59161/JCGM100-2008E

[serps]: https://patents.google.com/patent/US20170169941A1/en
[joints]: https://www.beldenuniversal.com/resources/technical-information/connecting-multiple-u-joints
[planet-takeoff]: https://www.jstage.jst.go.jp/article/jjspe/84/1/84_89/_article/-char/en
[switched-observability]: https://doi.org/10.1109/TAC.2012.2224257
