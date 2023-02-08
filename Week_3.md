### Monday 2/6

For consistency's sake with Imai and Oya papers, find way to have Offset in PV diagrams to center at 0".

Look into `pvextractor.PathFromCenter(SkyCoord center, lenght of path, position angle)` --> initial plotting continues to place offset 0" at the origin. Manually center?

Plot path (either from `Path` or `PathFromCenter`) using method `get_xy(wcs)` --> returns list of end point coordinates, which can be plotted overtop the cube slice after converting to arrays.


### Tuesday 2/7

birdseye drive failed, resulting in a reboot --> in the short term, provision new data from laptop.

Divide large data cubes into sub-cubes +/-20 km/s from system velocity (5-6 km/s?).

Eventually, model fitting via birdseye... 

`ax.set_ylim()` and `plt.ylim()` not behaving as expected when attempting to adjust range of the velocity axis --> taking parameters as indices instead of velocities --> discrepancy between displayed velocity axis and axis attribute parameter interpretation --> Python struggling to read the axes from `pvextractor.extract_pv_slice`?

Temporary solution is "plug and chug" indices until image is framed as desired. 


### Wednesday 2/8

When birdseye was rebooted, my ssh tunnels were closed and must be set up again.

Center offset of PV diagrams on the protostellar outflow: slice perpendicular to the position angle of the outflow (142° in Imai et al. 2022). Slices taken along outflow should have P.A. = 232°.


### Thursday 2/9


### Friday 2/10
