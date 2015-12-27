#1
##1.1 The R code in run_analysis.R proceeds under the assumption that the zip file available at https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip is downloaded and extracted in the R Home Directory.
##1.2 The libraries used in this operation are data.table and dplyr. We prefer data.table as it is efficient in handling large data as tables. dplyr is used to aggregate variables to create the tidy data.
##1.3 The supporting metadata in this data are the name of the features and the name of the activities. They are loaded into variables featureNames and activityLabels
##1.4 Both training and test data sets are split up into subject, activity and features. They are present in three different files.
##1.5 We can use combine the respective data in training and test data sets corresponding to subject, activity and features. The results are stored in subject, activity and features.
##1.6 The columns in the features data set can be named from the metadata in featureNames
##1.7 The data in features,activity and subject are merged and the complete data is now stored in completeData.
##2.1 Extract the column indices that have either mean or std in them.
##2.2 Add activity and subject columns to the list and look at the dimension of completeData
##2.3 We create extractedData with the selected columns in requiredColumns. And again, we look at the dimension of requiredColumns
##3.1 The activity field in extractedData is originally of numeric type. We need to change its type to character so that it can accept activity names. The activity names are taken from metadata activityLabels.
##3.2 We need to factor the activity variable, once the activity names are updated.
##4.1 Here are the names of the variables in extractedData
##4.2 Acronyms can be replaced
##4.3 Here are the names of the variables in extractedData after they are edited##5.1 Firstly, let us set Subject as a factor variable.
##5.2 We create tidyData as a data set with average for each activity and subject. Then, we order the enties in tidyData and write it into data file Tidy.txt that contains the processed data

