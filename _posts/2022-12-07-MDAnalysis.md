---
title: MDAnalysis
categories: [Molecular Dynamics, analysis tools]
tags: [MDAnalysis, MD]
---

## MDAnalysis

### Atoms, residules, and segments

The data structure in MDAnalysis
![Atoms and atom groups](/img/md/group_atoms.png){:class="img-responsive"}

Source: https://userguide.mdanalysis.org/stable/groups_of_atoms.html

### Selecting atoms
Numerical ranges can be written as first-last or first:last where the range is inclusive. Note that ***in slicing, the last index is not included***.


```console
print(u.select_atoms('resid 50-100').n_residues)
print(u.residues[50:100].n_residues)
> 51
> 50
```
