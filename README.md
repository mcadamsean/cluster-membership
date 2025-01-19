# cluster-membership
This repository contains my work completed at Western Washington University with the MWBest team of regional research institutions. 

The membership process uses observational data in a 5D parameter space of position and motion (RA,DEC,PMRA,PMDEC,PX) to:

  1. Create a simulated dataset of field stars, using the field density outside the cluster tidal radius to extrapolate a field density "behind" the cluster stars.
  2. Use the Gala simulation (ran by Faith Benda, WWU) to create a "cluster likelihood map" that tells us where we should be expecting cluster stars, according to the simulation.
  3. Use the simulated field stars to create a "field likelihood map" that tells us where we expect field stars, according to analysis of the observational data.
  4. Assess overdensities found in the observational data, and compare them to the two likelihood maps.
  5. Create and assign a probability of membership that represents the significance of the overdensity of observed data compared to simulated data, and weight that with the two cluster likehood maps.
  6. Compare new membership probabilities with members that have previously been established in published literature.

The entirety of the process, excluding the Gala simulation that is provided via .fits file, will be contained within the main membership notebook. The process of simulating the background field is expanded upon in the supplementary notebook, and contains comparisons to other methods of simulating this area of the sky.
