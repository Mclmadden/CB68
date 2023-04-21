### Monday 4/17

Create second J-shape region that traces H2CO (because tracer also has channel at 4.45 km/s) --> second J-shape aligns with the remaining tracers: c-C3H2, C18O, SiO, and SO.

Generate sets of 4.45 km/s channel images for each J-shape regions.

Read Nature article on protostellar streamers. 

### Tuesday 4/18 

Create polygon regions surrounding J-shape in CS and H2CO.

Read Valdivia-Mena et al. (2020).

Meeting with PI rescheduled to tomorrow.

### Wednesday 4/19

Repeat first coordinates of polygon to close shape. 

Meeting with PI

> "Offset" between CS/CCH and the rest of the tracers due to differing setups --> diffierent angular resolution and image size shifts pixel coordinates.

> Export region in wcs and convert to pixel coordinates based on each tracer's wcs. 

> Set NaN values in moment 1 and 2 maps to middlegrey color.

> Shift toward adding to the Overleaf draft: Observations from Imai et al. (2020), Methods from Oya et al. (2018) and relevant references, sections on jets and infalling streamers. 

### Thursday 4/20

Convert Jshape coordinates using `wcs.wcs_world2pix`.

Create figure with only 4.45 km/s channel in Inkscape, similar to the spliced cmap moment 0 map figure. 

Create Appendix channel map of all 7 tracers spanning 3.85 - 4.60 km/s to demonstrate J-shape. 

### Friday 4/21 

Matplotlib version doesn't support `copy` method for colormaps --> most recent version (3.7) doesn't work with current `plt.subplot` setting the argument `projection=wcs` --> force matplotlib to version 3.4.0 that is compatible with existing script and `copy`.

Add in new figures.

Continue adding to the Overleaf draft.
