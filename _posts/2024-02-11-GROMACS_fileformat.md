---
title: Convert file format from GROMACS to xyz
categories: [Molecular Dynamics,GROMACS]
tags: [GROMACS]
---

## Convert g96 to xyz

```
gmx editconf -f input.g96 -o output.gro
```

```
obabel input.gro -O output.xyz 
```
