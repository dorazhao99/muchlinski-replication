# COS 597E Assignment 2
## 1. Replicating Muchlinski et al (2016)

### Code:
- `replication_code.R` contains the fixed code that can be run with the following requirements.

### Requirements
* R <= 3.5
* randomForest = 4.6.12
* caret = 6.076
* ROCR <= 1.05
* pROC <= 1.16
* stepPlr <= 0.93
* doMC <= 1.3
* xTable <= 1.8

## 2. Extending Muchlinski et al.'s Findings

### Code:
- Data Preprocessing Notebook: generates the datasets used for geographic and temporal experiments.
- Logistic Regression and Random Forests Notebook: model selection.
- Geo Models Notebook: geographic experiments.
- Temp Models Notebook: temporal experiments.

### Geographic Experiments 
We used [CIA World Factbook](https://www.cia.gov/library/publications/resources/the-world-factbook/fields/278.html) to assign geographic regions to each of the countries. The association between country and geographic region can be found in cow.csv. 

Abbreviation| Region
------------ | -------------
AFR | Africa
ASI | Asia
CAM | Central America and the Caribbean
EUR | Europe
ME | Middle East
NAM | North America
OCE | Oceania
SAM | South America
SEA | Southeast Asia

To create our training and testing sets, we combined North America, South America, and Central America into the "Americas" and Asia, Southeast Asia, and Oceania into "Asia / Oceania". 

### Temporal Experiments 
We separated out our data into temporal chunks approximately based on decades. Specifically:
- Decade 1: 1945-1959.
- Decade 2: 1960-1969.
- Decade 3: 1970-1979.
- Decade 4: 1980-1989.
- Decade 5: 1990-2000.
