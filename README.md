# **Bounds on Busy Turing Machines**
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)]()

If you are unfamiliar with the busy beaver function, check out my short paper on the topic found [here](https://drive.google.com/file/d/1Zr2gmRvZiiqaG6sjilIARYlqr3fyGTUH/view?usp=sharing).

[simulations.ipynb](https://nbviewer.jupyter.org/github/cristopolis/busy_tm/blob/main/simulations.ipynb) contains a Turing machine search, a custom loader, and a straightforward BB(n) simulation. If the .ipynb file is not loading on github, link to the notebook view is [here](https://nbviewer.jupyter.org/github/cristopolis/busy_tm/blob/main/simulations.ipynb)


| Command           | Description                    |
| ------------------| ------------------------------ |
| `bbn_finder()`    | BBn machine search method.     |
| `run_custom()`    | Custom loader for state/tape   |
| `bbn_ones()`      | Simulate BBn tape output       |

The machine search method, `bbn_finder()`, searches for BB(1-3). It uses a bottom up approach to find candidates, graphing out all active machines into their respective runtime and output catagories. Prelimanary checks for halt counts and other redundancies are implimented to reduce the necessary test cases.

The custom loader, `run_custom()`, is for testing custom tapes and state input pairs. This can be used to check any of the configuration proof steps in the paper, or to create your own input pair. Currently it is running step 2 from the lower bound proof for Wythagoras' machine (see section 3.5 of the paper)

The last function, `bbn_ones()`, simulates the BB(1-5) Turing machines directly, reporting on the runtime, steps, and tape output. This is a separate process from the finder, because it uses the proven bounds for 1's output by Turing Machine instead of shifts made. 