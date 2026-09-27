---
title: "Finite Transfers and Open Energy Balances"
subtitle: "Exact controls and decisive measurements for gears, windings, and their supplies"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-09-27"
abstract: |
  A changed observation frame, a moved electrical return, and a newly prepared
  internal state can produce different work readings for different reasons.
  We derive finite controls for the open energy questions of rotating gears,
  transformer readouts, switching paths, and their physical supplies. Each
  transfer is an integral of its own signed effort–flow product; every store
  is evaluated independently at both endpoints. A loaded axial gear control
  changes carrier work by 7 joules in one second. Two ordered charge-sharing
  paths exchange the heat deliveries 3/8 and 3/32 joule while ending in the
  same state. A finite reference actuator gives a negative, explicitly
  calculated departure from an ideal 2-joule receiver store. These predictions
  have distinct instrumented boundaries and conditional uncertainty budgets.
  The exact model residuals vanish; omitted material, support, switching,
  sensor, and supply effects have unmeasured magnitudes and signs. Finite
  comparisons distinguish specified readings without establishing an exact
  singular apparatus, a universal correspondence, or physical closure of
  a different apparatus.
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

Latest PDF on GitHub:

<https://github.com/hobnilre/physics-gear-op/blob/main/finite-transfers-and-open-energy-balances.pdf>

# Introduction: quantities that require separate experiments

[*Frames, Returns, and Port Power* (Nilre and Herlin, 2026)][main]
connects mechanical observation frames with electrical readout returns.
Its finite models motivate the following open comparisons. All numerical
values below are exact illustrative model predictions. There are no apparatus
measurements. Unknown physical discrepancies retain unknown magnitude and
sign. A specified alternative constitutive law can predict a difference;
an unspecified discrepancy cannot be assigned a numerical value in advance.

## Moving supports and mechanical preparation

A rotor read against two stators has count difference equal to their relative
turns. Under the same prescribed planet motion, moving a drag stator changes
its dissipation by $7\pi/50$ J in the control developed below; the physical
lead-out and its finite-interval phase correction remain to be determined
[OP-EPI-05]. Attaching the receiver also changes the planet free body: the
axial control here changes carrier work by $+7$ J, while the signed remainder
of a complete train with actual joints is unknown [OP-EPI-33].

On a transient, an effective rotating-frame store is $E^f=K^0-\Omega H$,
where $H$ is axial angular momentum. The same preparation gives different
stores and shaft works in ground, carrier, sun, and ring observations:
ground and carrier endpoint stores are $673/72$ and $517/72$ J. Whether
all physically reconstructed balances meet their separate uncertainties is
open [OP-EPI-01]. The shaft difference $W_j^0-W_j^f=\int\Omega\tau_jdt$
need not reside at pins: a held ring can have negative rotating-frame work
[OP-EPI-02]. Its total division into shaft and effective-field contributions
is history dependent: the worked shares change from $(13/12,13/12)$ J to
$(13/9,13/18)$ J with unchanged endpoints [OP-EPI-04].

A massless double-Hooke torque path has exactly zero support work over its
complete ripple period under constant load and unchanged drag sign; this
leaves the work of actual joints open [OP-EPI-06]. A ratio-two bevel path
instead exports $\pi/2$ J through its support in the stated ground-frame
cycle while that port does zero carrier-frame work [OP-EPI-07]. Compound
largest-port/ground-throughput ratios depend on the observation: the
close-ratio example gives $1$ in ground and $2950/21$ in the carrier frame
[OP-EPI-08]. A simple or stepped planet does not determine a Ravigneaux,
helical, bevel, or nonparallel-axis energy partition; a separate two-sun
example below gives $6/5$ in its carrier frame [OP-EPI-21].

A compliant engagement can jump from zero to $1$ W at continuous energy and
zero instantaneous transfer [OP-EPI-10]. A rigid restitution law instead
permits a negative kinetic jump, $-3/16$ J in the two-body control
[OP-EPI-22]. Compliance together with carrier acceleration adds both mesh
stores and the effective term $-\dot\Omega H$; the six-contact control predicts $7/4$ J of conversion, while the actual full-train
remainder remains undetermined [OP-EPI-23].
Unequal planet loading redistributes individual contact works, and a pin
couple adds $\int M(\omega_p-\omega_c)dt$, equal to $-1/3$ J in the stated
one-pin control [OP-EPI-24].

