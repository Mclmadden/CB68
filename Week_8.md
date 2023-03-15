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

Copy pre-written Python notebooks to NM lustre directory. Open tunnel from node with `jupyter lab --no-browser /lustre/aoc/students/mmadden/<file>.ipynb`.

Upgrade Astropy version to be compatible with Numpy version.

Add other molecular tracers to pre-written PV diagram script --> check in CARTA for slice number in cube. 

`plt.subplots` dislikes new data headers having time in 'UTC' rather than 'utc' --> add `hdu.header['TIMESYS'] = 'utc'` to loops where `plt.subplots` is called. 

Most likely use `cube.spectral_slab(lowerlim, upperlim)` to extract smaller data cubes before running through `extract_pv_slice`, which results in kernel shutdown timeout with so many files.
