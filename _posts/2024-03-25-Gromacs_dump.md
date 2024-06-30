---
title: GROMACS gmx dump
categories: [Molecular Dynamics, Gromacs]
tags: [Gromacs, MD]
---

## Gromacs

#### trr file
Files with the trr file extension contain the trajectory of a simulation. In this file all the coordinates, velocities, forces and energies are printed as you told GROMACS in your mdp file. This file is in portable binary format an can be read with gmx dump.

Dump structure at specify time in (ps)
```console
% gmx trajconv -dump 1000 -s nvt.tpr -s nvt.trr -o nvt_time_1000ps.g96
```
You can also get a quick look in the contents of the file (number of frames etc.) using:
```console
% gmx check -f traj.trr
```

#### tpr file
tpr file extension stands for portable binary run input file. This file contains the starting structure of your simulation, the molecular topology and **all the simulation parameters**. This file is in **binary format** it cannot be read with a normal editor. To read a portable binary run input file type:

```console
% gmx dump -s topol.tpr | less
```
You can also compare two tpr files using:
```console
% gmx check -s1 top1 -s2 top2 | more
```
