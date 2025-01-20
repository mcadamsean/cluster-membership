# cluster-membership
This repository contains my work completed at Western Washington University with the MWBest team of regional research institutions. All code is my own, but I have the observational data thanks to the MWBest team, and the Gala simulation thanks to WWU's Faith Benda. 

The membership process uses observational and simulated data in a 5D parameter space of position and motion (RA,DEC,PMRA,PMDEC,PX) to identify overdensities in the observed data, and establish membership probabilities for each star in the dataset.

The process is split into four notebooks:

1. **Data Processing**
   - Calculates extinction-corrected magnitudes and limits Gala and observed data to the adjusted completeness limit.
   - Converts RA and DEC to Galactic 'l' and 'b' coordinates, to be used in the field star extrapolation.
2. **Field Star Extrapolation**
   - Simulates a new background of field stars based on the row-wise density of observed stars in 'l' and 'b' space
3. **Membership Probability**
   - Calculates density within 5D position-proper motion space, and creates residual array by subtracting observed - simulated
   - Creates likelihood maps for cluster and field stars, based on Gala stars and the extrapolated field stars
   - Creates residual ratio for each 'voxel' within 5D space, and weights based on the cluster and field likelihood maps
4. **Comparison with established members and other targets**
   - Uses probabilities from previous notebook to assign to stars from other datasets and compare memberships

**Planned additions:**
1. PDF explainers for each notebook, and a workflow guide for the whole process
2. Update and upload in-depth notebooks:
    - Finding the completeness limit
    - Creating the field star extrapolations, both in 'l' and 'b' space and the previous radial method for comparison
    - Quering and examing the Besancon Galaxy Model's simulation for this FOV to compare with extrapolated datasets

**Known issues:**
  1. Density of extrapolated field stars seems to be a bit funny when we look at the low probability members plotted in RA,DEC space. We can see the distinct square of the bounding box used in the extrapolation process
  2. Edge-case issues for probabilities of stars that lay on the bounding box. Most evident when we look at Dr. Johnson's members in RA,DEC space.
