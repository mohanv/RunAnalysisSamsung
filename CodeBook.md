##run_analysis.R

####Prerequisites
Place the zipfile set in the same directory as the run_analysis.R and unzip its contents so that they are extracted to the folder
"UCI HAR Dataset"
Make sure you set the current working directory to the directory of the r source file.

####Usage
Run the r source file by using the source command.  It will scan through all the test and train files and merge them to one and
create a file tidyData.csv file which is comma delimited and has the activity, subject and the average of various measurements.

####Variables
The following variables are used in the script
testX, testY, testSubject, trainX, trainY, trainSubject - representing the X, Y and subject for test and train
mergedTestData, mergedTrainData - representing the merged values of test and train
tidyData - Final consoidated table which is written to the file

####Transformations
All the test and train data are merged and mergedData is created with friendly names (except for the features) and only the features that have calculate
mean and standard deviation 
A data table dt is created from the mergedData to be used later to get the mean of the various measurements based on activity and subject
The feature names are later applied and written to file
