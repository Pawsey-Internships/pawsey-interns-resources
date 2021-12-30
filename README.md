![alt text](https://www.olcf.ornl.gov/wp-content/uploads/2019/02/pawsey-logo-blue.png)

# Pawsey Intern Resource Collection :books:
Hello Interns! Welcome to the CSIRO Pawsey Supercomputing Center internship resources page. Here you can find a library of all information and training materials that pertain to the internship program.

## Table of Contents
* [Introduction](#introduction) :wave:
* [Unix](#unix) :shell:
	* [Introduction to Unix](#introduction-to-unix)
	* [More Unix Features](#more-unix-features)
* [Version Control](#version-control) :floppy_disk::books:
	* [Project Git Worflow on Topaz](#git-workflow) :open_file_folder::construction:
	* [Setting up GitHub CLI](#gh-cli) 
* [Supercomputing](#supercomputing) :collision::computer:
	* [Introduction to Supercomputing and Pawsey](#introduction-to-supercomputing-and-pawsey)
	* [Using VisualStudio on a Pawsey system](#using-visualstudio-on-a-pawsey-system)
	* [Using Jupyter Notebook on a Pawsey system](#using-jupyter-notebook-on-a-pawsey-system) :ringed_planet::ledger:
		* [Storing Variables in Jupyter Notebook](#storing-variables-in-jupyter-notebook)
	* [Filetransfer](#filetransfer)  :email::airplane:
* [Cloud Computing](#cloud-computing) :cloud::computer:
	* [Nimbus](#nimbus) 
* [Parallel Programming](#parallel-programming) :flags::computer:
	* [Introduction to Parallel Programming](#introduction-to-parallel-programming)
	* [Parallel Programming with Python and MPI](#parallel-programming-with-python-and-mpi)
	* [Parallel Programming with Python using the multiprocessing library](#parallel-programming-with-python-using-the-multiprocessing-library)
	* [Efficient parallelisation of Python Machine learning libraries](efficient-parallelisation-of-python-machine-learning-libraries)
* [Package Management](#package-management)  :package::desktop_computer:
	* [Using containers on a Pawsey system](#using-containers-on-a-pawsey-system)
		* [Install additional Python packages in a container](#additional-python-packages-container)
	* [Using Python Virtual Environment on a Pawsey system](#using-python-virtual-environment-on-a-pawsey-system)
* [Soft Skills](#soft-skills) :icecream::bow_and_arrow:
	* [AIM WA Everyday Leadership Webinar](#aim-wa-leadership)
	* [Unintended Consequences, Diversity and Inclusion Workshop](#unintended-consequences)
* [Communication, Visualisation and Presentation](#communication-presentation) :speaking_head::gift:
	* [Posters and Internship Videos](#posters-videos) :video_camera: :page_facing_up:
	* [Intro to Tableau for Data Visualisation](#intro-tableau) :bar_chart::chart_with_upwards_trend:
* [Domain-specific knowledge resources](#domain-specific-knowledge-resources) :mortar_board::books:
	* [Machine learning with Python libraries](#machine-learning-with-python-libraries) :robot::snake:
	* [Molecular Dynamics resources](#molecular-dynamics-resources) :dna:
* [Additional resources to get ahead](#additional-resources) :smiley:

<a name="introduction"></a> 
## Introduction :wave:
[Supercomputers](#supercomputing) play an important role and are used for a wide range of computationally intensive tasks in various fields, including quantum physics, molecular modelling, machine learning, climate research and many more. The most common supercomputers provided by Pawsey are [Topaz](https://support.pawsey.org.au/documentation/download/attachments/34017103/Topaz_Quick_Reference_Guide.pdf?version=2&modificationDate=1601967569275&api=v2) (GPU), [Magnus](https://support.pawsey.org.au/documentation/download/attachments/34017103/Magnus_Quick_Reference_Guide.pdf?version=1&modificationDate=1536029582214&api=v2) (CPU), and [Zeus](https://support.pawsey.org.au/documentation/download/attachments/2918240/Zeus_Quick_Reference_Guide.pdf?version=4&modificationDate=1533713268300&api=v2) (CPU). Supercomputers are generally accessed via the local command line using SSH, which requires [Unix](#unix) skills to navigate through the supercomputer and launch and monitor jobs on the cluster. A major advantage of using a cluster is the possibility to speed up computations by using [Parallel Programming](#parallel-programming). To keep track of the changes made over the course of a project using [Version Control](#version-control) is a useful tool. In addition, there are various approaches for [Filetransfer](#filetransfer) of data bewteen a supercomputer and your local machine. You can find a variety of libraries and programs as modules on Pawsey supercomputers. If your required resource is not available as a module, you can use a [container](#using-containers-on-a-pawsey-system) or when working with Python you can use a [Python Virtual Environment](#using-python-virtual-environment-on-a-pawsey-system). For projects with the need for a specifically set up instance, it is recommended to use another Pawsey resource called [Nimbus](#nimbus). Depending on your research topic, your use of the Pawsey resources will differ, therefore we also provide you with [Domain-specific knowledge resources](#domain-specific-knowledge-resources).

<a name="unix"></a>
## Unix :shell:

<a name="introduction-to-unix"></a>
### Introduction to Unix
We introduce the BASH command line interface in our [Introduction to unix tutorial](https://youtu.be/UnRBoqVmV9U), including basic commands. This tutorial enables you to navigate and alter your file system and files. In addition, we introduce the concept of pipes and finding things using grep and sed.\
The supporting material and in-depth reading can be found on [GitHub Pages](https://pawsey-internships.github.io/intro-unix-shell/).

<a name="more-unix-features"></a>
### More Unix Features
Further Unix Features introduced in the subsequent [tutorial](https://youtu.be/BjHSjtuRFnE) range from BASH scripts and functions to developing a user-defined 'del' command. Other topics addressed are regular expressions, if-statements, loops, and many more.
The material accompanying the tutorial is in our [GitHub Repository](https://github.com/Pawsey-Internships/more_with_bash).

<a name="version-control"></a>
## Version Control :floppy_disk::books:
Version control with Git is a powerful tool, as it enables collaboration and navigating to previous versions, which is crucial in software development. ([Tutorial Part 1](https://youtu.be/1Rpr0XLoRJM), [Tutorial Part 2](https://youtu.be/0ZF8OPUnxKw)).

The material for the tutorial is published on our [GitHub Pages](https://pawsey-internships.github.io/version-control/).

<a name="git-workflow"></a> 
### Project Git Workflow on Topaz :open_file_folder::construction:
We demonstrate how to use git commands to set up a project git workflow between your local system project directory and your project directory on a Pawsey HPC system. ([Tutorial](https://youtu.be/BC1eNIXY3tE))

<a name="gh-cli"></a> 
### Setting up GitHub CLI on a Pawsey HPC

Bring GitHub to your terminal on Topaz, Magnus, Zeus etc: 

~~~
$ cd $MYGROUP
$ VERSION=2.3.0
$ curl -sSL https://github.com/cli/cli/releases/download/v${VERSION}/gh_${VERSION}_linux_amd64.tar.gz -o gh_${VERSION}_linux_amd64.tar.gz
$ tar xvf gh_${VERSION}_linux_amd64.tar.gz
$ cd gh_${VERSION}_linux_amd64/bin
$ ./gh auth login
~~~

[Additional supporting documentaion](https://cli.github.com/)

<a name="supercomputing"></a>
## Supercomputing :collision::computer:

<a name="introduction-to-supercomputing-and-pawsey"></a>
### Introduction to Supercomputing and Pawsey
Pawsey has multiple clusters which can be used for computation, when local resources do not suffice, or when the need to use GPUs / parallelise code arises. An introduction on how to use Pawsey supercomputing resources, including an introduction to the Slurm Workload Manager is provided in this [workshop](https://youtu.be/qfSetBs09SE).

The resources for the workshop are to be found in the [Pawsey GitHub Repository](https://github.com/PawseySC/Introductory-Supercomputing).

A collection of resources for further reading about Pawsey supercomputing systems is to be found under the following links:\
[Introductory Supercomputing at Pawsey slides](https://support.pawsey.org.au/documentation/download/attachments/2162899/Introductory%20Supercomputing.pdf?api=v2)\
[Slurm Workload Manager and Command/option summary documentation](https://slurm.schedmd.com/documentation.html)\
[Topaz Quick Reference Sheet](https://support.pawsey.org.au/documentation/download/attachments/34017103/Topaz_Quick_R[…]_Guide.pdf?version=2&modificationDate=1601967569275&api=v2)

<a name="using-visualstudio-on-a-pawsey-system"></a>
### Using VisualStudio on a Pawsey system 
We explain how to use the VS Code IDE while running the developed code on the high performance computing cluster Topaz. ([Tutorial](https://youtu.be/TbYAedvDqAQ))

<a name="using-jupyter-notebook-on-a-pawsey-system"></a>
### Using Jupyter Notebook on a Pawsey system :ringed_planet::ledger:
A demonstration on how to use Jupyter Notebook on Topaz using containers is provided in form of a [tutorial](https://youtu.be/qrz-Se2zwJ8).\
Further information, and the SLURM script used in the tutorial can be found in the [Pawsey Jupyter Notebook documentation](https://support.pawsey.org.au/documentation/display/US/Running+GPU+enabled+JupyterHub+on+Topaz+and+Zeus+with+Singularity)\
You can choose the Jupyter Docker image most suited for your project from this [list](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html)

<a name="storing-variables-in-jupyter-notebook"></a>
#### Storing Variables in Jupyter Notebook :floppy_disk::ringed_planet:
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
### Filetransfer  :email::airplane:
When working on a remote machine like the Pawsey system, often files need to be transferred between the local machine and the remote machine. One way of transferring and synchronising files is by using GitHub repositories and accessing the same repository from the local and from the remote machine. However, the filesize for GitHub is limited, therefore other options are recommended when transferring larger files.
In the provided [tutorial](https://youtu.be/WgzqGHtGluQ), we demonstrate how to transfer files from a Pawsey cluster to a local machine using the desktop application Filezilla and using rsync from the command line. It has to be noted, that on a windows machine, rsync can only be used with WSL (not with a GitBash/PowerShell/cmd terminal).\
If Filezilla is not installed on your local machine, you can download the application from the [Filezilla website](https://filezilla-project.org/index.php)
Additional file transfer methods, and additional information to the introduced methods can be found in the [Pawsey Filetransfer documentation](https://support.pawsey.org.au/documentation/display/US/Transferring+Files)

<a name="cloud-computing"></a>
## Cloud Computing :cloud::computer:

<a name="nimbus"></a>
### Cloud Computing with Nimbus :cloud::broom:
We introduce Nimbus, our cloud computing system at Pawsey in our [Introduction to Nimbus Tutorial](https://www.youtube.com/watch?v=5yItRsdleE4&t=939s), including logging in, set up and fundamental operations. 

<a name="parallel-programming"></a>
## Parallel Programming :flags::computer:

<a name="introduction-to-parallel-programming"></a>
### Introduction to Parallel Programming

<a name="parallel-programming-with-python-and-mpi"></a>
### Parallel Programming with Python and MPI
To use a Message Passing Interface with Python, the mpi4py library is used. MPI is a way to program on distributed memory devices. Every parallel process is working in its own memory space, and overhead occurs when processes communicate with each other. A demonstration of using MPI in Python and on how to design parallelism to incur minimised communication overhead is demonstrated in our [tutorial](https://youtu.be/90ZgZf7qWE8) using the example of Conway's Game of Life. 
The material used in the tutorial can be found in our [GitHub Repository](https://github.com/Pawsey-Internships/mpi_and_python)

<a name="parallel-programming-with-python-using-the-multiprocessing-library"></a>
### Parallel Programming with Python using the multiprocessing library
The use of the [multiprocessing library](https://docs.python.org/3/library/multiprocessing.html) offers an efficient approach to parallelise python code by side-stepping the Global Interpreter Lock (GLI).

<a name="efficient-parallelisation-of-python-machine-learning-libraries"></a>
### Efficient parallelisation of Python Machine learning libraries


<a name="package-management"></a> 
## Package Management  :package::desktop_computer:

<a name="using-containers-on-a-pawsey-system"></a>
### Using containers on a Pawsey system
An efficient way to use software and libraries that are not available on Pawsey system, is to use a container. In this [tutorial](https://youtu.be/gxe2ER5mDm0), you find step-by-step instructions on how to built containers using [sylabs](https://sylabs.io/) and [singularity](https://support.pawsey.org.au/documentation/display/US/Singularity+modules+on+Pawsey+systems) on Topaz.

In-depth [documentation](https://support.pawsey.org.au/documentation/download/attachments/2162899/Overview%20of%20Containers%20in%20HPC.pdf?api=v2) providing an overview of Containers in HPC at Pawsey might be useful for further reading in addition to the tutorial.

<a name="additional-python-packages-container"></a>
#### Installing additional python packages in a container

See how to install additional python packages as needed in a container [Video Demo](https://youtu.be/EDnngLOgDvY).

<a name="using-python-virtual-environment-on-a-pawsey-system"></a>
### Using Python Virtual Environment on a Pawsey system  :snake::leaves:
As an alternative to using containers when wanting to install various python libraries that are not available under modules, a Python Virtual Environment can be used. The set up and usage of a Python Virtual Environment is explained in this [tutorial](https://youtu.be/e4fBZIfndHc).

Further information on Python Virtual enviornments can be found in the official [documentation](https://docs.python.org/3/tutorial/venv.html), and further information on symlinks can be found [here](https://dashdash.io/1/ln).

Notes to the tutorial:\
In case your PYTHONPATH environment variable is not automatically set to the python version in your virtual enviornment, please manually set your PYTHONPATH as follows:
~~~
$ export PYTHONPATH=$MYGROUP/tutorial-env/lib/python3.6/site-packages
~~~
If your virtual environment is called differently to *tutorial-env*, please replace accordingly.

In the tutorial section where prompted to load the *fix.group.permissions.sh* file, the file does not need to be located in your current directory, but is already on the HPC, therefore typing the command as prompted in the video suffices, without prior downloading the file. More information on the fix group permissions Pawsey tool is provided in the [Pawsey Documentation](https://support.pawsey.org.au/documentation/display/US/Pawsey+File+Systems+and+their+Usage).

When running your Pawsey Virtual Environment on the cluster using Slurm, please create a Slurm script following the below example (making adjustments in the resources requested as needed):
~~~
#!/bin/bash
#SBATCH --job-name=test-job
#SBATCH --nodes=1
#SBATCH --tasks-per-node=1
#SBATCH --cpus-per-task=1
#SBATCH --partition=gpuq
#SBATCH --account=internsXXXXX

# COMMENT: change the --account flag to your own personal account.

module load python

# COMMENT: add the path (absolute path) to your virtual environment here.
source $MYGROUP/tutorial-env1/bin/activate

# COMMENT: call your python code here --> or use another command if you are not using python.
python3 test.py

# COMMENT: deactivate the virtual environment after the job is finished, such that the slurm script finishes properly.
deactivate
~~~

<a name="soft-skills"></a>
## Soft Skills :icecream::bow_and_arrow:

<a name="aim-wa-leadership"></a>
### AIM WA Everyday Leadership Webinar

A workshop core to the internship on everyday leadership provided by AIM WA covering emotional intelligence, traits of succesful leaders in modern society, and the changing dynamics of leadership. ([Webinar](https://pawsey.org.au/alumni/)).

<a name="unintended-consequences"></a>
### Unintended Consequences, Diversity and Inclusion Workshop :warning::rainbow_flag:

We explore what it means to consider unintended consequences resulting from research and industry, the implications this has both in the workplace and in the community, how historical bias can be unintentionally reinforced with data and algorithms, and how we can play our part by championing the principles of diversity and inclusion through our work and in the workplace. ([Unintended Consequences Workshop](https://drive.google.com/file/d/1c1pSSEBmRLViPNQdl2xcR0Lg5kLrmNtG/view?usp=sharing)).

<a name="communication-presentation"></a>
## Communication and Presentation :speaking_head::gift:

<a name="posters-videos"></a>
### Posters and Internship Videos :video_camera: :page_facing_up:

Once onto the web page for the ([Alumni Posters and Intern Videos](https://pawsey.org.au/alumni/)), click on an image of an alumni of interest to inspect their poster and internship video for benchmarking.

<a name="intro-tableau"></a>
### Introduction to Tableau for Data Visualisation :bar_chart::chart_with_upwards_trend:
Explore how to use Tableau for effective visualisation of Project results. Tableau can facilitate creation of many visualisation including the staple and ever reliable line charts and bar plots ([Intro to Tableau](https://www.youtube.com/watch?v=E833ClKqluM))

<a name="domain-specific-knowledge-resources"></a>
## Domain-specific knowledge resources :mortar_board::books:

<a name="machine-learning-with-python-libraries"></a>
#### Machine learning with Python libraries :robot::snake:

In general, a great resource for Python-related tutorial is the [Python Engineer YouTube Channel](https://www.youtube.com/c/PythonEngineer/videos).
You can find examples of various Machine Learning (ML) model implementations using PyTorch and Tensorflow, Data processing hacks, and other Python-related topics.

| Library | Learning Resource | Description |
| ----------- | :----------- |:-----------|
| [scikit-learn](https://scikit-learn.org/stable/)  | [scikit-learn documentation](https://scikit-learn.org/stable/)| Intuitive and easy to use ML library with pre-implemented ML algorithms. Limited configuration ability of models. |
| [PyTorch](https://pytorch.org/docs/stable/)  |[DeepLearning with PyTorch YouTube Training](https://www.youtube.com/watch?v=c36lUUr864M) | |
| [Tensorflow](https://www.tensorflow.org/learn) | | |
| OpenCV | | |

<a name="molecular-dynamics-resources"></a>
#### Molecular Dynamics Resources :dna:
For GROMACS users/beginners [introductory tutorials](http://www.mdtutorials.com/gmx/) are available.
*Tutorial 1: Lysozyme in Water* should be enough to get you started with the basics and provide you with a good foundation.

<a name="additional-resources"></a>
## Additional resources to get ahead with your project :smiley:

Here we provide what we think are exemplary resources to save you upfront time and energy. Please feel free to provide us additional suggestions of resources you found particularly useful at jordan.makins@csiro.au, melissa.speer@csiro.au or edric.matwiejew@csiro.au.

| Resource | Link to Content | Description |
| ----------- | :----------- |:-----------|
| Google Datasets | [Publicly available data sets from Google](https://datasetsearch.research.google.com/) | Search for a data set for your project in Google's data set search engine. |
| Python Basics for Data Science (IBM) | [Video by edX](https://www.youtube.com/watch?v=JC3urnvKanI&t=3s)  | A 19 part course available on YouTube. edX is an American open source online course provider created by Harvard and MIT. |
| Machine Learning & Deep Learning Fundamentals | [Deep Lizzard](https://www.youtube.com/playlist?list=PLZbbT5o_s2xq7LwI2y8_QtvuXZedL6tQU)| This series explains concepts that are fundamental to deep learning and artificial neural networks for beginners. |
| Help choosing a Data Viz | [data-to-viz.com](https://www.data-to-viz.com/) | Select a data visualisation depending on whether your data is numerical, categorical or time series and also based on how many variables you are trying to visualize |
| [Data visualisation in R with examples](https://rkabacoff.github.io/datavis/IntroGGPLOT.html) | [ggplot](https://ggplot2.tidyverse.org/) | ggplot2 is a data visualisation package in the R programming language. Please refer to the tidyverse documentation and sample graphs in the links provided. |
| Data visualisation in Python with examples | [matplotlib](https://matplotlib.org/stable/tutorials/introductory/pyplot.html) | An introduction and tutorial for the pyplot interface. |
|  |  |  |
