### Monday 2/13

Script works on archive data with adjustments to frequency/velocity slice and `set_aspect`.

Look into methods to overwrite the `imshow` axes to center the angular offset at the outflow center coordinates. 

`extent` parameter of `imshow` basing arguments off of pixel coordinates? --> not behaving as expected

### Tuesday 2/14 

Sent examples of CCH, CS, and SO PV diagrams to PIs --> asked about creating PV diagrams along the outflow axis (P.A. = 142°) simply by swapping out `PathFromCenter` variable.

Roundabout method to rewrite the axes labels in order to center the Angular Offset but possible easier solution. 

Issues with NM gygax system requiring maintenance throughout the day. 

### Wednesday 2/15

Ask about "inelegant" axes overwriting solution as a temporary fix? 

Difficulty tracing axes back to `imshow` using data created from `pvextractor.extract_pv_slice`.

E.g., CCH `print(im.get_extent())` returns the pixel coordinates `(-0.5,98.5,-0.5,475.5)` 

Experimenting with `extent` (and `aspect='auto'`) adjusts Angular Offset and Velocity boundaries but difficult to obtain accurate limits, e.g., `extent=(-10,10,30,-30)` returns plot displaying x spanning -2 to 2 and y spanning approximately 38.5 to 30.

### Thursday 2/16

Sent sample code to change plot axes labels. 


Removed warning produced when running data cube with a Stokes axis through `SpectralCube` instead of `StokesSpectralCube`; select specific warning from GitHub page: https://github.com/radio-astro-tools/spectral-cube/blob/master/spectral_cube/utils.py


```
import warnings
from spectral_cube.utils import StokesWarning
warnings.filterwarnings(action='ignore', category=StokesWarning,
                        append=True)
```

### Friday 2/17

Take a look at sample code that modifies axes the long way...

