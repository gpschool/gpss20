---
layout: page
weight: 5
title: Labs
---

The labs for the Gaussian Process Summer School can be downloaded here. All of the lab sheets are written in Python 3 given in Jupyter notebook format.

Each lab sheet will be made available on the day of the lab, and answers for each will be made shortly after. There are also some extra work sheets, for you to explore in your own time, which give details of other uses of Gaussian processes not covered in the summer school.

Details of how to set up your Python environment and on the installation of the necessary libraries are available on the [Getting Started](../gpss20/getting_started) page. Ensure you have completed the setup before starting the labs. We recommend that you use Binder during the lab sessions.

To view and run the full list of labs, click here: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gpschool/labs/2020?filepath=2020%2F). Alternatively, you can use the corresponding links for each lab.

#### Mirror Sites
If you are unable to connect to Binder due to use capacity, try one of the available mirror servers or
follow instructions for [running labs on your local machine](../gpss20/getting_started#running-labs-on-your-local-machine).

[![Mirror 1](https://img.shields.io/badge/mirror%201-binder-blueviolet)](https://mybinder.org/v2/gh/wilocw/labs/2020?filepath=2020%2F)&nbsp;&nbsp;&nbsp; [![Mirror 2](https://img.shields.io/badge/mirror%202-binder-blueviolet)](https://mybinder.org/v2/gh/SheffieldMLNet/labs/2020?filepath=2020%2F)

### Lab 1: Gaussian Process Regression
This lab is designed to introduce Gaussian processes in a practical way, illustrating the concepts introduced in the first two lectures. The key aspects of Gaussian process regression are covered: the covariance function (aka kernels); sampling a Gaussian process; and the regression model. The notebook will introduce the open source Python library GPy which handles the kernels, regression and optimisation of hyperparameter, allowing us to easily access the results we want.

[![Download](https://img.shields.io/badge/download-lab%201-green)](https://github.com/gpschool/labs/raw/2020/2020/lab_1.ipynb) &nbsp;&nbsp;&nbsp; [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gpschool/labs/2020?filepath=2020%2Flab_1.ipynb) &nbsp;&nbsp;&nbsp;[![Mirror 1](https://img.shields.io/badge/mirror%201-binder-blueviolet)](https://mybinder.org/v2/gh/wilocw/labs/2020?filepath=2020%2Flab_1.ipynb)&nbsp;&nbsp;&nbsp; [![Mirror 2](https://img.shields.io/badge/mirror%202-binder-blueviolet)](https://mybinder.org/v2/gh/SheffieldMLNet/labs/2020?filepath=2020%2Flab_1.ipynb)&nbsp;&nbsp;&nbsp;
[![Answers](https://img.shields.io/badge/answers-nbviewer-green)](https://nbviewer.jupyter.org/github/gpschool/labs/blob/2020/2020/.answers/lab_1.ipynb)

Resources: [mauna_loa](https://github.com/gpschool/labs/raw/2020/.resources/mauna_loa)

#### Lab 1 Extra: Uncertainty Propagation
This lab is an extension on the work introduced in Lab 1 of the summer school. It is more advanced, and you should make sure you've completed Lab 1 before attempting. It is designed to demonstrate the advantage of using models when we have only a small number of observations of a latent function.

[![Download](https://img.shields.io/badge/download-lab%201%20extra-green)](https://github.com/gpschool/labs/raw/2020/2020/lab_1_extra.ipynb)&nbsp;&nbsp;&nbsp;[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gpschool/labs/2020?filepath=2020%2Flab_1_extra.ipynb)&nbsp;&nbsp;&nbsp;[![Mirror 1](https://img.shields.io/badge/mirror%201-binder-blueviolet)](https://mybinder.org/v2/gh/wilocw/labs/2020?filepath=2020%2Flab_1_extra.ipynb)&nbsp;&nbsp;&nbsp; [![Mirror 2](https://img.shields.io/badge/mirror%202-binder-blueviolet)](https://mybinder.org/v2/gh/SheffieldMLNet/labs/2020?filepath=2020%2Flab_1_extra.ipynb)&nbsp;&nbsp;&nbsp;
[![Answers](https://img.shields.io/badge/answers-nbviewer-green)](https://nbviewer.jupyter.org/github/gpschool/labs/blob/2020/2020/.answers/lab_1_extra.ipynb)


### Lab 2: GPs for Non-Gaussian Likelihoods and Big Data
This lab introduces Gaussian process regression for data with non-Gaussian likelihoods, and shows how this can be applied to classification. The concept of sparse methods for Gaussian process regression is introduced for creating a scalable regression model, and this is combined with a large classification problem.

As with Lab 1, the notebook uses GPy for handling the regression model and likelihoods.

You will need to also download the banana.csv dataset for one of the examples in the lab.

[![Download](https://img.shields.io/badge/download-lab%202-green)](httpsa://github.com/gpschool/labs/raw/2020/2020/lab_2.ipynb)&nbsp;&nbsp;&nbsp;[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gpschool/labs/2020?filepath=2020%2Flab_2.ipynb)&nbsp;&nbsp;&nbsp;[![Mirror 1](https://img.shields.io/badge/mirror%201-binder-blueviolet)](https://mybinder.org/v2/gh/wilocw/labs/2020?filepath=2020%2Flab_2.ipynb)&nbsp;&nbsp;&nbsp; [![Mirror 2](https://img.shields.io/badge/mirror%202-binder-blueviolet)](https://mybinder.org/v2/gh/SheffieldMLNet/labs/2020?filepath=2020%2Flab_2.ipynb)&nbsp;&nbsp;&nbsp;
<!--[![Answers](https://img.shields.io/badge/answers-nbviewer-green)](https://nbviewer.jupyter.org/github/gpschool/labs/blob/2020/2020/.answers/lab_2.ipynb)-->


Resources: [olympic_marathon_men](https://github.com/gpschool/labs/raw/2020/.resources/olympic_marathon_men) | [banana.csv](https://github.com/gpschool/labs/raw/2020/.resources/banana.csv) 

**Note: ensure you have installed libraries, particularly `climin`, as per the instructions in [Getting Started](./getting_started). Installing `climin` using `$ pip install climin` _will not work_ with the labs as this is Python 2 only. Remove it, and follow the instructions.**

<!--
#### Lab 2 Extra: Deep Gaussian Processes

This lab introduces regression with hierarchical "deep" Gaussian processes. You will need to have installed `pyDeepGP` for this lab.


[![Download](https://img.shields.io/badge/download-lab%202%20extra-green)](https://github.com/gpschool/labs/raw/2020/2020/lab_2_extra.ipynb)&nbsp;&nbsp;&nbsp;[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gpschool/labs/2020?filepath=2020%2Flab_2_extra.ipynb)&nbsp;&nbsp;&nbsp;[![Mirror 1](https://img.shields.io/badge/mirror%201-binder-blueviolet)](https://mybinder.org/v2/gh/wilocw/labs/2020?filepath=2020%2Flab_2_extra.ipynb)&nbsp;&nbsp;&nbsp; [![Mirror 2](https://img.shields.io/badge/mirror%202-binder-blueviolet)](https://mybinder.org/v2/gh/SheffieldMLNet/labs/2020?filepath=2020%2Flab_2_extra.ipynb)&nbsp;&nbsp;&nbsp;-->

<!--[![Answers](https://img.shields.io/badge/answers-nbviewer-green)](https://nbviewer.jupyter.org/github/gpschool/labs/blob/2020/2020/.answers/lab_2_extra.ipynb)-->


<!--
### Lab 3: Global Optimisation with Gaussian Processes
This lab introduces the basic concepts of Bayesian optimisation with GPyOpt. The student will have to build and compare different models and aquisition functions to solve several optimisation problems.
-->

<!--[![Download](https://img.shields.io/badge/download-lab%203-green)](https://github.com/gpschool/labs/raw/2020/2020/lab_3.ipynb)&nbsp;&nbsp;&nbsp;[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gpschool/labs/2020?filepath=2020%2Flab_3.ipynb)&nbsp;&nbsp;&nbsp;[![Mirror 1](https://img.shields.io/badge/mirror%201-binder-blueviolet)](https://mybinder.org/v2/gh/wilocw/labs/2020?filepath=2020%2Flab_3.ipynb)&nbsp;&nbsp;&nbsp; [![Mirror 2](https://img.shields.io/badge/mirror%202-binder-blueviolet)](https://mybinder.org/v2/gh/SheffieldMLNet/labs/2020?filepath=2020%2Flab_3.ipynb)&nbsp;&nbsp;&nbsp;-->

<!--[![Answers](https://img.shields.io/badge/answers-nbviewer-green)](https://nbviewer.jupyter.org/github/gpschool/labs/blob/2020/2020/.answers/lab_3.ipynb)-->

