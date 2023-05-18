### Tuesday 5/16

Meeting with PI

> added packages to Overleaf to write molecules and units

> PI will eventually add method of creating the moment 0 maps with a CLEAN mask

> combine Methods and Results sections 

> apply Oya et al. (2018) outflow model to PV diagrams

> replicate Oya et al. (2018) Fig. 5/6 with CB 68 data 

> can skip SiO and SO for PV grids due to absence of extended emission

Correct molecule names and units in Overleaf draft. 

Awaiting reply from modeling teams. 

### Wednesday 5/17 

Start working on PV grids with offsets from the protostar: 0"-4.5" in increments of 0.5", followed by 5"-10" in increments of 1"

Create path using `PathFromCenter` along outflow axes (135° and 165°) --> take endpoints using `path.get_xy(wcs)` --> create second path using `Path` from protostar to the northeast endpoint, which halves the number of coordinates and able to apply `separation`.

Calculate distances between the protostar and coordinates along the path at aforementioned increments --> obtain the corresponding coordinates to those increments.

### Thursday 5/18 

Create paths using `PathFromCenter` centered on corresponding coordinates and perpendicular to outflow axes. 

Make PV diagrams.
