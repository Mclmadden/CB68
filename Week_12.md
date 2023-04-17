### Monday 4/10

Inspect modeling scripts.

Schedule meeting with eDisk collaborator to discuss their data next week.

Busy schedule with PPVII this week in Japan.

### Tuesday 4/11

Meeting with PI

> Work on scheduling meetings with collaborators to discuss modeling 

> Leave outflow modeling to collaborators

> Shift focus to streamer modeling 

> Closer inspection of "J-shape" seen in channel maps

> Re-grid with `spectral_interpolate` method in spectral cube

> Trace J-shape and overlay onto combined channel maps over a small velocity range 

### Wednesday 4/12 

Set `spectral_slab` range for all cubes to 3.80 - 4.65 km/s to produce 6 channels.

Re-grid the other 6 molecular tracers to CS's spectral axis using `spectral_interpolate`.

Use the same vmin/vmax across all tracers or keep individual values? 

Export CARTA region tracing J-shape in CS channel 4.45 km/s. 

### Thursday 4/13

Read Nature article by Pineda et al. (2020) on protstellar streamer.

Read PRODIGE article by Valdivia-Mena et al. (2022) on streamer.

CARTA's polyline region type is not supported by CRTF or ds9 formats --> create region from separate lines and read in individually. 

### Friday 4/14

Read in CARTA regions exported into ds9 files with pixel coordinates --> easier to overplot onto channel figures that also use pixel coordinates.

Create 3-line regions that are exported all at once automatically with sets of endpoints stored in the file. 

CS J-shape only aligns with CCH feature! 
