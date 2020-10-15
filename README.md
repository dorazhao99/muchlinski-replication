# COS 597E Assignment 2
Replicating Muchlinski et al (2016)

## Requirements
* R <= 3.5
* randomForest = 4.6.12
* caret = 6.076
* ROCR <= 1.05
* pROC <= 1.16
* stepPlr <= 0.93
* doMC <= 1.3
* xTable <= 1.8

## Extending Muchlinski et al.'s Findings
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
We separated out our data into temporal chunks based on decades.  
