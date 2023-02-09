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

When birdseye was rebooted, my ssh tunnels were closed and must be set up again. Following initial steps to set up vncserver --> still returning `channel 2: open failed: administratively prohibited: open failed`

Center offset of PV diagrams on the protostellar outflow: slice perpendicular to the position angle of the outflow (142° in Imai et al. 2022). Slices taken along outflow should have P.A. = 232°.

Take a ray from the continuum source location (Imai et al. 2022) direct along the outflow P.A., where a 0" angular offset would be the position along the ray with each PV diagram slice drawn perpendicular to the "outflow ray." Follow conventions for creating the PV diagrams in Oya et al. (2018) when possible. 

Peak position of 1.3mm dust continuum located R.A. = 16h 57m 19.647s, Dec = -16° 9' 23.94" (varies slightly from coordinates given in SIMBAD). 

Find method to set continuum source as angular offset 0" while default starts at endpoint of slice. 


### Thursday 2/9

[`wcs_pix2world`](https://docs.astropy.org/en/stable/api/astropy.wcs.WCS.html#astropy.wcs.WCS.wcs_pix2world) struggling with arrays given from `sample_points` attribute of PathFromCenter. --> referring back to original FITS cube confuses `wcs_pix2world` because of 4 axes (RA, Dec, Frequency, Stokes). --> `wcs.dropaxis(-1)` twice to remove Stokes and Frequency axes.

Able to take slices centered on outflow axis and create PV diagrams! 

Default x-axis still bases angular offset relative to starting point of slice, rather than the center point. 


### Friday 2/10
