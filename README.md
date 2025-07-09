# OSSE_pCO2

This repository contains introductory training material on climate and weather modelling,
focussing on Observation System Simulation Experience (OSSE), based on the article:

> Denvil-Sommer, A., Gehlen, M., and Vrac, M.: Observation system simulation experiments in the Atlantic Ocean for enhanced surface ocean pCO2 reconstructions, Ocean Sci., 17, 1011–1030, https://doi.org/10.5194/os-17-1011-2021, 2021.

## Base requirements

- Python 3

NOTE: this code uses [Pytorch](https://pytorch.org/), which on some laptops is not compatible with python versions >3.12 (for example if you are running a Mac with intel processors). If the installation of pytorch fails, you will need to use a different version of python (more details below).


The instructions below will install the necessary packages

## Getting started

1. Clone this repository into a directory
```
git clone https://github.com/lcimoli/OSSE_pCO2.git
```

2. Download the data set from:

> Denvil-Sommer, A. (2024). Dataset for OSSE exercise at ICCS Summer School 2024 Cambridge [Data set]. Zenodo. https://doi.org/10.5281/zenodo.12567970

It is easiest to download `Data_SS.zip` and unzip it into the same directory as the code so that the .csv
files are alongside the notebook file.

3. To setup the Notebook, we recommend running it in a virtual environment:

       python3 -m venv .venv
       source .venv/bin/activate
       pip install -r requirements.txt
       
<br/>
NOTE: If you get an error about pytorch, you will need to use a different python version when creating the virtual environment. First check what versions are available with 
	
	ls /usr/local/bin/python*

Then, pick a version previous to 3.13 (if available) and run
	
	/usr/local/bin/python3.XX -m venv .venv
	source ./venv/bin/activate
	pip install -r requirements.txt

Where XX should be changed with your python version (e.g. python3.11).
	
If a previous version of python is not available, you will need to install it. The easiest way is probably to use pyenv, i.e.

	brew install pyenv; pyenv install 3.12 . 
	
Alternatively, you can use conda to create an environment (this might take some time to setup):
1. first install miniforge https://conda-forge.org/download/
2. then create a new environment using 

	conda create -n my-env "python==3.12"

3. then pip install inside of this



<br/>
Once the requirements have been installed, you can load the notebook using your favourite mechanism. For example,
using Jupyter lab you can do:

      jupyter-lab

and then choose the `SOCAT_20082010_AtlOcean_ADS_05062024.ipynb` notebook.

If you are using VScode, you can select the version of python when you create a virtual environment.


## Credits

Originally created by Anna Denvil-Sommer. Reviewed by Laura Cimoli.