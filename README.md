# HBL_Parallel_Processing
A parallel processing program based on Dask for processing URI Hurricane Boundary Layer Model's Wind output.


## The Model: Hurricane Boundary Layer (HBL) Model

- A three-dimensional model developed with a focus on improving surface wind forecast during landfall of hurricanes.

- Horizontal and vertical resolution of the model is 1km and 30m; respectively.

- The wind outputs are saved at every minute interval.

- Model uses a vortex-following moving system. 

- Computational routines are written in Fortran and the model uses Intel’s Message Passing Interface (MPI) to run in parallel across different nodes and CPUs. 


## The Challenges

- Because of higher spatial and temporal resolution, output netCDF files can get very large (~20-30 GBs).

- Programs i.e. NCAR Command Language (NCL), Matlab takes longer time to process the data; usually an hour to process a HBL forecast data of a day (1440 minutes).

- In addition to that, Matlab and NCL doesn’t have parallel processing system.


## Why Parallel Processing?

- A parallel post-processing program for an MPI-based Hurricane Boundary Layer Model.
- 
- To meet the demand of operational forecast that requires faster & efficient analysis within a limited time range for decision making. 
- 
- To take the advantage of recent advancement in High-Performance computing system.
- 
- Significant progress in open-source software development. 



# Required Libraries

- [Dask](https://dask.org/)

- [Numpy](https://numpy.org/)

- [xarray](http://xarray.pydata.org/en/stable/)

- [Matplotlib](https://matplotlib.org/)

- [Pandas](https://pandas.pydata.org/)

- [cartopy](https://scitools.org.uk/cartopy/docs/latest/)

- [Geocat](https://geocat.ucar.edu/)

- [IPython](https://ipython.org/)

- [FFmpeg](https://github.com/kkroening/ffmpeg-python)

- [graphviz](https://graphviz.org/)
