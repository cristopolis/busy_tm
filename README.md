# **Bounds on Busy Turing Machines**
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)]()

If you are unfamiliar with the busy beaver function, check out my short paper on the topic found [here](https://drive.google.com/file/d/1ZWqyUv3QAnn1spLqz5vBBY-HBQIlHYDI/view?usp=sharing).

[simulations.ipynb](https://nbviewer.jupyter.org/github/cristopolis/busy_tm/blob/main/simulations.ipynb) contains a Turing machine search, a custom loader, and a straightforward BB(n) simulation. If the .ipynb file is not loading on github, link to the notebook view is [here](https://nbviewer.jupyter.org/github/cristopolis/busy_tm/blob/main/simulations.ipynb)

The machine search method searches for BB(1-3). It uses a bottom up approach to find candidates, graphing out all active machines into their respective runtime and output catagories. Prelimanary checks for halt counts and other redundancies are implimented to reduce the necessary test cases.

The custom loader is for testing custom tapes and state input pairs. This can be used to check any of the configuration proof steps in the paper, or to create your own input pair. Currently it is running step 2 from the lower bound proof for Wythagoras' machine (see section 3.5 of the paper)
