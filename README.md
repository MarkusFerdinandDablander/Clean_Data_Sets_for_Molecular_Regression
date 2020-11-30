# Clean_Data_Sets_for_Molecular_Regression
A collection of 6 clean benchmark data sets for regression tasks on molecules (represented as SMILES). These data sets have been retrieved from MoleculeNet.ai; they are are canonically used in publications in the area of molecular machine learning to validate and compare computational classification techniques.

Each folder corresponds to one data set and contains the following items:

- A readme file or a scientific paper which describes the nature of the data set and its context and source.
- A .csv file in which one can find a SMILES representation for each molecule and the regression values
- Depending on the context, some additional information and data.

The file "overview.csv" gives some basic information about the chosen data sets.

A Jupyter lab notebook called "data_pipeline" with Python code is contained which provides computational pipelines to automatically load the data sets and bring them into a useful form for machine learning. This notebook encompasses methods for each data set 

- to import the data set into a pandas dataframe,
- to check for and remove invalid SMILES (there is none in most data sets),
- to check for missing values (there is none in most data sets)
- to get some basic statistics on the data set,
- to construct a continuous target variable y in the form of a 1d numpy array which contains real values,
- to z-transform the target variable y for it to have mean 0 and standard deviation 1, and
- to construct a predictor variable x in the form of a 1d numpy array which contains SMILES strings.

The data processing functions in the notebook rely on basic functions within the Python packages numpy, pandas, matplotlib, math, sys, io and RDkit. To get a nice structuring of the notebook, it is recommended to use a Jupyer lab extension for collapsible headings.
