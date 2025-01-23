### **Please view the Piecewise Membership Workflow PDF for more detailed documentation of the process**


**Requirements to start:**
1. An observed dataset that contains:
     - Position and motion information (RA,DEC,PMRA,PMDEC, Px)
     - Magnitude information, with extinction estimates
2. A simulated set of cluster stars (currently from the Gala simulation)
3. Simulated isochrone data for the cluster
4. External datasets to compare memberships with

**Workflow:**
1. Completeness limit
     - Calculates extinction-corrected completeness limit of observational data
2. Data processing
     - Corrects magnitudes for extinction
     - Limits data to extinction-corrected completeness limit of observational data
3. Field star extrapolation
     - Creates the simulated field star dataset, extrapolated from observed stars density in 'l' and 'b' space
4. Membership calculation
     - Sorts data into a 5D position-motion parameter space and calculates densities
     - Creates likelihood maps for the simulated field and cluster stars
     - Subtracts simulated densities from observed to reveal overdensities in the real data
     - Calculates ratio of stars in residual dataset to observed on a per-voxel basis
     - Creates a weighted residual using the field and cluster likelihood maps
5. Comparisons
     - Crossmatches with stars from other datasets to compare probabilities

I'll include the full process, potentially as a script rather than a notebook, soon.
