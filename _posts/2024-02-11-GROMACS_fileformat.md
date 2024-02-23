---
title: GROMACS: file format
categories: [Molecular Dynamics,Gromacs]
tags: [GROMACS]
---

## Convert g96 to xyz

```
gmx editconf -f input.g96 -o output.gro
```

```
obabel input.gro -O output.xyz 
```
