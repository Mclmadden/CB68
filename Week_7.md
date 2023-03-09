### Monday 3/6

Plan to re-measure P.A. of outflow? Imai et al. (2022) took P.A. = 142° from Wu et al. (1996) and Valée et al. (2000). 

[Dunham et al. (2014)](https://ui.adsabs.harvard.edu/abs/2014ApJ...783...29D/abstract) use P.A. = 135° for CB68 in Table 5, which was measured "by hand with a prototractor as the angle east of north." 

Compare the two position angles against CCH map --> Dunham et al. appears to fit the contours better.

Mix and match moment 0 maps and contours, starting with molecular tracers SiO, c-C3H2, H2CO, CH3OH, C18O, SO, CS, CCH. 

### Tuesday 3/7

Add black and red labels to indicate moment map and contour tracers respectively.

Disk(?) doesn't align when comparing most tracers to CCH and C18O disks. 

Look into obtaining the new data to plug into the PV diagram script --> large files to copy over to lustre and download locally? 

### Wednesday 3/8

Set up new weekly meeting? 

`images` directories from CB68 setups are much too large to download locally; each image file is 680 GB! --> work within birdseye or check out a node

Feedback on CCH and C18O disks not matching up with the rest of the tracers: check CARTA for plotting issue, and zoom in on the source to negate aliasing effects. 

Find better method than roughly picking pixel coordinates for `ax.set_xlim` and `ax.set_ylim`.

Scheduled meeting tomorrow to discuss. 

### Thursday 3/9

SSH tunneling not connecting to gateway (but connects to computer and node). May have to redirect connection to a different port in gateway.

Reserved `nmpost004` node for 14 days.

Figure out misalignment of some moment maps --> suspected errors in the file headers. 

Imai et al. (2022) Figure 2 shows integrated intensity maps of C18O, c-C3H2, and CCH with continuum extinction contours: C18O aligns with contours, while CCH doesn't align with contours... 

### Friday 3/10

