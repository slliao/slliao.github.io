---
title: "Wool's Critical Entanglement Molecular Weight"
categories: [Polymer Physics, Entanglement]
tags: [polymer, entanglement, molecular weight, rheology, tube model]
math: true
---

## Chain Entanglement: A Purely Topological Effect

Polymer chains have no covalent bonds between them — yet long chains resist flow in a way short ones do not. The reason is purely topological: chains cannot pass through each other. When a chain is long enough, surrounding chains form a persistent set of constraints that trap it. This is **chain entanglement** — and it is entirely a consequence of topology, not chemistry.

$M_c$ (Critical Entanglement Molecular Weight) marks the onset of this regime. Below $M_c$, a polymer melt flows like a simple liquid. Above it, viscosity scales steeply with molecular weight and the material develops a rubbery plateau — the hallmarks of an entangled network.

---

## Three Theoretical Foundations

### 1. Flory's Characteristic Ratio $C_\infty$

A freely jointed chain of $N$ bonds of length $b$ has a mean-square end-to-end distance:

$$\langle r^2 \rangle_0 = Nb^2$$

Real chains deviate from this because bond angles are fixed and rotational barriers correlate neighboring bond orientations. Flory captured this with the characteristic ratio $C_\infty$:

$$\langle r^2 \rangle = C_\infty N b^2$$

$C_\infty$ quantifies chain stiffness — it is the ratio of the true mean-square end-to-end distance to the ideal FJC value. Flexible chains have $C_\infty \approx 2$–$4$; stiff aromatic backbones can reach $6$–$10$. A stiffer chain sweeps out more volume per monomer, requiring more monomers to form a stable entanglement.

### 2. The Tube Model (de Gennes, Doi–Edwards)

In the tube model, each chain is confined by surrounding chains to a virtual tube. The chain moves by **reptation** — snake-like diffusion along the tube axis. Lateral motion is topologically forbidden.

The key length scale is the **entanglement strand**: the chain segment between two consecutive entanglement points. If this strand contains $n_e$ backbone bonds, its spatial extent (the tube diameter $d$) follows random-walk statistics:

$$d^2 = C_\infty\, n_e\, b^2$$

### 3. Wool's Geometric Factor

Wool (1993) introduced a factor connecting the local repeat-unit geometry to macroscopic entanglement. For a repeat unit with $z$ monomers per crystallographic c-axis repeat, backbone bond length $b$, and projected length $C$ along the chain axis, the ratio $(zb/C)^2$ measures how efficiently the backbone traverses space.

When $C \approx zb$, the chain is nearly fully extended and $(zb/C)^2 \approx 1$. When the repeat unit is compact or twisted ($C \ll zb$), the chain coils tightly, intersects neighboring chains more readily, and reaches the entanglement condition at lower molecular weight.

---

## The Formula

$$\boxed{M'_c = 30.89 \left(\frac{zb}{C}\right)^2 j\, M_0\, C_\infty}$$

This is Wool (1993), corresponding to Sperling *Introduction to Physical Polymer Science* (4th ed.), Eq. 10.59a.

| Symbol | Meaning | Units |
|--------|---------|-------|
| $z$ | monomers per c-axis repeat | — |
| $b$ | backbone bond length | Å |
| $C$ | projected repeat-unit length along chain axis | Å |
| $j$ | backbone atoms per monomer | — |
| $M_0$ | monomer molecular weight | g mol⁻¹ |
| $C_\infty$ | Flory characteristic ratio | — |

---

## Derivation

**Step 1 — Chain statistics.** For a real chain with $N$ backbone bonds:

$$\langle r^2 \rangle = C_\infty N b^2$$

**Step 2 — Entanglement strand.** The tube diameter is set by the entanglement strand of $n_e$ bonds:

$$d^2 = C_\infty\, n_e\, b^2$$

**Step 3 — Geometric constraint.** Wool's condition ties the tube diameter to repeat-unit geometry:

$$d^2 \propto \left(\frac{zb}{C}\right)^2$$

**Step 4 — Convert to molecular weight.** With $j$ backbone atoms per monomer and monomer mass $M_0$:

$$M_e = \frac{n_e}{j}\, M_0$$

**Step 5 — Assemble.** Combining steps 2–4 and inserting the prefactor 30.89 (which absorbs the tube-model geometric constant and the empirical relation $M_c \approx 2M_e$) gives the final expression.

**Simplified form for vinyl polymers.** Setting $z = 1$ and $(b/C)^2 \approx 1/30$ recovers (Sperling Eq. 10.59b):

$$M_c \approx 30\, C_\infty M_0$$

For simple backbones, $M_c$ is governed almost entirely by chain stiffness and monomer mass.

---

## Reading the Formula

$$M'_c \propto \underbrace{\left(\frac{zb}{C}\right)^2}_{\text{coiling efficiency}} \times \underbrace{j \cdot M_0}_{\text{mass per bond}} \times \underbrace{C_\infty}_{\text{chain stiffness}}$$

- **Coiling efficiency** — compact repeat units lower $M_c$; extended ones raise it.
- **Mass per bond** — heavier or more complex monomers push $M_c$ higher.
- **Chain stiffness** — stiffer chains need longer contour lengths to entangle.
- **Prefactor 30.89** — encodes the tube-model geometry and the $M_c \approx 2M_e$ empirical factor.

---

## Physical Consequences: Two Viscosity Scaling Regimes

The clearest experimental signature of $M_c$ is a change in how melt viscosity scales with molecular weight.

**Below $M_c$:** chains slip past one another freely:

$$\eta \sim M^{1.0}$$

**Above $M_c$:** stable entanglements form a transient network; chains must reptate to move:

$$\eta \sim M^{3.4}$$

Above $M_c$, the viscoelastic spectrum also develops a **rubbery plateau** — a frequency window where the material stores elastic energy rather than dissipating it. The plateau modulus $G_N^0$ is directly related to the entanglement strand molecular weight $M_e$:

$$G_N^0 = \frac{\rho RT}{M_e}$$

This provides an experimental route to $M_e$ (and hence $M_c$) from rheological measurements.

---

## References

1. Wool, R. P. (1993). *Polymer Interfaces: Structure and Strength*. Hanser.
2. Sperling, L. H. (2006). *Introduction to Physical Polymer Science*, 4th ed. Wiley. §10.4, Eqs. 10.59a–b.
3. de Gennes, P.-G. (1971). Reptation of a polymer chain in the presence of fixed obstacles. *J. Chem. Phys.*, 55, 572.
4. Doi, M. & Edwards, S. F. (1986). *The Theory of Polymer Dynamics*. Oxford University Press.
5. Flory, P. J. (1953). *Principles of Polymer Chemistry*. Cornell University Press.
