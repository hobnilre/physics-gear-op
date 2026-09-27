# Conventions and fixed controls

This file fixes the notation and illustrative values for *Finite Transfers
and Open Energy Balances*. Values are SI unless a unit is displayed.
A parameter choice is not an apparatus measurement. All calculations use exact
rational arithmetic, elementary closed forms, or untruncated matrix functions.
No numerical trajectory, integration routine, or measurement dataset is present.

## Common rules

- Positive power enters the named boundary. Integrate each signed effort–flow
  product on its stated interval before adding works.
- Force is paired with application-point velocity, couple with body angular
  velocity, complete voltage difference with entering current. Thermal export
  is negative and equals boundary temperature times outward entropy flow.
- Internal opposite sides cancel only on the same realized trajectory. Heat
  conversion inside a combined thermal boundary is not exported twice.
- Stores are evaluated from both endpoint states. Mathematical observation
  fields are not physical motor supplies. Physical moving supports and driven
  electrical returns have additional measured ports.
- Unless another interval is named, controls occupy [0,1] s. In explicit paths,
  t is numerical time in seconds, with coefficients carrying their SI units.
- J denotes total rotational inertia except in the impact subsection, where
  its locally defined J is impulse. C denotes electrical capacitance except
  capital member C in the compound train. The symbol a is centre distance in
  gears, reference ramp slope in the actuator, and locally specified quartic
  coefficient in the material model. These sections have disjoint boundaries.
- Effective coaxial-frame store: E^f = K^0 − ΩH. Relative kinetic store alone
  is K^f = K^0 − ΩH + JΩ²/2. Never compare these as the same store.
- Numerical integration residual: exactly zero. Omitted physical-law error:
  unknown unless an explicit independent constitutive control supplies it.

## I — Simple train

Three equally loaded planets, right-hand +z rates. Teeth (24,18,60), module
1/500 m, radii (3/125,9/500,3/50) m, centre distance 21/500 m. The three-planet
phase quotient is 28. Radial reaction uses the tangential pitch-contact law;
pressure-angle radial forces are excluded.

I_s = I_r = 3 I_p = J_c = 1 kg m²; planet mass 1 kg and carrier disc inertia
248677/250000 kg m². These are independently stipulated inertias, not a
uniform-disc density law. J = 4 kg m².

Steady rates (sun,ring,carrier,planet) = (7/2,0,1,−7/3) rad/s, sun torque
2 N m, duration 1 s. Shaft torques (2,5,−7); H = 13/6, K = 673/72,
carrier effective store 517/72 in their SI units. Steady shaft works are
(7,0,−7) J in ground and (5,−5,0) J in carrier coordinates.

Preparation multiplies those rates and sun torque by t. Ring/carrier torques
are 5t−595/36 and 673/36−7t. Ground/carrier/sun final effective stores are
673/72, 517/72, 127/72 J. Ring and ground observations coincide in this control.
The nonproportional history H=(13/6)t, Ω=t+b t(1−t), b=0 or 1, reconstructs
rates from H=4ω_c−(11/15)(ω_s−ω_c); it does not hold the ring during the ramp.

The locked approach fixes carrier rate one, sun 1+ε, ring 1−2ε/5, planet
1−4ε/3, with either sun torque 2 or 2ε. Loaded control: three unity lead-outs,
ground stators, passive output torque +1, zero drag. Shaft torques become
(2,−5,0), ground works (7,0,0), each receiver work −7/3 J. Added rotor and
output inertias remain symbolic positive values in the endpoint formula.

The full compliant control holds sun, ring, and planet spins; θ_c=t²/2.
Both contacts on each planet have overlap a t²/2−g, g=a/8, stiffness 2/a²,
damping 1/a². Gap [0,1/2], active contacts [1/2,1]. Individual spring endpoints
9/64 J, heat works −7/24 J, ground carrier work 99/32 J, ground final store
43/32 J. Carrier shaft works (83/112,415/224,0) J, field −1/2 J, final effective
store 11/32 J. These are linear pitch-compliance coordinates with finite
forces, not literal large-deflection tooth geometry.

## II — Linkage and mechanical extension controls

Eleven mountings: equal-angle correctly phased and quarter-turn Hooke against
two stators; ground-phased Hooke against ground; constant-ratio offset coupling
against two stators; bevel ratios 1 and 2 against two stators. Retain the
finite-interval periodic correction. Ground phase has its own unknown actuator.

Massless cycle control: planet/carrier rates (3,1), receiver torque −1, no
drag, interval [0,π/2]. Hooke works (3π/2,0,−3π/2); ratio-two bevel works
(3π,−π/2,−5π/2) J. Hooke angles lie strictly below π/2; cycle result holds
for any such angle with constant load and unchanged drag sign.

