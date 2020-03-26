---
title: "CodeBook.md"
author: "shubham"
date: "26/03/2020"
output: html_document
---

# The run_analysis.R script performs the 5 steps required as described in the course project’s definition.

## *1. Merges the training and the test sets to create one data set*

### * xDataSet (10299 rows, 561 columns) is created by merging xTrain and xTest using rbind() function
      
### * yDataSet (10299 rows, 1 column) is created by merging yTrain and yTest using rbind() function
      
### * subjectDataSet (10299 rows, 1 column) is created by merging subjectTrain and subjectTest using rbind() function
      

## *2. Extracts only the measurements on the mean and standard deviation for each measurement*

###  * xDataSet_mean_std (10299 rows, 66 columns) is created by subsetting xDataSet, selecting only columns: subject, code and the  measurements on the mean and standard deviation (std) for each measurement
      

## *3. Uses descriptive activity names to name the activities in the data set*

### * Entire numbers in code column is replaced with corresponding activity taken from second column of the activities variable


## *4. Appropriately labels the data set with descriptive variable names*
      
### * code column renamed into activities
      
### * All Acc in column’s name replaced by Acceleration
      
### * All Gyro in column’s name replaced by AngularSpeed
      
### * All Mag in column’s name replaced by Magnitude
      
### * All start with character f in column’s name replaced by FrequencyDomain
      
### * All start with character t in column’s name replaced by TimeDomain
      
### * All GyroJerk in column’s name replaced by AngularAcceleration
      
### * All ending with Freq replaced by Frequency
###  ...


## *5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject*

### * Data2 (180 rows, 68 columns) is created by sumarizing TidyData taking the means of each variable for each activity and each subject, after groupped by subject and activity.


## *Export Data2 into tinyData.txt file.*

