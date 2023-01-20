sxrd-thermomechanical-test-analysis
-----------

A set of Python notebooks for analysing different types of thermomechanical test data, taken from accompanying in-situ synchrotron X-ray diffraction (SXRD) beam line experiments, for syncing a material's thermomechanical behaviour with the SXRD crystallographic observations.

The package includes notebooks for analysing resistivity/conductivity measurements made on an electro-thermal mechanical tester (ETMT), which can be used to calculate either the phase fraction or plastic strain changes, depending on the type of thermomechanical test.

A notebook is also included for extracting outputs for the NEXUS (.nxs) file format, which can be used for syncing thermomechanical test data with the synchrotron diffraction pattern image number from experiments at Diamond Light Source Ltd.

Development
--------------

This package was developed by Christopher S. Daniel at The University of Manchester, UK, and was funded by the Engineering and Physical Sciences Research Council (EPSRC) via the LightForm programme grant (EP/R001715/1). LightForm is a 5 year multidisciplinary project, led by The Manchester University with partners at University of Cambridge and Imperial College, London (https://lightform.org.uk/).

Contents
-----------

**It is recommended the user works through the examples in the notebooks in the following order:**
    
1. `ETMT_phase_fraction_calculator.ipynb` A notebook for analysing ETMT data to calculate phase fraction changes from resistivity and conductivity measurements, recorded as changes in voltage and current during heating experiments.

2. `ETMT_plastic_strain_calculator.ipynb` A notebook for analysing ETMT data to calculate plastic changes from resistivity and conductivity measurements, recorded as changes in voltage and current during high temperature deformation experiments.

3. `ETMT_plastic_strain_plotter.ipynb` A notebook for plotting the calculated plastic strain changes recorded from an ETMT during high temperature deformation experiments.

4. `NXS_analogue_output_calculator.ipynb` A notebook for extracting analogue outputs recorded from an ETMT and synced with the SXRD pattern image number, to sync thermomechanical test data with SXRD image number for experiments run at Diamond Light Source Ltd.

*Note, the `example-data/` folder contain data that can be used as an example analysis, but a clear external file structure should be setup to support the analysis of large synchrotron datasets.*

Installation and Virtual Environment Setup
-----------

Follow along by copying / pasting the commands below into your terminal (for a guide on using a python virtual environments follow steps 4-7).

**1. First, you'll need to download the repository to your PC. Open a unix command line on your PC and navigate to your Desktop (or GitHub repository):**
```unix
cd ~/Desktop
```
**2. In your teminal, use the following command to clone this repository to your Desktop:**
```unix
git clone https://github.com/LightForm-group/sxrd-thermomechanical-test-analysis.git
```
**3. Navigate inside `Desktop/sxrd-thermomechanical-test-analysis/` and list the contents using `ls`(macOS) or `dir`(windows):**
```unix
cd ~/Desktop/sxrd-thermomechanical-test-analysis/
```
**4. Next, create a python virtual environment (venv) which contains all of the python libraries required to use sxrd-thermomechanical-test-analysis.
Firstly, use the following command to create the venv directory which will contain the necessary libraries:**
```unix
python -m venv ~/Desktop/sxrd-thermomechanical-test-analysis/venv
```
**5. Your `sxrd-thermomechanical-test-analysis/` directory should now contain `venv/`. Install the relevant libraries to this venv by first activating the venv:**
```unix
source ~/Desktop/sxrd-thermomechanical-test-analysis/venv/bin/activate
```
*Note, the beginning of your command line should change from `(base)` to include `(venv)`.*

**6. Install the python libraries to this virtual environment using pip and the `requirements.txt` file included within the repository:**
```unix
pip install -r ~/Desktop/sxrd-thermomechanical-test-analysis/requirements.txt
```
**7. To ensure these installed correctly, use the command `pip list` and ensure the following packages are installed:**
```unix
pip list
# Check to ensure that all of the following are listed:
#numpy
#matplotlib
#pathlib
#tqdm
#jupyter
#pyyaml
#nexusformat
```
**8. If all in step 7 are present, you can now run the example notebooks.
Ensure the venv is active and use the following command to boot jupyter notebook (using all libraries installed in the venv)
Warning - using just `jupyter notebook` without `python -m` can result in using your default python environment (the libraries may not be recognised):**
```unix
python -m jupyter notebook
```
**9. Work through the notebooks and setup yaml text files for reproducible analysis of thermomechanical test data.**

**10. When you're finished using the virtual environment, deactivate it!
This will avoid confusion when using different python libraries that are not installed within the virtual environment:**
```unix
deactivate
```

Required Libraries
--------------------

The required libraries are listed in requirements.txt