# extract_from_curvilinear_NEMO_grid

Some basic python code, showing the versions of packages, required to regrid the NEMO ocean model curvilinear grid to a rectilinear grid using the XESMF package. We then extract many variables, both physical and biogeochemical, from a hindcast reanalysis simulation of the NEMO-PISCES model forced by the Japanese Reanalysis 55do from 1958-2022.

The data extraction at point locations are those provided by Coraline Leseurre, interested in C13 measurements taken during hydrographic surveys.

It is very likely that my chunking could be better.

## Structure 
1. import packages
2. load model data (lazy)
3. do some housekeeping (renaming of coordinates, etc.)
4. fold two time dimensions (year and month) into each other to make one time dimension
5. apply chunking
6. regrid the arrays
7. load the observations for point locations
8. extract the data
