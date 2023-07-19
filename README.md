# How to install LALSuite in a Linux desktop machine

This is a short note about installing [LAL](https://git.ligo.org/lscsoft/lalsuite), and the necessary dependencies in a Linux machine from scratch. 

LAL speaks in Python, so we need to install a Python distribution and interpreter first. I like [Anaconda](https://docs.anaconda.com/free/anaconda/install/) because it makes it nice and easy to install Python packages and interpreters from a terminal, manage different Python environments and it comes with a nice visual interface called [Anaconda Navigator](https://docs.anaconda.com/free/navigator/install/). 

It's a good practice to create a Python [environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#activating-an-environment) for each of your projects that require different Python packages, this will spare some problems in the future. So, let's create an environment called lalsuite where you will install all the packages required to run your simulations. Hence, once you have Anaconda installed, open a terminal and type: 

```bash
conda create --name lalsuite
```
When conda asks you to proceed, type y. You can list all discoverable environments with

```bash
conda info --envs
```
Next, you need to activate your environment to install the packages you need:

'''bash
conda activate lalsuite
'''
Once your environment is activated, you can install [LALsuite](https://anaconda.org/conda-forge/lalsuite)
'''bash
conda install -c conda-forge lalsuite
'''
and [Lalsimulation](https://anaconda.org/conda-forge/lalsimulation)

'''bash
conda install -c conda-forge lalsimulation
'''
Next, we install [Bilby](https://anaconda.org/conda-forge/bilby/):

'''bash
conda install -c conda-forge bilby
'''
and [HDF5](https://anaconda.org/anaconda/hdf5) to manage large files:
'''bash
conda install -c anaconda hdf5
'''
The delicate part is the following: we need a different version of Astropy than the one provided by default with the above installation. Then, to make things work, as per today, you need astropy version 5.3.1. To install this version you just need to type:

'''bash
conda install -c conda-forge astropy=5.3.1
'''
That's all regarding the Lalsuite installation. Now let's install some dependencies. To perform algebraic manipulations, including indexing, you need to install [numpy](https://anaconda.org/anaconda/numpy):
'''bash
conda install -c anaconda numpy 
'''
and it extension [Scipy](https://anaconda.org/anaconda/scipy)
'''bash
conda install -c anaconda scipy
'''
For plotting, you might like to install [Matplotlib](https://anaconda.org/conda-forge/matplotlib)
'''bash
conda install -c conda-forge matplotlib
'''
That is all. I've provided a list of the packages and dependences in my current lalsuite working environment for further reference.
