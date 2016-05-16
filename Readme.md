#Course Project for the course of Getting and Cleaning Data.

Contains run_analysis.R and CodeBook.md.

##Script: run_analysis.R

Description:

The script assumes that the root directory of the data set provided by the course is located in the same location which is named "UCI HAR Dataset".

The script does the following actions:
- Looks for the directory containing the dataset and downloads it from the source and unzips it if not found.
- Reads the test data set (x, y and subject) and merge into one dataset named test.frame.
- Reads the train data set (x, y and subject) and merge into one dataset named train.frame.
- Merge test and train dataset into Data.full.
- Read feature names from the features.txt file.
- Remove duplicate names and apply as column labels to the merged dataset.
- Extract only the columns containing mean and std in their names (excluding freq and angle) to Data.new.
- Read activity labels from the provided activity_labels.txt file.
- Replace activity codes with labels in dataset.
- Rename the columns with tidy names.
- Calculate the mean for each group of subject and activity.
- Write tidy dataset and summary dataset to csv files.
