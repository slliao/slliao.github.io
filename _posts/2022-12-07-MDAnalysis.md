---
title: MDAnalysis
categories: [MD, tools]
tags: [MDAnalysis, MD]
image:
  path: /img/md/
  width: 800
  height: 500
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

The data structure in MDAnalysis
![Atoms and atom groups](group_atoms.png)

Source: https://userguide.mdanalysis.org/stable/groups_of_atoms.html

![Atoms and atom groups](/img/md/group_atoms.png){:class="img-responsive"}

### Selecting atoms

Numerical ranges can be written as first-last or first:last where the range is inclusive. Note that ***in slicing, the last index is not included***.


```console
print(u.select_atoms('resid 50-100').n_residues)
print(u.residues[50:100].n_residues)
```
```
51
50
```
