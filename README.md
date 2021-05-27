# Group12_WSCBS
_Universiteit van Amsterdam - Web Services and Cloud-Based Systems: assignment 5_

The code for the assignment consists of three Brane packages:
- etl
- create_prediction
- plot

All three packages are also shared in individual GitHub repositories, such that they can be imported very conveniently. 
This repository contains all the code we used, the datasets and documentation on how to run each of the packages.

## Installation
Import the packages as follows:
```shell
$ brane import sasjaderuijter/etl
```
```shell
$ brane import sasjaderuijter/create_prediction
```
```shell
$ brane import sasjaderuijter/plot
```

## Using the packages
Place the datasets needed in the shared filesystem of Brane. Example datasets are provided in [Group12_WSCBS/data](https://github.com/sasjaderuijter/Group12_WSCBS/tree/main/data).

Import the packages using BraneScript in a JupyterLab notebook.
```shell
import etl;
import create_prediction;
import plot;
```
The functions of all three packages can now be used in the notebook.
### etl
Create the titanic training data, using the dataset _titanic.csv_
```shell
create_titanic_trainset("/data/titanic");
```
Create the diabetes training data, using the dataset _diabetes.csv_
```shell
create_diabete_trainset("/data/diabetes");
```
Create the heart disease training data, using the dataset _heart_disease.csv_
```shell
create_heart_disease_trainset("/data/heart_disease");
```
### create_prediction
Run a regression model on a trainingset, using the example dataset _titanic_trainset.csv_
```shell
run_regression("/data/titanic_trainset");
```

Run a random forest model on a trainingset, using the example dataset _titanic_trainset.csv_
```shell
run_random_forest("/data/titanic_trainset");
```

### plot
Create a confusion matrix, using the example dataset _regression_results.csv_
```shell
create_plot("/data/regression_results");
```
Create a boxplot, using the example dataset _titanic_trainset.csv_
```shell
create_boxplot("/data/titanic_trainset");
```
