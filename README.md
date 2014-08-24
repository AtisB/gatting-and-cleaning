getting-and-cleaning

This repo contains code for Getting and Cleaning Data

Script
The script contains a function run.analysis() that performs the actual job:
•	reads train and test data sets and merges them
•	processes the merged data set (extract the relevant variables, adds descriptive activity names, etc.)
•	creates the merged data set 
•	generates the tidy data set
•	writes the tidy data set to tidydata.csv

It is assumed that data available in the current directory and the script file run_analysis.R resides in the current working directory. 

Data sets
Raw data set
In order to create a raw data set all variables containing -mean( or –std) in their names were filtered., using the following regular expression: -(mean|std)[(]. 
•	subject - An identifier of the subject who carried out the experiment.
•	label - An activity label.

Tidy data set
Tidy data set contains the same variables as the raw does, but the variables were renamed according to following rules:
•	All lower case when possible .
•	Descriptive - the variable names are descriptive, so nothing special should be done.
•	Not duplicated - the variable names are unique.
•	Not have underscores or dots or white spaces - dashes and parentheses were removed from variable names.

To satisfy the requirements above, the following replacements were performed:
1.	Replace -mean with Mean
2.	Replace -std with Std
3.	Remove characters -()

