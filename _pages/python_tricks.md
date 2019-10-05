---
layout: single
author_profile: true
title: Python Tricks
permalink: /python_tricks/
---


These are some stupid little python tricks I use (mostly to make plots pretty).


## Formating for journals

This little bit of code makes plots that are very natural for two-column journals. You can adjust the fig_width to the journal of your choice

```python
import matplotlib.pyplot as plt

def set_journal(fig_width=245.26653, height_factor=1.):
    """
    Sets the matplotlib rc params to generate plots that are the proper
    size for two column journals. Simple specify the column width
    :param fig_width: Get this from LaTeX using \showthe\columnwidth
    """
    

    fig_width_pt =fig_width 
    inches_per_pt = 1.0/72.27               # Convert pt to inch
    golden_mean = (np.sqrt(5)-1.0)/2.0         # Aesthetic ratio
    fig_width = fig_width_pt*inches_per_pt  # width in inches
    fig_height = fig_width*golden_mean * height_factor      # height in inches
    fig_size =  [fig_width,fig_height]
    params = {'backend': 'ps',
              'axes.labelsize': 10,
              'font.size': 10,
              'legend.fontsize': 10,
              'xtick.labelsize': 8,
              'ytick.labelsize': 8,
              'text.usetex': True,
              'figure.figsize': fig_size,
              'font.family': 'serif'}
    plt.rcParams.update(params)
    
def reset():
    """
    Reset the plotting settings
    """
    
    plt.rcdefaults()

    #optional for notebook

    #%matplotlib inline
    #%matplotlib notebook


```

## CMAP arrays

I often want an to create a color map to color points based on values in an array. It is relatively easy to do, but I forget.

```python
import matplotlib as mpl
import matplotlib.pyplot as plt
import numpy as np

def array_to_cmap(values,cmap,use_log=False):
    """
    Generates a color map and color list that is normalized
    to the values in an array. Allows for adding a 3rd dimension
    onto a plot
    
    :param values: a list a values to map into a cmap
    :param cmap: the mpl colormap to use
    :param use_log: if the mapping should be done in log space
    """
    
    if use_log:
        
        norm = mpl.colors.LogNorm(vmin=min(values),vmax=max(values))
        
    else:
        
        norm = mpl.colors.Normalize(vmin=min(values),vmax=max(values))
        
        
    cmap = plt.cm.ScalarMappable(norm=norm,cmap=cmap)
    
    rgb_colors = map(cmap.to_rgba,values)
    
    return cmap, rgb_colors


```
