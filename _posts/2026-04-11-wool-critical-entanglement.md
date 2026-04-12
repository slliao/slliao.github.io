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

Wool (1993) introduced a repeat-unit geometry factor via a **critical overlap volume** argument. Entanglement is triggered when a chain's coil volume contains enough monomers from *other* chains to create unavoidable topological constraints. The number of foreign monomers inside the coil scales with chain dimensions and packing, and the ratio $(zb/C)^2$ emerges naturally from this condition — where $z$ is monomers per c-axis repeat, $b$ the backbone bond length, and $C$ the projected repeat-unit length along the chain axis.

This factor is a single-chain geometric quantity, distinct from the tube diameter $d$, which is a many-chain topological property. When $C \approx zb$ the chain is nearly fully extended and coils loosely; when $C \ll zb$ the repeat unit is compact, the chain fills its coil volume more densely with foreign monomers, and the entanglement threshold is reached at lower molecular weight.

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

**Step 3 — Critical overlap condition.** Wool's argument requires that the number of foreign-chain monomers inside a coil of $n_e$ bonds reaches a critical value. Working out the volume fractions, this condition introduces the geometric ratio $(zb/C)^2$ as a prefactor to $n_e$:

$$n_e \propto \left(\frac{zb}{C}\right)^{-2}$$

Chains that coil compactly (small $C/zb$) reach this threshold with fewer bonds; extended chains need more.

**Step 4 — Convert to molecular weight.** $n_e$ is a bond count; dividing by $j$ (backbone atoms per monomer) converts it to a monomer count, giving the entanglement strand molecular weight:

$$M_e = \frac{n_e}{j}\, M_0$$

**Step 5 — Assemble.** Combining steps 1–4 and inserting the prefactor 30.89 gives the final expression. Note that the formula yields $M'_c$, which corresponds to the onset of entanglement ($M_e$). The experimentally measured critical molecular weight $M_c$ — defined as the inflection point in the $\log \eta$ vs. $\log M$ curve — is empirically larger, with $M_c / M_e$ typically in the range 1.7–2.4 depending on chain flexibility. The prefactor 30.89 absorbs both the tube-model geometric constant and an approximate factor of 2 for this ratio.

**Empirical correlation for flexible backbones.** Across many common vinyl and addition polymers, Sperling (Eq. 10.59b) notes the empirical approximation:

$$M_c \approx 30\, C_\infty M_0$$

This is a data-fitted correlation, not a geometric derivation — the numerical coefficient is an average over a class of polymers and should not be applied to stiff or aromatic-backbone systems.

---

## Reading the Formula

$$M'_c \propto \underbrace{\left(\frac{zb}{C}\right)^2}_{\text{coiling efficiency}} \times \underbrace{j \cdot M_0}_{\text{mass per bond}} \times \underbrace{C_\infty}_{\text{chain stiffness}}$$

- **Coiling efficiency** — compact repeat units lower $M_c$; extended ones raise it.
- **Mass per bond** — heavier or more complex monomers push $M_c$ higher.
- **Chain stiffness** — stiffer chains need longer contour lengths to entangle.
- **Prefactor 30.89** — encodes the tube-model geometry constant and an approximate $M_c / M_e \approx 2$ factor (empirically 1.7–2.4; varies with chain flexibility).

---

## Physical Consequences: Two Viscosity Scaling Regimes

The clearest experimental signature of $M_c$ is a change in how melt viscosity scales with molecular weight.

**Below $M_c$:** chains slip past one another freely:

$$\eta \sim M^{1.0}$$

**Above $M_c$:** stable entanglements form a transient network; chains must reptate to move:

$$\eta \sim M^{3.4}$$

Above $M_c$, the viscoelastic spectrum also develops a **rubbery plateau** — a frequency window where the material stores elastic energy rather than dissipating it. The plateau modulus $G_N^0$ is directly related to the entanglement strand molecular weight $M_e$:

$$G_N^0 = \frac{\rho RT}{M_e}$$

This provides an experimental route to $M_e$ from rheological measurements. Note that the Doi–Edwards tube model introduces a prefactor of $\frac{4}{5}$, giving $G_N^0 = \frac{4}{5}\frac{\rho RT}{M_e}$; the form above is the classical rubber-elasticity (phenomenological) version. Both conventions appear in the literature — check which definition of $M_e$ a source uses before comparing values.

**$M_c$ and $M_e$ are not the same quantity.** $M_e$ is a network topology parameter extracted from $G_N^0$. $M_c$ is the inflection point in the zero-shear viscosity curve. They are related but distinct: the ratio $M_c/M_e$ typically falls between 1.7 and 2.4, and varies with chain flexibility. Treating them as interchangeable introduces systematic error.

---

## A Modern Perspective: Packing Length

Wool's geometric factor is an early-1990s framework. The field has since converged on a more unified quantity: the **packing length**, introduced by Fetters et al. (1994):

$$p = \frac{M}{\rho N_A \langle r^2 \rangle_0}$$

Here $\langle r^2 \rangle_0$ is the unperturbed mean-square end-to-end distance. In a polymer melt, Flory's theorem tells us that chains adopt ideal (unperturbed) conformations, so $\langle r^2 \rangle_0 = C_\infty N b^2$ — the same quantity used throughout this post. $p$ measures how densely a chain fills its own coil volume — a stiffer, more extended chain has a larger $p$. The entanglement molecular weight scales as:

$$M_e \propto p^3$$

This single relation unifies entanglement behavior across chemically diverse polymers and connects directly to measurable chain dimensions. Wool's formula and the packing length approach address the same physics from different angles; the latter is now the standard language in modern polymer rheology.

---

## References

1. Wool, R. P. (1993). *Polymer Interfaces: Structure and Strength*. Hanser.
2. Sperling, L. H. (2006). *Introduction to Physical Polymer Science*, 4th ed. Wiley. §10.4, Eqs. 10.59a–b.
3. de Gennes, P.-G. (1971). Reptation of a polymer chain in the presence of fixed obstacles. *J. Chem. Phys.*, 55, 572.
4. Doi, M. & Edwards, S. F. (1986). *The Theory of Polymer Dynamics*. Oxford University Press.
5. Flory, P. J. (1953). *Principles of Polymer Chemistry*. Cornell University Press.
6. Fetters, L. J., Lohse, D. J., Richter, D., Witten, T. A. & Zirkel, A. (1994). Connection between polymer molecular weight, density, chain dimensions, and melt viscoelastic properties. *Macromolecules*, 27, 4639–4647.
