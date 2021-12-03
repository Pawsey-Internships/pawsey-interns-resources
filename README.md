# Pawsey Intern Resource Collection
< !-- *Quick intro to repo.* --/>

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
	* [Using containers on a Pawsey system](#using-containers-on-a-pawsey-system)
* [Parallel Programming](#parallel-programming)
	* [Introduction to Parallel Programming](#introduction-to-parallel-programming)
	* [Parallel Programming with Python and MPI](#parallel-programming-with-python-and-mpi)
	* [Parallel Programming with Python using the multiprocessing library](#parallel-programming-with-python-using-the-multiprocessing-library)
* [Package Management](#package-management)
* [Domain-specific knowledge resources](#domain-specific-knowledge-resources)
	* [Machine learning with Python libraries](#machine-learning-with-python-libraries)
	* [Molecular Dynamics resources](#molecular-dynamics-resources)

<a name="introduction"></a>
### Introduction
< !-- *The introduction we discussed referring to the other sections as hyperlinks, that user can click when interested while reading intro.* --/>

<a name="unix"></a>
### Unix

<a name="introduction-to-unix"></a>
#### Introduction to Unix
We introduce the BASH command line interface in our introduction to unix tutorial, including basic commands. This tutorial enables you to navigate and alter your file system and files. In addition, we introduce the concept of pipes and finding things using grep and sed.\
The supporting material and in-depth reading can be found in our [GitHub Documentation].

<a name="more-unix-features"></a>
#### More Unix Features

<a name="version-control"></a>
### Version Control

<a name="supercomputing"></a>
### Supercomputing

<a name="introduction-to-supercomputing-and-pawsey"></a>
#### Introduction to Supercomputing and Pawsey

<a name="using-visualstudio-on-a-pawsey-system"></a>
#### Using VisualStudio on a Pawsey system

<a name="using-jupyter-notebook-on-a-pawsey-system"></a>
#### Using Jupyter Notebook on a Pawsey system
A demonstration on how to use Jupyter Notebook on Topaz using containers.\
Further information, and the SLURM script used in the tutorial can be found in the [Pawsey Jupyter Notebook documentation](https://support.pawsey.org.au/documentation/display/US/Running+GPU+enabled+JupyterHub+on+Topaz+and+Zeus+with+Singularity)\
You can choose the Jupyter Docker image most suited for your project from this [list](https://support.pawsey.org.au/documentation/display/US/Running+GPU+enabled+JupyterHub+on+Topaz+and+Zeus+with+Singularity)

<a name="storing-variables-in-jupyter-notebook"></a>
##### Storing Variables in Jupyter Notebook
When you run computationally intensive code in your Jupyter Notebook, it unnecessarily uses up resources, when you re-run it every time, in order to run subsequent code. Therefore, it is recommended to save intermediary results. One option would be to save your intermediate output to file, and re-load it when continuing your work. Another option which does not require storing to file,is introduced in this tutorial. The ipython feature used is called [StoreMagic](https://ipython.readthedocs.io/en/stable/config/extensions/storemagic.html).\
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
A demonstration on how to transfer files from a Pawsey cluster to a local machine using Filezilla and rsync.\
If Filezilla is not installed on your local machine, you can download the application from the [Filezilla website](https://filezilla-project.org/index.php)
Additional file transfer methods, and additional information to the introduced methods can be found in the [Pawsey Filetransfer documentation](https://support.pawsey.org.au/documentation/display/US/Transferring+Files)

<a name="using-containers-on-a-pawsey-system"></a>
#### Using containers on a Pawsey system

<a name="parallel-programming"></a>
### Parallel Programming

<a name="introduction-to-parallel-programming"></a>
#### Introduction to Parallel Programming

<a name="parallel-programming-with-python-and-mpi"></a>
#### Parallel Programming with Python and MPI
To use a Message Passing Interface with Python, the mpi4py library is used. MPI is a way to program on distributed memory devices. Every parallel process is working in its own memory space, and overhead occurs when processes communicate with each other. A demonstration of using MPI in Python and on how to design parallelism to incur minimised communication overhead is demonstrated in our [tutorial](https://www.youtube.com/watch?v=90ZgZf7qWE8) using the example of Conway's Game of Life. 
The material used in the tutorial can be found in our [GitHub Repository](https://github.com/Pawsey-Internships/mpi_and_python)

<a name="parallel-programming-with-python-using-the-multiprocessing-library"></a>
#### Parallel Programming with Python using the multiprocessing library

<a name="package-management"></a>
### Package Management

< !-- *maybe as subsection instead? But where?* --/>

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

< !-- *for installation name a pawsey container if available + pip command if working locally* --/>

<a name="molecular-dynamics-resources"></a>
#### Molecular Dynamics Resources


