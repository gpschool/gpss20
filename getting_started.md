---
layout: page
title: Getting Started
weight: 3
---


## Introduction 

The Gaussian Process Summer School will include some hands-on tutorials in which we will build some simple Gaussian process models. The tutorials will be in Python, featuring the open source _GPy package_ that has been developed by the Machine Learning group at the University of Sheffield.

Labs will take place via Zoom. Participants will be divided into breakout rooms. Each room will have a dedicated lab helper.

Prior Python programming skills are not required, however you should ensure that you have installed the appropriate version of Python and the packages/libraries we will be using:

- **Python 3.6**
- `numpy`
- `scipy`
- `matplotlib`
- `GPy`
- `jupyter`

Additional requirements include
- `climin`
- `GPyOpt`
- `pyDeepGP`

All labs are in a format called "_notebooks_", which can be run using [Jupyter](http://jupyter.org/index.html). These are worksheets that can execute Python code in blocks in your web browser.

## Running Labs in Binder

This year, we are hosting the labs on Binder, a cloud-based environment that you can use to run labs in. You can run the labs in Binder from your browser, without the need to setup a python environment locally on your machine.

To access the labs on Binder, follow the appropriate links on the [Labs](./labs) page. We recommend using Binder during the lab sessions. Note that due to high numbers of participants and limits on concurrent users in Binder, you may have to use one of the mirror lab, if you are unable to load a lab.

**Remember to download your notebooks if you would like to save them, as changes made will not be saved across different sessions.**

## Running Labs on your Local Machine

You may wish to run the labs on your local machine. You can do this by setting up a Python environment using the following instructions. We highly recommend that you install an integrated Python environment, in particular [Anaconda](https://store.continuum.io/cshop/anaconda) which will allow for easy installation of packages. It also comes with the latest versions of `numpy` and `scipy`.

The following instructions will tell you how to install and setup the Python library for the tutorials, and some information on installing and running Jupyter.

To use the notebooks locally, you should download the respective lab sheet. In a terminal window, navigate to the file's path (using the `cd` command) and run the command `jupyter notebook`. This will open a browser window connecting to the (locally hosted) notebook server. The notebook should be visible in the file list.

Typically, Jupyter will launch the server at [http://localhost:8888/tree](http://localhost:8888/tree), and you can navigate to it this way, should you accidentally close the window.

## Installing Python with Anaconda

Anaconda is a distribution of the Python prorgamming language that comes integrated with a number of precompiled libraries, and its own package and environment manager, called `conda`. It freely allows use of installation of packages and libraries via `conda` or `pip`. We recommend using Anaconda to manage your Python language environment, _particularly if you are new to Python_, and the following instructions will assume you are using Anaconda. If you are using a different Python distribution, you may have to tailor to following instructions, but you should ensure that you are using Python 3.5+.

### Installing
The easiest way to get a working Python environment is to install Anaconda. It is fairly straightforward to install, but can take some time so you must make sure this is done before the lab.

1. Download and install the free version of Anaconda from its webpage: [https://www.anaconda.com/download](https://www.anaconda.com/download), selecting the *Python 3.7 version* appropriate for your operating system
  - Windows: the installer will be a `.exe` executable, and you can follow the setup as instructed
  - macOS: the installer is a `.pkg` software package, and you can follow the setup as instructed
  - Linux: the installer is a `.sh` shell script, and you can run it in the terminal and follow the setup as instructed
    - Note you may have to enable execution of the file, by either
      - Right click the file and select Properties, and under `Permissions` check "Allow executing file as program"
      - `$ chmod +x /path/to/installationfile.sh`
1. Update Anaconda, `numpy`, `scipy`, and `matplotlib`: open a command prompt or terminal and execute the following commands
  1. `conda update -y anaconda`
  1. `conda update -y numpy scipy matplotlib`
1. Update `jupyter`
  1. `conda update -y jupyter`
  - If you are not using Anaconda, you can install `jupyter` by calling `$ python3 -m pip install juypter`

## Setting up your Conda Environment with `environment.yml` [**recommended**]
To setup an environment to use with the labs, we have provided a setup file that will allow Conda to automatically install the default libraries.

First, download [environment.yml](https://github.com/gpschool/labs/raw/2019/environment.yml).

Now, execute the following command in your command terminal, e.g. `Anaconda Prompt` or `terminal`:
```
$ conda env create -f environment.yml
```
This will generate a Conda environment called `python_3_gpss` with all the packages required to run the labs. You can check this by running 
```
$ conda activate python_3_gpss
(python_3_gpss) $ python

>>> import GPy
>>> GPy.tests()
``` 

You can now download the labs and run them in Jupyter notebook. To do this, you can either activate the environment and run `jupyter notebook`:
```
$ conda activate python_3_gpss
(python_3_gpss) $ jupyter notebook
```
... or you can follow the instructions in [Using the New Environment in Jupyter](#using-the-new-environment-in-jupyter).

## Manually Creating an Environment with Conda
**If you have used `environment.yml` to setup your environment, you don't need to do this.**

Full details of the functionality of `conda`'s virtual environment are available on its [documentation page](https://conda.io/docs/user-guide/tasks/manage-environments.html). The following instructions should get you a working environment with all the necessary features using a terminal. It is also possible to use Anaconda Navigator, if you have it installed, to perform these steps using a graphical user interface.

In the following steps, we will name our environment "`python_3_gpss`", but you can name it whatever is most appropriate (just make sure you replace any mention of `python_3_gpss` with your preferred name). Likewise, we will use Python 3.6, though 3.5 may also be used, in which case replace `3.6` with `3.5` as appropriate. Setting the version is particularly important if you use Python 2 with Anaconda by default.

In a command prompt / terminal, execute the following line:
```
$ conda create -y --name python_3_gpss python=3.6 anaconda
```

This may take a while to install, as it is replicating the default Anaconda packages in the new environment (alternatively, you can customise the packages installed, as found in the provided environment.yml file).

Next, you must "activate" the new environment. While an environment is activated (in a given terminal window), we will be able to access the `python` executable and install any packages by simply calling `python` and `pip`:

**Windows (using `Anaconda Prompt`) / Linux / macOS**:
```
$ conda activate python_3_gpss
```

You will now see that the terminal prompt is prefixed by `(python_3_gpss)`. While this is here, we are in the activated environment, and you can now install `GPy` as described above. Make sure to run the tests, as described, to confirm the installation.

Note that to deactivate the environment and return to the default Python environment, simply execute the command `deactivate` / `source deactivate` for Windows / Linux respectively.

### Using the New Environment in Jupyter
By default, we cannot use the environment in Jupyter (and so cannot use it to run the labs). However, it is relatively simple to add the new environment as a "kernel" for Jupyter to use.

Simply activate the environment, and run the following command:

```
$ python -m ipykernel install --user --name python_3_gpss --display-name "Python 3 (GPSS)"
$ deactivate
```
_Remember that, for Linux or macOS, you must prepend `deactivate` with `source`_.

We have deactivated, as we can now access the environment as a Jupyter kernel regardless of whether the environment is activated in the terminal -- this is particularly convenient.

If you run `jupyter notebook` now and open a notebook, you should be able to see the new kernel in the dropdown list when selecting a kernel. You should select your environment, the name of which will be shown in the top right of the notebook. **If you select the wrong kernel, or Jupyter chooses the wrong one, you can change it by selecting the correct one from the `Change kernel >` menu in the `Kernel` taskbar at the top**.

### Deleting an Environment
If you need to delete a created environment, for example if you make a mistake and want to start afresh, you can simply use the `remove` command in `conda`:
```
$ conda remove --name python_3_gpss --all
```

## Installing with Libraries with `pip`
If you have manually created your Conda environment, or would simply like to install these libraries in your base `python` environment, follow these instructions.
  
### GPy
We will install `GPy` using `pip`, by performing the following command in the terminal/command prompt:

```
$ pip install GPy
```

Installing `GPy` will also install its other dependencies, such as `paramz`, so you don't need to worry about these. You can test that the installation of `GPy` is working by running the following in a Python shell:
```
>>> import GPy
```
If you want to check your installation, you need to `$ pip install nose` and run `>>> GPy.tests()` in the Python shell. This will run through the testing sequence.

Note that GPy currently has **not** been updated to work with Python 3.7 so you should avoid using this version. For details on how to create a working environment, see [Advanced: Creating a Python Environment for the Labs](#Advanced%3A-Creating-a-Python-Environment-for-the-Labs) for details.

### GPyOpt

```
$ pip install gpyopt
```
Some of the options of GPyOpt depend on other external packages: `DIRECT`, `cma`, and `pyDOE`. Please be sure that these are installed if you want to use all the options. With everything installed, you are ready to start.

### pyDeepGP

This is the library used for created deep Gaussian Processes with GPy.

```
$ pip install git+https://github.com/SheffieldML/pyDeepGP
```

### climin
This is the library used for stochastic optimisation, and is required for the final section of Lab 2.

```
$ pip install git+https://github.com/BRML/climin
``` 

**Do not install `climin` from PyPI -- ensure you use the GitHub version as instructed**