At fixed drive, locking relative motion leaves ground shaft works
$(2,5,-7)$ J; scaling the drive to zero gives $(0,0,0)$ J instead
[OP-EPI-12]. Coulomb
mesh conversion $\mu N|v_{\rm slip}|$ has zero frame difference for a fixed
physical contact [OP-EPI-13]. Bearing drag, windage, churning, and stored heat
require other laws: the thermal control retains $1-e^{-1}$ J of a 1 J
conversion rather than exporting it all [OP-EPI-25]. Radial planet motion
adds radial support work, $-3/2$ J in the guide control, and transverse
Coriolis force without total Coriolis power [OP-EPI-26]. A nonparallel
observation requires $-\symbf{\Omega}\cdot\mathbf H$; omitting a
transverse component loses $-1$ J in the vector control [OP-EPI-27].
A reversal can give zero net shaft work but absolute transfer $1/2$ J and
unit-drag heat $1/2$ J on the same interval [OP-EPI-28].

The transverse forces and bending couples of a double Cardan path are not
fixed by its axial torque relation, so their actual work is undetermined
[OP-EPI-30]. Unequal joint angles, carrier acceleration, and a physical
phase-reference actuator add separate endpoint or supply terms; their
finite control values below are nonzero even where an equal-angle steady
model omits them [OP-EPI-31]. The physical gear discrepancy remains an
unmeasured signed quantity, distinct from an exact zero algebraic residual
[OP-EPI-34].

## Electrical returns, finite states, and correspondence

A common change of voltage zero leaves complete port powers unchanged. A
conducting bond and chassis capacitor add actual work and storage: the
ramp control requires $5/6$ J of attachment-source work [OP-TRF-01].
A complete transformer cycle must separately include preparation, operation,
commutation, relaxation, and reset; finite passive relaxation leaves a
positive store and therefore need not complete the cycle [OP-TRF-05].
A linear reciprocal inductance does not specify saturation, remanence,
hysteresis, or temperature-dependent stores; the saturated ramp below needs
$1/4$ J more magnetic input than its linear control [OP-TRF-03].
Opening an energized winding, moving a return, and reconnecting a charged
capacitor retain distinct paths: the finite clamp control delivers $3/2$ J,
but that number is not the work of an unspecified winding switch
[OP-TRF-02].

An ideal compound correspondence does not fix finite actuator work or state
tracking. In the reference control, finite response replaces the ideal 2 J
by $(9+e^{-10})^2/50$ J [OP-TRF-12]. Perfect coupling, zero capacitance,
zero source resistance, a shorted output, and zero turns ratio each change
the constrained equations; perfect coupling alone retains a $1/2$ J
magnetizing store in the unit ramp [OP-TRF-04]. Crossed load, probe, drive
frequency, and prepared-state settings can change the sign of the difference
between receiver works; one-factor comparisons leave those interactions open
[OP-TRF-06]. Calibrated simultaneous port and endpoint observations have
not supplied the physical transformer residual [OP-TRF-07].

A voltage/count correspondence lacks a loaded dynamic correspondence unless
its independent stores and reaction ports also map. A common coordinate
shift alone misses 2 J of relative kinetic energy in the reference-only
control [OP-TRF-09]. Ideal transformer terminal contributions reproduce the
compound mechanical ratios, whereas complete physical ports define another
ratio; the stated physical-minus-mapped difference is $-241/100$
[OP-TRF-11].

## Prepared, hidden, switched, and supplied energy

Finite component limits can depend on a companion scaling; in the passive
two-store network the same vanishing capacitance has terminal limits
$3/2$ and $1/2\,\Omega$. Neither specifies the fate of incompatible
prepared energy [OP-LR21-01]. A smooth zero-state drive cannot determine
switching work of a prepared state; resistor discharge and reactive transfer
have different finite port works even as their durations decrease
[OP-LR21-02].

Near cancellation, terminal uncertainty can permit a large internal store;
with several modes it can leave an exactly unobserved energy direction
[OP-LR23-01]. At exact decoupling a prepared $1\,\mu$F capacitor has
$1/2000000$ J despite zero terminal hidden-mode current [OP-LR23-02].
Changing initial branch currents to $(10+u,u)$ A is a physical preparation:
the store $50+10u+10u^2$ J ranges from $95/2$ to $115/2$ J for
$-1\leq u\leq1/2$, with different flux signs [OP-LR42-02].

Two charge-sharing stages can commute as state maps while their heat
partitions interchange $3/8$ and $3/32$ J [OP-LR48-02]. Actual ignition,
restrike, clamp release, winding capacitance, and the complete release
connections can change that partition; their unmeasured switch laws leave
its sign and magnitude open [OP-LR48-03]. Finite capacitance ratios and
edge durations cannot realize zero capacitance or zero time, nor cover every
orientation or continuous limiting-ratio surface [OP-LR48-05].

