# Course Project Code Book

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.  

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Here are the data for the project: 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 


The R script (run_analysis.R) does the following:

1. Merges the training and the test sets to create one data set:
train/X_train.txt and test/X_test.txt: a 10299x561 data frame ("Number of Instances: 10299" and "Number of Attributes: 561").
train/subject_train.txt and test/subject_test.txt: a 10299x1 data frame with subject IDs.
train/y_train.txt and test/y_test.txt: a 10299x1 data frame with activity IDs.

2. Extracts only the measurements on the mean and standard deviation for each measurement:
features.txt: a 10299x66 data frame. Only 66 out of 561 attributes are measurements on the mean and standard deviation.

3. Uses descriptive activity names to name the activities in the data set:
activity_labels.txt:
```
walking
walkingupstairs
walkingdownstairs
sitting
standing
laying
```

4. Appropriately labels the data set with descriptive variable names:
* Feature names (attributes) and activity names are converted to lower case. Underscores and brackets () are removed.
* Merge 10299x66 data frame containing features with 10299x1 data frames containing activity labels and subject IDs.
* Save the result as UCI_HAR_tidy_data.txt, a 10299x68 data frame containing subject IDs, activity names, and measurements. 

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
* Save the result as UCI_HAR_averages.txt, a 80x68 data frame.
