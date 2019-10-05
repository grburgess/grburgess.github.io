---
title: "IPN"
excerpt: "Trying to build a better IPN"
header:
  image: 
  teaser: /assets/images/ipn1.gif

---

Locating GRBs is a pain in the posterior. We've developed our [BALROG]() algorithm for GBM, but there are other ways to use non-imaging detectors to try and find these elusive objects. 

## History

The [Inter Planetary Network](http://ssl.berkeley.edu/ipn3/) (IPN) is an old idea that uses relative arrival time from a different gamma-ray sensitive satellites psread throughout the solar system to triangualte GRBs on the sky. The method is rather simple and it is one of the most arcurate ways to locate GRBs when an imaging telescope has not found them.

### Issues
The classic algorithm(s) for doing the triangulation are based off cross-correlations in time. This is likely ok, but they also make a lot of assumptions about Gaussian statistics (we have Poisson data) that can lead to poorly derived uncertainties in the predicted locations. We are attempting to fix this.

## Our Approach
We are attempting to forward model the problem by assuming that the GRB emits a latent light curve into all detectors and we must figure out the location on the sky that gives the appropriate time delay between them. We will attempt to do this with a non-parametric Bayesian hierarchical model.

The idea is still in alpha stage and I'm working with [Ewan Cameron](https://astrostatistics.wordpress.com). 

![alt text](/assets/images/ipn_orb.png "Attempted fit")
![alt text](/assets/images/failed_sphere.png "Attempted fit")
![alt text](/assets/images/ipn_lc.png "Attempted fit")


