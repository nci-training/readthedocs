Installing Jupyter and Python
==============================

We recommend installing `Anaconda`_ which conveniently installs:

	* Python
	* Jupyter Notebook
	* Other commonly used packages for scientific computing and data science


Installing Miniconda and Anaconda on macOS
-------------------------------------------

	#. Download the installers
		* `Miniconda installer for macOS`_
		* `Anaconda installer for macOS`_ - note you will need to register your email to download. Installation takes up approximately 2.2Gb of disk space.
	
	#. Install
		* **Miniconda** via terminal::    
   
		    $ cd ~/Downloads

		    $ bash Miniconda3-latest-MacOSX-x86_64.sh

		Then follow the installation instructions		
		
		* **Anaconda** -- Double click the ``.pkg`` file and follow the prompts on the installer screens. Accept the defaults if you are unsure about any settings – you can change them later.
	
	#. Close and re-open your terminal window.

	#. To test that the installation was successful, run the following command::
	
	    $ conda list


Installing Jupyter:
---------------------

Run the following command to install Jupyter::

   $ conda install jupyter


Clone GSKY Jupyter notebooks
-----------------------------

Open a working folder where we can clone the GSKY Jupyter notebooks and run::

   $ git clone https://github.com/nci/gsky-demos.git

   $ cd gsky demos


Here we have a list of GSKY demo tutorials. For this example, we will set up a virtual environment and run the ``Notebook_GSKY_WMS_ipyleaflet.ipynb`` tutorial.

Setting up virtual environment
-------------------------------

Let’s first set up a virtual environment to install all the required modules for this tutorial::

   $ conda create -n GSKY_WMS python=3.6 anaconda

Now let's activate our virtual environment::

   $ source activate GSKY_WMS

For this tutorial we need to install `ipyleaflet`_, `ipywidgets`_ and `owslib`::

   $ conda install -c conda-forge ipyleaflet

   $ conda install -c conda-forge ipywidgets

   $ conda install -c conda-forge owslib

Now we need to make sure our Jupyter notebook kernel uses our current environment. To do this, let's first install `nb_conda`_::

   $ conda install nb_conda
  
Now we can add our GSKY_WMS environment to the Jupyter kernel list::

   $ conda install -n GSKY_WMS nb_conda_kernels

Running notebooks
------------------

We should now be ready to run the ``Notebook_GSKY_WMS_ipyleaflet.ipynb`` tutorial::

   $ Jupyter notebook Notebook_GSKY_WMS_ipyleaflet.ipynb



.. _Anaconda: https://en.wikipedia.org/wiki/Anaconda_(Python_distribution)
.. _Miniconda installer for macOS: https://conda.io/miniconda.html
.. _Anaconda installer for macOS: https://www.anaconda.com/download/#macos
.. _ipyleaflet: https://github.com/jupyter-widgets/ipyleaflet
.. _ipywidgets: https://ipywidgets.readthedocs.io/en/stable/user_guide.html
.. _obslib: https://geopython.github.io/OWSLib/
.. _nb_conda: https://github.com/Anaconda-Platform/nb_conda


