### Monday 2/27

Continue investigating `extent` keyword argument of `imshow`.

Ability to redefine plot boundaries but not fitting to given input values. 

Add other Archive files to PV diagram script: H2CO, SiO. c-C3H2

Exact Archive files given as:

```
H2CO 218.222 GHz as SPW 33 in Setup 1 (216-234GHz)
SiO 217.105GHz as SPW 20 in Setup 1 (216-234GHz) 
c-C3H2 217.822 GHz as SPW 22 in Setup 1 (216-234GHz)
CS 244.936 GHz as SPW 29 in Setup 2 (244-259GHz)
CCH 262004 GHz as SPW in 41 in Setup 2 (244-259GHz)
```

### Tuesday 2/28

Start making moment 0 and moment 1 maps with `spectral-cube`.

```
cube = SpectralCube.read(file)
moment0 = cube.moment(order=0)
moment0.writeto('moment0.fits') #saves moment map as FITS file
```
`moment` produces a Projection instances, which behave like Quantity objects to allow for easy file saving and conversion to WCS or FITS HDU.

View moment maps in `matplotlib` as with the original spectral cubes:

> format figure axes and colorbar

> add contour of continuum source, rather than the contours of the specific moment map (or PV diagram)

### Wednesday 3/1

Loop through tracers and create moment 0 maps with molecular tracer labeled on the figure. Saved as pngs.

For now, molecular tracer annotations are located in the bottom left corner of the figures because of difficulty obtaining the maximum y-axis value to automate placing the annotations in the upper left corner.

$$Moment 0: M_0 \int I dx$$

$$Moment 1: M_1 = \frac{\int I x dx}{M_0}$$

$$Moment N: M_N = \frac{\int I (x - M_1)^N dx}{M_0}$$

Moment1 maps encountering `RuntimeWarning: invalid value encountered in true_divide`. Resolved issue on GitHub page discusses fully masked cubes encountering NaN/NaN? 

Look at manually overwriting Angular Offset axes of PV diagrams or resolve `extent` keyword argument of `imshow`. 

> `ax.set_xticks` and `ax.set_xticklabels` 
> conversion between pixel coordinates and wcs

Copied `CB68-Setup1` and `CB68-Setup2` directories `moments` and `plots` to `/lustre/aoc/students/mmadden` in order to `scp` to local directories. `moments` contains 192 files, and `plots` contains 58 files.

### Thursday 3/2

Work on new data! 

### Friday 3/3 
