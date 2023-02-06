### Monday 2/6

For consistency's sake with Imai and Oya papers, find way to have Offset in PV diagrams to center at 0".

Look into `pvextractor.PathFromCenter(SkyCoord center, lenght of path, position angle)` --> initial plotting continues to place offset 0" at the origin. Manually center?

Plot path (either from `Path` or `PathFromCenter`) using method `get_xy(wcs)` --> returns list of end point coordinates, which can be plotted overtop the cube slice after converting to arrays.
