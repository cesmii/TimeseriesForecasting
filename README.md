# TimeseriesForecasting

This code uses FB Prophet to forecast the demand in the future for items that used in different manufacturing locations. This is meant to be used on Azure ML with Azureml Python SDK. The environment requirements are enumerated in the requirements.txt file. You can use this file to create an environment within the Azure compute. For the purposes of testing, we used an Azure Virtual machine size Standard_DS12_v2 (4 cores, 28 GB RAM, 56 GB disk). All codes and data in this repo is covered under the MIT Open Source Licencing.

The main.ipynb notebook contains the code to run forecast on the data contained in the anonymized_historical_data_03_03_22.csv. The specific functions used to:
- clean and aggregate data, 
- run Prophet models as well as carry out hyperparameter searches to return the best model, 
- calculate metrics and store them 
are found in functions.ipynb notebook. 

The main.ipynb file uses a model_config_file that can be found in files/model_cvs. the config file contains necessary parameters to compare with the previous run to make sure new values are added, then run the forecast with the hyperparameter search.

The model forecast outputs are writtten into files/forecasts and the metrics and associated parameters can be found in files/model_evals.