Unequal Hooke cosines (β1,β2)=(4/5,3/5), x=t, carrier rate one, transmitted
effort one, interval [0,π/4]. Support work π/4−atan(3/4) J. Large articulation
is an illustrative kinematic choice, not a practical-joint specification.
Accelerating rotor-pin control m_R a²=1, ω_c=t gives 1/2 J. Unit phase-actuator
and transverse-force calibration paths give 1 J through their own unit flows;
these values are not assigned to unidentified Cardan reactions.

Stator mounting comparison shared with the linked main article: planet rate
−14π/3, carrier 2π, drag torque magnitude 1/50, duration 7/2 s. Heat conversion
49π/150 and 7π/15 J; difference 7π/50 J.

Other local controls: compliant spring δ=t,k=2,c=1; two unit impact masses,
incoming (1,0), restitution 1/2; planet load fractions (1/2,1/3,1/6);
one pin couple 1/10 at relative rate −10/3; unit-torque reversal ω=1−2t;
radial guide m=1,r=1+t,ω_c=1; free spherical unit rotor ω=(1,0,2) observed
with Ω=(t,0,0). These are different physical boundaries and trajectories.

## III — Compound geometry and its electrical mapping

The five tooth quadruples, mesh signs, and ratios are:

| Teeth A,pA,pB,B | Signs A,B | R |
|---|---|---|
| 24,18,18,60 | −,+ | −5/2 |
| 20,22,20,62 | −,+ | −341/100 |
| 30,20,19,31 | −,− | 62/57 |
| 62,20,21,63 | +,+ | 30/31 |
| 100,58,59,101 | +,+ | 2929/2950 |

The massless control fixes carrier rate, applied A torque, and duration to one
in SI units. One stepped planet suffices; multi-planet phasing is additional.
The nine sides are signed copies of three shaft powers. Ground denominator
is the maximum absolute ground shaft power and must exclude zero from its
uncertainty interval. R=1 held-member ratios are undefined.

The separate Ravigneaux pitch example has A,B,R,S,L teeth (30,60,90,15,15),
module 1/30 m, short/long centre radii 3/4,5/4 m, and different sun planes.
Carrier one and ring zero give rates (A,B,S,L)=(−2,5/2,7,−5), shaft torques
(A,B,R,C)=(1,1,−3/2,−1/2), ground/carrier shaft ratio 1 and 6/5. This has four
contact equations, not a stepped-planet reduction.

Mobility mapping uses V=αω, I=τ/α, capacitance J/α². Electrical terminal
contributions and complete winding powers are explicitly distinct. The finite
Maxwell/transformer control uses each L0=1, k=1/2, node capacitance one,
branch resistance one, unit source at A, unit receiver conductance at B,
zero initial state, duration one. B has the four columns printed in the
manuscript. Magnetics map to elasticity, capacitance to inertia.

## IV — Winding and active-reference controls

Regular winding baseline: L1=1/25 H, ρ=1, k=19/20, positive polarity,
C=1/500 F, Rs=1/5 Ω, R1=R2=1/10 Ω, core conductance 1/100 S.
Cross all combinations of load {1/10,2/5} S, probe {0,1/10} S,
angular frequency {0,2π} s⁻¹, initial state {(0,0,0),(0,0,1)} in A,A,V.
Use u=cos(ωt) V over one second; there are 16 combinations per connection.
All seven works have exact matrix-function primitives. Isolated returns
are distinct conductors. The tapped receiver return parameter h is binary.

Commutation: keep capacitor at b–c; two physical receiver branches Ga at b–a
and Go at b–c. Three intervals, each 1/10 s, use conductances (1,0),(1,1),(0,1)
S; the separate gap control replaces the middle pair by (0,0). Copper and
core shunt remain in the equations even though suppressed in the diagram.

Attachment: R=C=1, imposed v=t, duration one; work 5/6 J, heat −1/3 J,
endpoint 1/2 J. A parallel unit-current receiver is a separate example giving
source work 4/3 J. Prepared RC probe control: C=1,V0=1,GL=1,GP=0 or 1.
Clamp control: L=1,I0=2, opposing clamp voltage 1 or 2, duration one.

Each singular winding law is derived separately. Unit perfect-coupling ramp
L1=ρ=1, zero copper, v1=v2=1, i2=0 gives final magnetic energy 1/2 J.
Other finite approaches are explicitly stated with their prepared-state scaling;
no single simultaneous singular model is assumed.

Active cell: J=C=α=1 in matching units, torque zero, reference 2t, interval one.
Compensation current −2 A gives 2 J final receiver store; disabled gives zero.
Reference driver Cd=1/200 F,Rd=3/4 Ω, command 2t+3/400 V, zero initial state.
Finite actuator: τa=1/10 s, La=Ra=1, C=1, reference slope 2, initial j=w=0.
Receiver endpoint (9+exp(−10))²/50 J. Prepared limiting pair L0=ε⁻¹,
k=1−ε², (h i1,i2)=(sqrt(ε)/2,sqrt(ε)/2) retains (2−ε²)/4 J.

