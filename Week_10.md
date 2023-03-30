### Monday 3/27

Combine CS moments 0-2 maps into a single 1x3 figure for Overleaf draft --> difficulty with calling different WCS for `plt.subplots` `projection` parameter --> manually format moments 0-2 maps in Inkscape.

Change figure font to Roman serif in order to match Overleaf text.

Look into converting angular offset of PV diagrams into sky coordinates in order to determine 0 offset at the source coordinates and manually overwrite the x-axis.

### Tuesday 3/28 

Meeting with PI notes:

> edit jupyter notebooks with Archive data for GitHub posts

> adjust vmin for C18O (and c-C3H2 and H2CO) based on the zoomed window, rather than the drastic pbcorr edges of the whole field of view

> reverse CS moment 1 map `cmap='RdBu_r`

> schedule meeting with Japan team to discuss new data and modeling 

> create PV diagrams for meeting

Estimate secondary P.A. in CARTA by tracing high-velocity feature of CS: P.A. = 165 degrees.

Generate PV diagrams for CS, CCH, and c-C3H2 along both P.A. = 135 deg and P.A. = 165 deg. with slices "near," "middle," and "far" relative to the source. 

Send new PV diagrams to PI.

### Wednesday 3/29

Determine new vmin values for C18O, H2CO, and c-C3H2 channel maps in CARTA based on the zoom windows for figures. 

Re-assemble channel maps with updated colorscales in Inkscape. 

Work on cleaning up jupyter notebook scripts for GitHub postings using ALMA Archive data cube as an example: posted as `PV_diagram.ipynb` in `Python_samples` repository. 

Group meeting this afternoon. 

### Thursday 3/30 

PI obtained code for splicing together 2 matplotlib colormaps from Eric Koch (posted to Github).

Generate moment 0 maps with spliced cmap, combining `Grey` and `hot` with `pivot=0.2`. `pivot` parameter in defined function gives the fraction at which the cmaps are stitched together. 

Organize subplots in Inkscape, e.g. new moment 0 maps.

Continue working on Overleaf draft: Introduction, upload new figures, add sources. 

### Friday 3/31 

