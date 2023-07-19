# How to install LALSuite in a Linux desktop machine

This is a short note about installing [LAL](https://git.ligo.org/lscsoft/lalsuite), and the necessary dependencies in a Linux machine from scratch. 

LAL speaks in Python, so we need to install a Python distribution and interpreter first. I like [Anaconda](https://docs.anaconda.com/free/anaconda/install/) because it makes it nice and easy to install Python packages and interpreters from a terminal, manage different Python environments and it comes with a nice visual interface called [Anaconda Navigator](https://docs.anaconda.com/free/navigator/install/). 

It's a good practice to create a Python [environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#activating-an-environment) for each of your projects that require different Python packages, this will spare some problems in the future. So, let's create an environment called lalsuite where you will install all the packages required to run your simulations. Hence, once you have Anaconda installed, open a terminal and type: 

```bash
conda create --name lalsuite
```