A prescribed rest-to-rest trajectory can deliver 2 J while demanding
controller work; its balance does not establish that a physical supply will
produce the prescribed path [OP-LR49-01]. Finite preparation paths for some
coil and pickup arrangements do not specify the missing source, switch,
converter, battery, and arc laws of field, moving-material, or spark-gap
apparatus [OP-LR49-02].

An admissible magnetic material law has its own internal state: the explicit
periodic lag control converts $\pi/2$ J per cycle into heat, whereas a
reversible control gives zero [OP-LR57-01]. Sensors and thermal endpoints add
physical supply work and stored energy, including a $1/8$ J sensor-capacitor
endpoint in the finite charging control [OP-LR57-07]. Unequal electrical and
mechanical backaction requires a controller port $(g_m-g_e)iv$; a finite
bias supply must support that transfer, including any source-off return
[OP-LR59-02]. Finally, correlated gain, phase, timing, polarity, bandwidth,
loading, and endpoint errors can give a signed apparent energy residual;
the quadrature-phase control changes from zero to $-\pi/2$ J under the
specified relative phase error [OP-LR63-02].

The following derivations separate these questions by their actual boundaries.
The final comparisons specify held and driven quantities, different predictions,
and the uncertainty needed to distinguish them. A local exact control leaves
unidentified constitutive laws and broader apparatus questions open.

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

The numerical integration residual throughout this article is exactly zero:
no numerical integration is used. The model residual comprises omitted
physical laws and ports. It remains unquantified unless a separate,
explicit constitutive control calculates a particular contribution.

# Gears: free bodies, stores, and physical lead-outs

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
Their coordinate reconstructions do not physically remount any load.

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
They are coordinate terms, not physical motor or heat supplies.
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
$(13/6)(1/2+b/6)$ and $(13/6)(1/2-b/6)$ J. Thus $b=0,1$ give the
introduction's two pairs. The same endpoint total $13/6$ J follows by
integration by parts, not by presuming an equal division or a held ring
throughout a nonproportional preparation.

For a locked approach retain $\omega_c=1$, put $\omega_s=1+\epsilon$,
and obtain $\omega_r=1-2\epsilon/5$, $\omega_p=1-4\epsilon/3$.
At fixed $\tau_s=2$ the one-second ground shaft works are
$(2+2\epsilon,5-2\epsilon,-7)$ J. At
$\tau_s=2\epsilon$ they are $\epsilon$ times that triple.
Their exact limits are $(2,5,-7)$ and $(0,0,0)$ J. Carrier-frame works
vanish at the locked endpoint in both controls. The independent kinetic
endpoints are evaluated by \eqref{eq:frame}; a steady interval has identical
states at its ends, not necessarily zero energy.

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
A whole-cycle support null cannot be inferred for a partial cycle.

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
$\gamma=t$ supplies 1 J. None is supplied by a count alone.

The actual Cardan force and bending system requires its bearing constraints,
member stiffnesses, and application-point motions. A finite control with
$F_x=1$ N, $\dot x=1$ m/s over one second transfers 1 J; a fixed support
transfers zero at the same force. The same rule applies to a bending couple.
It specifies a force/displacement discrimination, not the unknown force in
an unspecified double Cardan device.

For a stator comparison reproducing the finite scale of
[Nilre and Herlin (2026)][main], take $\omega_p=-14\pi/3$,
$\omega_c=2\pi$, $d_0=1/50$ and duration $7/2$ s. The separate relative
drag integrals are $Q_0=49\pi/150$ and $Q_c=7\pi/15$ J, giving
$Q_c-Q_0=7\pi/50$ J. This is a change of physical mounting, not a
coordinate dependence of the heat produced by one mounting.

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
those independent physical ports and states.

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
specified comparisons.

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
trajectory. The two-sun example supplies no such missing law.

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
separate intervals; the actuator imposing $\delta$ has the opposite work.

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
it cannot realize a zero-time impulse.

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
unequal loading, and actual force laws remain separate physical questions.

With unequal planet fractions $(1/2,1/3,1/6)$, a steady total 7 J sun-contact
transfer divides into $(7/2,7/3,7/6)$ J rather than three $7/3$ J values.
The fractions specify a load-sharing law; they are not inferred from an
aggregate balance. A pin couple $M=1/10$ N m on a planet with
$\omega_p-\omega_c=-10/3$ rad/s gives pair work $-1/3$ J in one second.
Its two separately integrated sides are $M\omega_p$ and $-M\omega_c$.
Bearing heat or elastic torsion then needs an independently chosen law.
Each planet's force and couple channels must therefore be observed.

