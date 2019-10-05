---
title: "BALROG"
excerpt: "Unofficial GMB GRB Locations"
header:
  image: 
  teaser: /assets/images/balrog.png

---

I developed the BALROG algorithm a few years ago to try and deal with systematics in GRB locations from Fermi-GBM. The [first paper](https://academic.oup.com/mnras/article-abstract/476/2/1427/4670828/?redirectedFrom=fulltext) looked at the general idea. Next, our graduate student, Francesco Berlato examined the systematics of the technique in a [follow-up paper](https://iopscience.iop.org/article/10.3847/1538-4357/ab0413). 

We need to accurately locate GRBs so that follow-up telescopes can identify their afterglows and get redshifts.

## Basic idea
The idea is that we fit simultaneously for the position and location of GRBs rather than assuming templates. This is in contrast to the [classical location](https://iopscience.iop.org/article/10.1088/0067-0049/216/2/32/meta). The approach is relatively straight forward, but can be numerically intensive.

## Real time locations
Luckily, we have some genius students at MPE. [Felix Kunzweiler](https://fkunzweiler.github.io), Bjoern Biltzinger, and Francesco Berlato put together an amazing pipeline and [website](https://grb.mpe.mpg.de) that runs BALROG automatically and issues GCNs to alert the GRB follow-up community with our refined locations. 

## Controversy

As we are not the "official" GBM team, the American team is not so happy with our attempt to improve the GBM locations. GBM was built in Germany by the way. Recently, the America First team published a [paper](https://arxiv.org/abs/1909.03006).  

### Issues

The American GBM team utilized our open source software to perform this analysis. However, their software is *not* open source. If you have further questions about this analysis, feel free to contact me. I'll leave you with this picture:
![alt text](/assets/images/jochen.jpeg "Jochen")
