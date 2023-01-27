### Thursday 1/26

Data transferred over to my birdseye directory under the two directories: `CB68-Setup1` and `CB68-Setup2`, each containing three sub-directories: `images`, `moments`, and `plots`.

`images` contains a clean mask, a primary beam, and a primary-beam-corrected image for each molecular tracer. 

`moments` contains moment 0, 1, and 2 maps of each molecular tracer.

Open CARTA via ssh tunneling: https://casadocs.readthedocs.io/en/stable/notebooks/carta.html#Running-CARTA-at-NRAO

Eventually use parabolic outflow model (Lee et al. 2000; Oya et al. 2018) on CB68:
```math
z = CR^2, v_R = v_0 \frac{R}{R_0}, v_z = v_0 \frac{z}{z_0}
```
where z is the point on the z-axis, which is along the outflow with the origin at the protostar; R is the radial size of the outflow cavity; and $v_z$ is the velocity component along the z-axis. 

### Friday 1/27

Inspect data in CARTA, using Position-Velocity (PV) image generator widget: https://carta.readthedocs.io/en/3.0/analysis_tools.html#position-velocity-pv-image-generator 

Look into the documentation to create moment maps and PV diagrams using CASA toolkits (`ia.moments`, `ia.pv`) tasks (`immoments`, `impv`) and Python libraries (`spectral_cube` and `pvextractor`).

Waiting on lustre based in NM to be set up... 
