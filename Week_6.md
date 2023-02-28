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

View moment maps in `matplotlib`.
