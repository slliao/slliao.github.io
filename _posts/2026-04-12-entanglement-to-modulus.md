---
title: "From Entanglement to Modulus: Rubber Elasticity of Polymer Networks"
categories: [Polymer Physics, Mechanical Properties]
tags: [polymer, entanglement, modulus, rubber elasticity, viscoelasticity, rheology]
math: true
---

## Overview

[Part 1]({% post_url 2026-04-11-wool-critical-entanglement %}) established that above the critical entanglement molecular weight $M_c$, polymer chains form a persistent topological network. This post asks the next question: **what are the mechanical consequences?** Specifically, how does that network resist deformation, and how does the molecular structure — chain stiffness, repeat-unit geometry, monomer mass — determine the modulus?

---

## Entanglements as Temporary Crosslinks

The key insight is an analogy with chemically crosslinked rubber. In a vulcanized network, covalent crosslinks pin chain segments together and store elastic energy under deformation. Entanglements do the same thing — but transiently. On timescales shorter than the reptation time $\tau_d$ (the time for a chain to escape its tube), the entanglement network is effectively permanent and responds elastically.

**Affine network model.** Treat each entanglement strand as an entropic spring. A strand of $N_e$ monomers between two entanglement points has a free energy:

$$f = \frac{3k_BT}{2\langle r_e^2 \rangle}\, r^2$$

When the network deforms affinely (each strand deforms proportionally to the macroscopic strain), the elastic free energy density sums over all strands. The result is the **shear modulus**:

$$G = \nu_e k_B T$$

where $\nu_e = \rho N_A / M_e$ is the number of elastically active strands per unit volume. Substituting:

$$\boxed{G_N^0 = \frac{\rho R T}{M_e}}$$

This is the **plateau modulus** — the modulus of the entanglement network in the rubbery regime. A lower $M_e$ means more strands per unit volume and a higher modulus.

---

## From Shear Modulus to Tensile Modulus

For an incompressible material (Poisson's ratio $\nu \approx 0.5$, which holds for rubber-like networks), the tensile (Young's) modulus is:

$$E = 2G(1 + \nu) \approx 3G_N^0$$

So:

$$E \approx \frac{3\rho RT}{M_e}$$

This is the modulus measured in the rubbery plateau regime — above $T_g$, at a strain rate fast enough that chains cannot reptate on the experimental timescale ($\omega \gg \tau_d^{-1}$, so the entanglement network behaves elastically), yet slow enough to remain out of the glassy regime ($\omega \ll \omega_g$).

---

## Closing the Loop: Molecular Structure → Modulus

Part 1 showed that $M_e \approx M'_c / 2$, where $M'_c$ is given by Wool's formula. Substituting:

$$G_N^0 \approx \frac{2\rho RT}{30.89\left(\dfrac{zb}{C}\right)^2 j\, M_0\, C_\infty}$$

Every parameter here is a molecular property:

- $(zb/C)^2$ — repeat-unit coiling efficiency
- $j\, M_0$ — mass per backbone bond
- $C_\infty$ — chain stiffness

**Reading the modulus expression:**

- **Stiff chains** (large $C_\infty$) → large $M_e$ → fewer entanglement strands per volume → **lower** $G_N^0$.
- **Compact, flexible repeat units** (small $(zb/C)^2$ *and* small $C_\infty$) → small $M_e$ → dense entanglement network → **higher** $G_N^0$.
- **Heavy monomers** (large $M_0$) → fewer strands per unit volume → lower $G_N^0$.

A concrete comparison: polyethylene (PE) has an extremely flexible backbone ($C_\infty \approx 6.7$, small $M_e \approx 1.2$ kg/mol) and a plateau modulus $G_N^0 \approx 2.6$ MPa. Polystyrene (PS), with its bulky phenyl side group and larger effective chain dimensions, has $M_e \approx 13$ kg/mol and $G_N^0 \approx 0.2$ MPa — more than ten times lower.

**Important distinction.** Stiff-backbone polymers such as polyimides do have very high moduli (~3 GPa), but that is the *glassy-state* modulus, governed by backbone rigidity and intermolecular forces (e.g. $\pi$–$\pi$ stacking). The plateau modulus $G_N^0$ is a property of the *rubbery* entanglement network — a completely different regime — and does not follow the same trend.

---

## The Viscoelastic Spectrum

The modulus of a polymer melt is not a single number — it depends on the timescale (or frequency) of deformation. Three regimes emerge from the interplay of $M_e$, reptation time $\tau_d$, and the glass transition:

| Regime | Frequency | $G'(\omega)$ | Physical picture |
|--------|-----------|--------------|-----------------|
| Glassy | $\omega \gg \omega_g$ | ~1 GPa | Backbone stiffness and secondary bonds dominate; chains are frozen |
| Rubbery plateau | $\tau_d^{-1} \ll \omega \ll \omega_g$ | $G_N^0 \sim 10^5$–$10^6$ Pa | Entanglement network bears load; chains cannot reptate on this timescale |
| Terminal flow | $\omega \ll \tau_d^{-1}$ | $\to 0$ | Chains reptate out of tubes; network dissolves; viscous flow |

