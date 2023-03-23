### Monday 3/20

Adjust zoom regions for channel maps --> estimate SkyCoord and convert to pixel coordinates with `skycoord_to_pixel`.

> x-axis boundary: RA = 16h 57m 20.4s, RA = 16h 57m 18.8s

> y-axis boundary: Dec = -16d 09m 30s, Dec = -16d 09m 08s

Remove axes labels and tick labels in preparation for channel map assembly. 

Locally download all individual figures to configure in Inkscape.

### Tuesday 3/21 

Import all channel figures into Inkscape to arrange into full channel maps.

Prepare for meeting with PI.

Meeting To-Do List:

> Need to remake channel figures with consistent colorscale determined by maximum cube value and $3\sigma$ for the minimum.

> Change colorscale for figures to `cmap='magma'` for better contrast. 

> Adjust channel map velocity range to 2 - 8 km/s because CCH originally set the minimum to 1 km/s, but CCH feature is duplicated, so one of them can be cut off.

> Enlarge and bold velocity text for individual figures in channel maps for legibility. 

> Add colorbars to the empty space in channel maps. 

> Choose consistent window size and vmin/vmax for moment 0 maps --> a little saturation at source location is acceptable, add 3-5 contours to make up for the loss.  

> Set moment map NaN values to 0 to hide mask features. 

> Potentially use CS as an example to create 1x3 figure with moments 0, 1, and 2 maps: magma, diverging red/blue, and a third cmap option. 

> Add subsections to the Discussion section in Overleaf draft with qualitative descriptions of each molecule's morphology seen in the channel maps. 

### Wednesday 3/22

Determine vmins/vmaxes for channel maps, and change cmap to magma.

Generate standalone colobars for channel maps.

Re-assemble channel maps in Inkscape with consistent colorscales: completed CS, CCH, c-C3H2, H2CO, C18O, SiO, and SO.

Prepare for group meeting.

### Thursday 3/23

Add contours to moment 0 maps to compensate for the saturation near the source.

Set NaN values in moment 0 maps to 0 to disguise mask features:

```
nans = np.isnan(data[0,:,:])
data[0,nans] = 0
im = ax.imshow(data[0,:,:], cmap='magma', vmin=vmin, vmax=vmax)
```

Determine a consistent vmin and vmax for all the moment 0 maps.

Create moment 0, 1, and 2 maps of CS --> numpy versions more recent than 1.23.5 return error with `cube.moment(order=0)` from SpectralCube: `AttributeError: module 'numpy' has no attribute 'bool'`

### Friday 3/24
