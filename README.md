Python wrapper for MLDS R package 
[![Build Status](https://travis-ci.org/computational-psychology/mlds.svg?branch=master)](https://travis-ci.org/computational-psychology/mlds)

Contents
========

It contains:

- a python implementation that wraps the R package MLDS. This wrapper makes easier to analyse the data obtained in MLDS experiments. It also provides the extra functionality to using multi-thread, making the bootstrap calculation much faster.

- utilities for designing MLDS experiments (method of triads and quadruples)
- functions to simulate an observer performing an MLDS experiment (so far only for the method of triads).


Requirements
============

- Python modules: numpy, subprocess, multiprocessing and rpy2 (>=2.3.10)

- R (>=3.0), with the *MLDS* and *psyphy* packages already installed.
- Optional but recommended: *snow* package in R for multithreading.

Python module dependencies are installed automatically.

R packages must be installed manually, either from CRAN (see below)
or using the files provided in this repository (mlds/CRAN).


Installation
============

- Install R and the requirements within R: `install.packages(c("MLDS", "psyphy", "snow"))` (*snow* is optional)

##### For users
- Simply run `pip install https://github.com/computational-psychology/mlds/tarball/master`

##### For developers
- Clone the repository from github (`git clone https://github.com/computational-psychology/mlds.git`)
- Go to the root of the repository and run `python setup.py install -f` (you can also run `pip install -e .`)


Testing
=======
In a Python console, run:
```python
import mlds
mlds.test() # this should take around a minute
```


Usage examples
==============

- *examples/example.py* gives usage example for MLDS analysis
- *examples/example_stim_generation.py* gives usage example for designing the triads or quadruples.
- *examples/example_simulation.py* gives usage example for simulating an observer performing the method of triads.
- *examples/example_predict_thresholds.py* gives usage example for predicting discrimination thresholds from a perceptual scale, using signal detection theory assumptions. See Aguilar, Wichmann & Maertens (2017) for details.



Contact
=======
Questions? Feedback? Don't hesitate to fork, pull request, or 
contact me (guillermo.aguilar@mail.tu-berlin.de)

This repository has so far only been tested in Linux (Debian Jessie and Stretch, Ubuntu Xenial and Bionic) 


