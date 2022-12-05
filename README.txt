Modeling hydraulic heads with impulse response functions in different environmental settings


This folder contains the data to reproduce the results from the article Jemeljanova et al. "Modeling hydraulic heads with impulse response functions in different environmental settings".

# Guidelines to reproduce the results
This guide assumes the Anaconda software is installed (https://www.anaconda.com/products/individual). First, create a new conda environment, install all the required python packages from the environment.yml file, and activate the new conda environment.

Type `conda env create -f environment.yml`
`conda activate stable_pastas`


Second, run the python scripts to preprocess the input data and create the time series models. Depending on the computer resources, this may take a few hours to complete.

Move into the scripts folder
`jupyter execute 01_Modeling.ipynb` 


Next, evaluate the resulting model fits.
`jupyter execute 02_Model_fit_evaluation.ipynb`

 
Lastly, apply the correlation and linear regression analyses.
`jupyter execute 03_Correlation_and_linear_regression.ipynb`


The resulting data will be saved in the 'output' folder.


# Input data

The data used in this study was obtained from various organisations and online sources, and is open-source. It was extracted from the original data types, pre-processed according to the methodology of the study and rewritten to csv files.
The head series were pre-cleaned according to the methodology of Retike et al. (2022). No data alterations were performed on the meteo and environmental variables data beyond, e.g., extracting specific periods of the time series.

1. Groundwater data ('hydraulic_head.csv', [m]) was provided upon request by  the Republic of Estonia Environment Agency, the Latvian Environment, Geology, and Meteorology Center, and the Lithuanian Geological Survey.
2. Daily precipitation ('precipitation.csv', [mm/d]) and temperature data ('temperature_mean.csv', [degree Celcius]) were obtained from the European Climate Assessment & Dataset E-OBS gridded data ensemble (v.25.0e, resolution 0.1 degrees) (Cornes et al. 2018) from the closest cell center.
3. Potential evaporation data [mm/d] is computed from temperature data using the Hargreaves-Samani method '0' available from PyEt.
4. The environmental setting data ('environmental variables.csv') was calculated from various open-source datasets (see the Materials section in the article).




# Files

input/*
output/*
scripts/
  01_Modeling.html
  01_Modeling.ipynb
  02_Model_fit_evaluation.html
  02_Model_fit_evaluation.ipynb
  03_Correlation_and_linear_regression.html
  03_Correlation_and_linear_regression.html
  environment.yml


README.md


Cornes, R., G. van der Schrier, E.J.M. van den Besselaar, and P.D. Jones. 2018: An Ensemble Version of the E-OBS Temperature and Precipitation Datasets, J. Geophys. Res. Atmos., 123. doi:10.1029/2017JD028200