$M_e$ controls two things in this spectrum:

1. **Height of the plateau** — $G_N^0 = \rho RT / M_e$. Smaller $M_e$ raises the plateau.
2. **Width of the rubbery window** — the reptation time scales as $\tau_d \sim M^3$ (in the simplest Doi–Edwards model). A higher-$M_e$ polymer has fewer entanglements per chain, a shorter reptation time, and a narrower rubbery window.

---

## Beyond the Melt: Solid-State Strain Hardening

The entanglement network does not disappear when a polymer cools below its glass transition temperature $T_g$. The topological constraints are **frozen** into the glassy solid. While $M_e$ does not strongly influence the initial linear elastic modulus (which is governed by intermolecular forces and backbone stiffness), it dictates **large-strain plastic deformation** — the behavior that determines whether a material is tough or brittle.

When a glassy polymer is strained beyond its yield point, the amorphous chains are forced to flow plastically. The frozen entanglement network resists this flow and gives rise to **strain hardening**:

**Strain hardening modulus $G_R$.**
The resistance to plastic flow scales inversely with entanglement strand length:

$$G_R \propto \frac{1}{M_e}$$

The proportionality constant is set by the energy scale at which the network was frozen — near $T_g$, not room temperature, since the glassy entanglement topology reflects conformations locked in at $T_g$. Polymers with dense entanglement networks (small $M_e$) show strong strain hardening. Polycarbonate (PC, $M_e \approx 1.6$ kg/mol) is a classic example: it cold-draws extensively before fracture and is famously impact-resistant. The entanglement network distributes and stores strain energy across the sample, preventing localized crack propagation.

**Natural draw ratio $\lambda_{max}$.**
The maximum extension ratio before entanglement strands pull taut scales as:

$$\lambda_{max} \propto \sqrt{M_e}$$

A larger $M_e$ means longer strands between entanglement points, so the chain can be stretched further before going taut. However, a sparse entanglement network (large $M_e$) also means fewer strands to distribute stress. Polystyrene (PS, $M_e \approx 13$ kg/mol) illustrates the failure mode: PS has a large $\lambda_{max}$ in principle, but its sparse entanglement network transmits stress so poorly that **crazing** (formation of fibrillar microvoids) sets in long before the chains approach their maximum extension. PS fails in a brittle manner under impact.

The contrast between PC and PS is therefore a direct consequence of their $M_e$ values — not their backbone stiffness per se, but the density of topological constraints frozen into the glassy state.

---

## $M_c$ vs. $M_e$ Revisited

The plateau modulus is set by $M_e$, not $M_c$. The viscosity kink at $M_c$ and the plateau modulus at $G_N^0$ are two experimental windows into the same entanglement network, but they probe it differently:

- $G_N^0$ measures the **density of entanglement constraints** (equilibrium elasticity).
- The $\eta \sim M^{3.4}$ onset measures the **dynamical effect** of entanglements on chain mobility.

The empirical ratio $M_c / M_e \approx 2$ (ranging 1.7–2.4) reflects this: the viscosity transition requires roughly twice the entanglement strand length because a chain needs multiple entanglements along its contour before reptation dynamics dominate over Rouse dynamics.

---

## Summary

The chain from molecular structure to macroscopic modulus is:

$$\underbrace{(zb/C)^2,\; j,\; M_0,\; C_\infty}_{\text{molecular parameters}} \xrightarrow{\text{Wool}} M_e \xrightarrow{\text{rubber elasticity}} G_N^0 = \frac{\rho RT}{M_e} \xrightarrow{\nu \approx 0.5} E \approx 3G_N^0$$

The entanglement strand molecular weight $M_e$ is the single quantity that bridges chemistry and mechanics:

| $M_e$ role | Observable |
|---|---|
| Sets entanglement strand density | Plateau modulus $G_N^0 = \rho RT / M_e$ |
| Controls rubbery window width | Reptation time $\tau_d \sim M^3 / M_e^2$ |
| Governs solid-state strain hardening | $G_R \propto 1/M_e$ |
| Sets maximum draw ratio | $\lambda_{max} \propto \sqrt{M_e}$ |
| Determines ductile vs. brittle failure | Small $M_e$ → tough (PC); large $M_e$ → brittle crazing (PS) |

---

## References

1. Treloar, L. R. G. (1975). *The Physics of Rubber Elasticity*, 3rd ed. Oxford University Press.
2. Doi, M. & Edwards, S. F. (1986). *The Theory of Polymer Dynamics*. Oxford University Press.
3. Rubinstein, M. & Colby, R. H. (2003). *Polymer Physics*. Oxford University Press. Ch. 7–9.
4. Ferry, J. D. (1980). *Viscoelastic Properties of Polymers*, 3rd ed. Wiley.
5. Fetters, L. J., Lohse, D. J., Richter, D., Witten, T. A. & Zirkel, A. (1994). Connection between polymer molecular weight, density, chain dimensions, and melt viscoelastic properties. *Macromolecules*, 27, 4639–4647.