For a reversal, $\omega=1-2t$, $\tau=1$ on $[0,1]$ s gives
$W_{[0,1/2]}=1/4$ J and $W_{[1/2,1]}=-1/4$ J.
Net work is zero while $\int|P|dt=1/2$ J. A separate Coulomb drag of
unit magnitude converts $\int|\omega|dt=1/2$ J; treating its sign as
constant would give the wrong zero. A unit inertial rotor has equal endpoint
kinetic energies $1/2$ J on this prescribed reversal, and its inertial
actuator torque $\dot\omega=-2$ supplies works $-1/2,+1/2$ J on the two
halves. Any concurrent applied constant torque and brake require their
own compensating drive. The examples are separate effort laws, not a claim
that torque one alone produces that trajectory.

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
net Coriolis power. This distinction follows from the vector product itself.

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
train has this nonzero component.

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
and chassis capacitance are distinct branches with their own endpoints.

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
primitives, not a ratio of voltage integrals.

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
compatible initial states. Capacitor energy maps to inertia, magnetic
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

# Prepared states, hidden modes, and switching paths

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

# What must be measured

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
The numerical integration residual here is exactly zero, and each complete
ideal control has $r_E=0$ by independently calculated works and endpoints.
Physical model residuals remain unmeasured. They include omitted joint,
contact, bearing, windage, churning, switch, arc, magnetic, dielectric,
thermal, sensor, controller, and supply behavior. No aggregate model identity
assigns the magnitude or destination of an unexplained transfer.

# Conclusion

The mechanical comparisons distinguish changed frame works from changed
physical loads: the held-ring work is $0$ or $-5$ J in the two stated
observations, attaching three receivers changes carrier work by $+7$ J,
and the Hooke and bevel support controls give $0$ and $-\pi/2$ J.
History changes the shaft/field division; locking at fixed and scaled drive
gives different shaft-work limits. Other gear geometry, contact impulses,
compliance with acceleration, unequal loading, pin couples, radial motion,
nonparallel observation, reversals, transverse reactions, and phase actuation
retain the separate values and measurement conditions in the mechanical
comparison table. Heat conversion can be frame invariant while exported
heat differs from retained thermal energy.

Electrical coordinate invariance does not determine attached-return work,
loaded trajectories, or energized switching transfers. The RC attachment
requires $5/6$ J, the two clamp laws deliver $3/2$ and 2 J, and finite
reference actuation replaces 2 J by $(9+e^{-10})^2/50$ J. The constrained,
crossed-load, dynamic-map, and complete-port comparisons specify which
states and ports must accompany those readings. Calibrated physical gear
and winding remainders remain unknown in sign and magnitude.

Preparation can hide energy from a terminal, change coil work signs, and
select different singular approaches. Charge-sharing order interchanges
$3/8$ and $3/32$ J without changing final state. Common-current preparation
has the explicit $95/2$ to $115/2$ J range. Material lag, sensor stores,
converter losses, finite bias supplies, and reset paths each introduce
separately measurable work or endpoints. Polarity, gain, phase, timing,
loading, and store calibration must resolve each finite separation;
the phase control alone can change zero work to $-\pi/2$ J.

For each listed comparison, the exact model predicts its own signed works
and endpoint states. Whether the actual apparatus follows that model is
resolved by those measurements within independently established uncertainty.
An unexplained positive or negative remainder retains its value, conditions,
and completed checks; no omitted port receives it by definition.

\clearpage

# References {-}

1. Hob Nilre and Bo C. Herlin (2026), *Frames, Returns, and Port Power:
   Changing stores and open energy transfers in gears and transformer readouts*,
   27 September 2026. [Companion's main article, GitHub PDF][main].
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

[main]: https://github.com/hobnilre/physics-gear/blob/main/frames-returns-and-port-power.pdf
[gear]: https://ocw.mit.edu/courses/2-000-how-and-why-machines-work-spring-2002/432880e8fab4781d81ef88470751b397_PlanetaryGearTrains.pdf
[frames]: https://ocw.mit.edu/courses/8-01sc-classical-mechanics-fall-2016/mit8_01scs22_chapter31.pdf
[magnet]: https://web.mit.edu/6.013_book/www/chapter9/9.7.html
[gum]: https://doi.org/10.59161/JCGM100-2008E
