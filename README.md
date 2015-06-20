# Getting-and-Cleaning-Data


# Course Project

Step 1. Unzip the source (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) into a folder on your local drive \Users\yourname\Downloads\R\

Step 2. Save run_analysis.R into \Users\yourname\Downloads\R\UCI HAR Dataset\

Step 3. In RStudio:
> setwd("\\Users\\yourname\\Downloads\\R\\UCI HAR Dataset\\")
> source("run_analysis.R")

Step 4. Read data:
> data <- read.table("UCI_HAR_averages.txt")

It has 180 rows and 68 columns.
There are 30 subjects and 6 activities.
"for each activity and each subject" means 30 * 6 = 180 rows.
