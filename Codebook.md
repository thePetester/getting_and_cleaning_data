---
title: "CodeBook"
author: "thepetester"
date: "Wednesday, January 21, 2015"
output: html_document
---

H1 Introduction
===================
The script run_analysis.Rperforms the 5 steps described in the course project's definition.

**Step 1** - Merge the training and test sets into one data set.
**Step 2** - Extract the measurements on the mean and standard deviations.
**Step 3** - Use descriptive activity names in the data set.
**Step 4** - Appropriately label the data set with descriptive variable names
**Step 5** - Create a second, independent tidy data set with the average of each variable for each activity and each subject and write to file

H1 Variables
================
-**x_train**, **y_train**, **x_test**, **y_test** contain the data from the downloaded files.
-**x_data**, **y_data** and **all_data** merge the previous datasets to further analysis.
-**features** contains the correct names for the **x_data dataset**, which are  applied to the column names stored in -**mean_and_std_features**, a numeric vector used to extract the desired data.
-A similar approach is taken with activity names through the activities variable.
-**all_data** merges x_data, y_data in a big dataset.
-Finally, averages_data contains the relevant averages which will be later stored in a averages_data.txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.

