# Pawsey Intern Resource Collection
< !-- *Hello Interns! Welcome to the CSIRO Pawsey Supercomputing Center internship resources page. Here you can find a library of all information and training materials that pertain to the internship program. * --/>

## Table of Contents
* [Introduction](#introduction)
* [Unix](#unix)
	* [Introduction to Unix](#introduction-to-unix)
	* [More Unix Features](#more-unix-features)
* [Version Control](#version-control)
* [Supercomputing](#supercomputing)
	* [Introduction to Supercomputing and Pawsey](#introduction-to-supercomputing-and-pawsey)
	* [Using VisualStudio on a Pawsey system](#using-visualstudio-on-a-pawsey-system)
	* [Using Jupyter Notebook on a Pawsey system](#using-jupyter-notebook-on-a-pawsey-system)
		* [Storing Variables in Jupyter Notebook](#storing-variables-in-jupyter-notebook)
	* [Filetransfer](#filetransfer)
* [Parallel Programming](#parallel-programming)
	* [Introduction to Parallel Programming](#introduction-to-parallel-programming)
	* [Parallel Programming with Python and MPI](#parallel-programming-with-python-and-mpi)
	* [Parallel Programming with Python using the multiprocessing library](#parallel-programming-with-python-using-the-multiprocessing-library)
* [Package Management](#package-management)
	* [Using containers on a Pawsey system](#using-containers-on-a-pawsey-system)
	* [Using Python Virtual Environment on a Pawsey system](#using-python-virtual-environment-on-a-pawsey-system)
* [Domain-specific knowledge resources](#domain-specific-knowledge-resources)
	* [Machine learning with Python libraries](#machine-learning-with-python-libraries)
	* [Molecular Dynamics resources](#molecular-dynamics-resources)

<a name="introduction"></a>
### Introduction
< !-- *The introduction we discussed referring to the other sections as hyperlinks, that user can click when interested while reading intro.* --/>
[Supercomputers](#supercomputing) play an important role and are used for a wide range of computationally intensive tasks in various fields, including quantum physics, molecular modelling, machine learning, climate research and many more. Supercomputers are generally accessed via the local command line using SSH, which requires [Unix](#unix) skills to navigate through the supercomputer and launch and monitor jobs on the cluster.

<a name="unix"></a>
### Unix

<a name="introduction-to-unix"></a>
#### Introduction to Unix
We introduce the BASH command line interface in our [Introduction to unix tutorial](https://youtu.be/UnRBoqVmV9U), including basic commands. This tutorial enables you to navigate and alter your file system and files. In addition, we introduce the concept of pipes and finding things using grep and sed.\
The supporting material and in-depth reading can be found on [GitHub Pages](https://pawsey-internships.github.io/intro-unix-shell/).

<a name="more-unix-features"></a>
#### More Unix Features
Further Unix Features introduced in the subsequent [tutorial](https://youtu.be/BjHSjtuRFnE) range from BASH scripts and functions to developing a user-defined 'del' command. Other topics addressed are regular expressions, if-statements, loops, and many more.
The material accompanying the tutorial is in our [GitHub Repository](https://github.com/Pawsey-Internships/more_with_bash).

<a name="version-control"></a>
### Version Control
Version control with Git is a powerful tool, as it enables collaboration and navigating to previous versions, which is crucial in software development. ([Tutorial Part 1](https://youtu.be/1Rpr0XLoRJM), [Tutorial Part 2](https://youtu.be/0ZF8OPUnxKw)).

The material for the tutorial is published on our [GitHub Pages](https://pawsey-internships.github.io/version-control/).

<a name="supercomputing"></a>
### Supercomputing

<a name="introduction-to-supercomputing-and-pawsey"></a>
#### Introduction to Supercomputing and Pawsey
Pawsey has multiple clusters which can be used for computation, when local resources do not suffice, or when the need to use GPUs / parallelise code arises. An introduction on how to use Pawsey supercomputing resources, including an introduction to the Slurm Workload Manager is provided in this [workshop](https://youtu.be/qfSetBs09SE).

The resources for the workshop are to be found in the [Pawsey GitHub Repository](https://github.com/PawseySC/Introductory-Supercomputing).

A collection of resources for further reading about Pawsey supercomputing systems is to be found under the following links:\
[Introductory Supercomputing at Pawsey slides](https://support.pawsey.org.au/documentation/download/attachments/2162899/Introductory%20Supercomputing.pdf?api=v2)\
[Slurm Workload Manager and Command/option summary documentation](https://slurm.schedmd.com/documentation.html)\
[Topaz Quick Reference Sheet](https://support.pawsey.org.au/documentation/download/attachments/34017103/Topaz_Quick_R[…]_Guide.pdf?version=2&modificationDate=1601967569275&api=v2)

<a name="using-visualstudio-on-a-pawsey-system"></a>
#### Using VisualStudio on a Pawsey system
We explain how to use the VS Code IDE while running the developed code on the high performance computing cluster Topaz. ([Tutorial](https://youtu.be/TbYAedvDqAQ))

<a name="using-jupyter-notebook-on-a-pawsey-system"></a>
#### Using Jupyter Notebook on a Pawsey system
A demonstration on how to use Jupyter Notebook on Topaz using containers is provided in form of a [tutorial](https://youtu.be/qrz-Se2zwJ8).\
Further information, and the SLURM script used in the tutorial can be found in the [Pawsey Jupyter Notebook documentation](https://support.pawsey.org.au/documentation/display/US/Running+GPU+enabled+JupyterHub+on+Topaz+and+Zeus+with+Singularity)\
You can choose the Jupyter Docker image most suited for your project from this [list](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html)

<a name="storing-variables-in-jupyter-notebook"></a>
##### Storing Variables in Jupyter Notebook
When you run computationally intensive code in your Jupyter Notebook, it unnecessarily uses up resources, when you re-run it every time, in order to run subsequent code. Therefore, it is recommended to save intermediary results. One option would be to save your intermediate output to file, and re-load it when continuing your work. Another option which does not require storing to file, is introduced in this tutorial. The ipython feature used is called [StoreMagic](https://ipython.readthedocs.io/en/stable/config/extensions/storemagic.html).\
Using Store Magic with Jupyter Notebook is demonstrated in our [tutorial](https://youtu.be/uT-EBq-kdvY).\
Note for the tutorial: When using the WSL terminal on a windows machine, your .ipython directory is most likely not located in your Linux home directory, but in your windows home directory. This results in the following change of paths:\
Instead of using:
~~~
$ vim ~/.ipython/profile_default/ipython_config.py
~~~

use the following command:

~~~
$ vim /mnt/c/Users/USERNAME/.ipython/profile_default/ipython_config.py
~~~
Where USERNAME is the username of your windows user profile. Note: If your username has a blank space in it, i.e. Darth Vader, your path has to be in quotation marks, i.e.:

~~~
$ vim "/mnt/c/Users/Darth Vader/.ipython/profile_default/ipython_config.py"
~~~

alternatively, you can use the CMD command line, which when promoted will automatically be in your windows home directory. Then use the following command:
~~~
$ notepad .ipython/profile_default/ipython_config.py
~~~


<a name="filetransfer"></a>
#### Filetransfer
When working on a remote machine like the Pawsey system, often files need to be transferred between the local machine and the remote machine. One way of transferring and synchronising files is by using GitHub repositories and accessing the same repository from the local and from the remote machine. However, the filesize for GitHub is limited, therefore other options are recommended when transferring larger files.
In the provided [tutorial](https://youtu.be/WgzqGHtGluQ), we demonstrate how to transfer files from a Pawsey cluster to a local machine using the desktop application Filezilla and using rsync from the command line. It has to be noted, that on a windows machine, rsync can only be used with WSL (not with a GitBash/PowerShell/cmd terminal).\
If Filezilla is not installed on your local machine, you can download the application from the [Filezilla website](https://filezilla-project.org/index.php)
Additional file transfer methods, and additional information to the introduced methods can be found in the [Pawsey Filetransfer documentation](https://support.pawsey.org.au/documentation/display/US/Transferring+Files)

<a name="using-containers-on-a-pawsey-system"></a>
#### Using containers on a Pawsey system
An efficient way to use software and libraries that are not available on Pawsey system, is to use a container. In this [tutorial](https://youtu.be/gxe2ER5mDm0), you find step-by-step instructions on how to built containers using [sylabs](https://sylabs.io/) and [singularity](https://support.pawsey.org.au/documentation/display/US/Singularity+modules+on+Pawsey+systems) on Topaz.

In-depth [documentation](https://support.pawsey.org.au/documentation/download/attachments/2162899/Overview%20of%20Containers%20in%20HPC.pdf?api=v2) providing an overview of Containers in HPC at Pawsey might be useful for further reading in addition to the tutorial.

<a name="using-python-virtual-environment-on-a-pawsey-system"></a>
#### Using Python Virtual Environment on a Pawsey system
As an alternative to using containers when wanting to install various python libraries that are not available under modules, a Python Virtual Environment can be used. The set up and usage of a Python Virtual Environment is explained in this [tutorial](https://youtu.be/e4fBZIfndHc).

Further information on Python Virtual enviornments can be found in the official [documentation](https://docs.python.org/3/tutorial/venv.html), and further information on symlinks can be found [here](https://dashdash.io/1/ln).

Notes to the tutorial:\
In case your PYTHONPATH environment variable is not automatically set to the python version in your virtual enviornment, please manually set your PYTHONPATH as follows:
~~~
$ export PYTHONPATH=$MYGROUP/tutorial-env/lib/python3.6/site-packages
~~~
If your virtual environment is called differently to *tutorial-env*, please replace accordingly.

In the tutorial section where prompted to load the *fix.group.permissions.sh* file, the file does not need to be located in your current directory, but is already on the HPC, therefore typing the command as prompted in the video suffices, without prior downloading the file. More information on the fix group permissions Pawsey tool is provided in the [Pawsey Documentation](https://support.pawsey.org.au/documentation/display/US/Pawsey+File+Systems+and+their+Usage).

<a name="parallel-programming"></a>
### Parallel Programming

<a name="introduction-to-parallel-programming"></a>
#### Introduction to Parallel Programming

<a name="parallel-programming-with-python-and-mpi"></a>
#### Parallel Programming with Python and MPI
To use a Message Passing Interface with Python, the mpi4py library is used. MPI is a way to program on distributed memory devices. Every parallel process is working in its own memory space, and overhead occurs when processes communicate with each other. A demonstration of using MPI in Python and on how to design parallelism to incur minimised communication overhead is demonstrated in our [tutorial](https://youtu.be/90ZgZf7qWE8) using the example of Conway's Game of Life. 
The material used in the tutorial can be found in our [GitHub Repository](https://github.com/Pawsey-Internships/mpi_and_python)

<a name="parallel-programming-with-python-using-the-multiprocessing-library"></a>
#### Parallel Programming with Python using the multiprocessing library
The use of the [multiprocessing library](https://docs.python.org/3/library/multiprocessing.html) offers an efficient approach to parallelise python code by side-stepping the Global Interpreter Lock (GLI).

<a name="package-management"></a>
### Package Management

<a name="domain-specific-knowledge-resources"></a>
### Domain-specific knowledge resources

<a name="machine-learning-with-python-libraries"></a>
#### Machine learning with Python libraries

In general, a great resource for Python-related tutorial is the [Python Engineer YouTube Channel](https://www.youtube.com/c/PythonEngineer/videos).
You can find examples of various Machine Learning (ML) model implementations using PyTorch and Tensorflow, Data processing hacks, and other Python-related topics.

| Library     | Learning Resources | Description |
| ----------- | :----------- |:-----------|
| [scikit-learn](https://scikit-learn.org/stable/)  |  | Intuitive and easy to use ML library with pre-implemented ML algorithms. Limited configuration ability of models. |
| [PyTorch](https://pytorch.org/docs/stable/)  |[DeepLearning with PyTorch YouTube Training](https://www.youtube.com/watch?v=c36lUUr864M) | |
| [Tensorflow](https://www.tensorflow.org/learn) | | |
| OpenCV | | |
| ... | | |

<a name="molecular-dynamics-resources"></a>
#### Molecular Dynamics Resources


