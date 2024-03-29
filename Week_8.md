### Monday 3/13

Set up meeting for tomorrow to discuss new data PV diagrams, outflow position angle, and header offset.

### Tuesday 3/14

Lustre maintanance today at 14:00 ET. 

Set up TigerVNC to connect through node on work station and Windows machine. Error with TigerVNC on Macbook --> look into alternative VNC?

As long as Jupyter Notebook tunnel is open (in lustre, for example), and tunnel to node is open, then access TigerVNC from either machine.

Install CARTA on Macbook to determine moment map parameters in Python script. Annotate visible structures in Inkscape. 

Create channel maps spanning a range to cover molecular detections across all FITS cubes. N.B. CB68 systemic velocity ~5 km/s (Imai et al. 2022). 

Create PV diagrams of new data. 

Start with CS, CCH, c-C3H2, H2CO, C18O, SiO, and SO when working on longer Python scripts. 

### Wednesday 3/15 

Start Overleaf draft with basic section headers and use as place to draft figures and captions. 

Copy pre-written Python notebooks to NM lustre directory. Open tunnel from node with `jupyter lab --no-browser /lustre/aoc/students/mmadden`.

Working through VNC is much faster than directly on the work station. 

Upgrade Astropy version to be compatible with Numpy version.

Add other molecular tracers to pre-written PV diagram script --> check slice number in ds9.
  
> SiO = 240

> c-C3H2 = 239

> H2CO = 237

> C18O = 240

> SO = 238

`plt.subplots` dislikes new data headers having time in 'UTC' rather than 'utc' --> add `hdu.header['TIMESYS'] = 'utc'` to loops where `plt.subplots` is called. 

Most likely use `cube.spectral_slab(lowerlim, upperlim)` to extract smaller data cubes before running through `extract_pv_slice`, which results in kernel shutdown timeout with so many files.

### Thursday 3/16 

Takes ~90 minutes for PV script to run 7 spectral slabs through `extract_pv_slice` --> keep running in the background?

Misalignment of CCH and C18O compared to the other molecules could be due to CCH and C18O not necessarily tracing the isolate protostar but outflow structure. Double parabolic structure observed could hint at either a low-mass binary star with intersecting outflows or an infalling stream of gas and dust.

Velocity ranges of molecular tracers for channel maps:

> CS = 2 - 8.5 km/s

> CCH = 1 - 6.2 km/s

> c-C3H2 = 3 - 6.3 km/s

> H2CO = 2.5 - 8 km/s

> C18O = 3 - 7.5 km/s

> SiO = 2.2 - 6.5 km/s

> SO = 2.5 - 7.2 km/s

Set general range to 1 - 8.5 km/s for all channel maps --> narrow channels result in 45-55 figures per molecule in that range.

### Friday 3/17

Format figures for channel maps. 

Inspect the 7 molecules in CARTA to determine colormap stretch parameters for the moment maps script.

Experiment with bounds to zoom in on outflow regions, rather than the entire field of view --> offset to the northwest.

Generate channel maps with `plt.subplots` or generate individually and edit in Inkscape?

Throw figures into powerpoint draft to present to collaborators. 

Experiencing VNC dropping due to refused connection to port 22... 