## V — Passive preparation, hidden branches, and charge sharing

Series connection of parallel RC and parallel RL sections: C=L=RC=RL=1
for the prepared state (v,i)=(1,0), shorted terminal, one-second release.
Separate component-limit paths retain the impedance printed in the manuscript.
Resistive edge: unit capacitor at 1 V, R=ε, duration ε ln2; reactive edge:
L=ε², duration πε/2. No unspecified clamp impulse is assigned.

Hidden series RC branch: C=1/1000000 F,R=100 Ω,V0=1 V, terminal zero voltage,
release duration ln2/10000 s. n=0 is the decoupled topology. Single-mode
uncertainty control n=1/100, terminal current bound 1/1000000 A. Multiple
opposite modes have equal R,C,n and independent initial voltages +V and −V;
V=1 V gives total initial store 1/1000000 J despite zero terminal signal.

Common-current example: L1=1,L2=19,C=20/19, initial (10+u,u,0), u∈[−1,1/2].
Preparation is a one-second independent current ramp; operation [0,π].
Magnetic-only preparation is lossless unless Rj is explicitly added.

Charge sharing: C1=C2=2 F, initial (1,0) V, GA=GB=1 S, two stages of ln2 s.
Compare A then B with B then A. Unequal controls (C1,C2)=(1,2) and (2,1) F
keep initial voltages and use half-difference durations Ce ln2/G. Reversed
preparation (1,−1) applies only to the equal-capacitance control.
Released-parasitic comparisons use Cp={1/100,1/1000,1/10000} F and edge
durations {1/50,1/200} s. Exact Cp=0, duration=0, other orientations, and a
continuous ratio domain are not physical results of those comparisons.
Two wider finite controls use (C1,C2)=(1/2000,1) and (1,1/2000) F with
the same (1,0) V preparation, G=1, and two ln(2)/2001 s stages. Final stores
are 21/1334000 and 10667/21344 J; total heat is 5/21344 J in each case.

## VI — Material, thermal, sensor, and supplies

Thermal example D=1 W, CT=HT=2, θ0=0, duration one; excess energy 1−exp(−1) J
and exported heat exp(−1) J. Mesh friction μ=1/2,N=2,vslip=1, or μ=0 control.
Bearing and windage laws have symbolic positive coefficients and no invented
churning coefficient.

Magnetic ramp φ=t, R=1/5, h=0, quartic coefficient a=0 or 1, duration one.
Periodic material control a=h=ζ=1,R=1/5, φ=sin t, m=(sin t−cos t)/2,
interval [0,2π]; its initial periodic material state is explicitly prepared,
not assigned a preparation work. Transient material offset δ exp(−t) remains
in both endpoints and the period integrals.

Sensor control: source 1 V, R=C=1, zero initial voltage, interval [0,ln2].
Transducer: L=m=1,R=c=k=0,ge=1,gm=2,i=vm=1,vs=1,Fs=−2, duration one.
Converter delivery efficiency 1/2; bias coil Lb=1/2,Rb=1,ib=1. Finite rail
Cs=2,V=sqrt(4−3t), cutoff 1 V, load current 3/V. Separate recovery example
receives 1 W at efficiency 1/2 for one second, Cs=2,V0=1.

Complete elementary cycle: capacitor one; preparation v=t on [0,2], operation
v=(6−t)/2 on [2,6], zero state on reset [6,10] and hold [10,12]. Converter
half-efficiency is an explicit alternative to the ideal current controller.
The broader coil/pickup, field, moving-material, and spark-gap cycles retain
independent apparatus-specific supply and event laws.

## Observation bounds and figure colours

Transfer decision target U≤gap/4; physical residual bound sums independently
established endpoint and per-port uncertainties. Unknown physical δ is never
assigned a numerical prediction. A separately metered positive 1/4 J input
is an observation-chain challenge with omitted/included residuals +1/4 and 0.

Loaded carrier budget: observed |τ|≤8,|ω|≤4, errors both 1/100 in their units;
product uncertainty for two one-second works 1201/5000 J; total target 1 J.
Actuator endpoint: Ĉ=1,uC=1/100,|ŵ|≤2,uV=1/100; each bound 80501/2000000 J;
two-observation total target 1/10 J. These are requirements, not instrument
specifications. Phase control uses unit cosine peaks, duration 2π, φ=π/2,
relative phase error π/6. Gain example is +3/100 and −3/100. Endpoint example
uses true C=1,V=100, positive voltage error 1/100.

Blue elemA (#1F5FA8): plant/storage network and ideal reference comparator.
Orange elemB (#B8461B): external receiver branches. Green elemC (#2E7D32):
carrier/support/reference control and actuator. Purple elemD (#6A4C93):
thermal subsystem and heat delivery. Grey frameline (#555555): boundary or
geometric annotation. Colours identify subsystem roles consistently; no
geometrical proportion is asserted by the schematics.
