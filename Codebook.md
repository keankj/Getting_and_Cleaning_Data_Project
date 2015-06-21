# Course Project Codebook

This codebook describes the variables, the data, and any transformations or work that I performed to clean up the data

1) Reads `X_train.txt` and `X_test.txt` and stores them in `t1` and `t2` respectively. Concatenate `t1` and `t2` to create `X` (10299x561 data frame). Reads `y_train.txt` and `y_test.txt` and stores them in `t1` and `t2` respectively. Concatenate `t1` and `t2` to create `Y` (10299x1 data frame). Reads `subject_train.txt` and `subject_test.txt` and stores them in `t1` and `t2` respectively. Concatenate `t1` and `t2` to create `S` (10299x1 data frame).

2) Reads `features.txt`, extracts only the measurements on the mean and standard deviation for each measurement and stores the data in a variable named `features`(10299x66 data frame). The 66 features (or columns) are as follows:
```
tbodyacc-mean-x
tbodyacc-mean-y
tbodyacc-mean-z
tbodyacc-std-x
tbodyacc-std-y
tbodyacc-std-z
tgravityacc-mean-x
tgravityacc-mean-y
tgravityacc-mean-z
tgravityacc-std-x
tgravityacc-std-y
tgravityacc-std-z
tbodyaccjerk-mean-x
tbodyaccjerk-mean-y
tbodyaccjerk-mean-z
tbodyaccjerk-std-x
tbodyaccjerk-std-y
tbodyaccjerk-std-z
tbodygyro-mean-x
tbodygyro-mean-y
tbodygyro-mean-z
tbodygyro-std-x
tbodygyro-std-y
tbodygyro-std-z
tbodygyrojerk-mean-x
tbodygyrojerk-mean-y
tbodygyrojerk-mean-z
tbodygyrojerk-std-x
tbodygyrojerk-std-y
tbodygyrojerk-std-z
tbodyaccmag-mean
tbodyaccmag-std
tgravityaccmag-mean
tgravityaccmag-std
tbodyaccjerkmag-mean
tbodyaccjerkmag-std
tbodygyromag-mean
tbodygyromag-std
tbodygyrojerkmag-mean
tbodygyrojerkmag-std
fbodyacc-mean-x
fbodyacc-mean-y
fbodyacc-mean-z
fbodyacc-std-x
fbodyacc-std-y
fbodyacc-std-z
fbodyaccjerk-mean-x
fbodyaccjerk-mean-y
fbodyaccjerk-mean-z
fbodyaccjerk-std-x
fbodyaccjerk-std-y
fbodyaccjerk-std-z
fbodygyro-mean-x
fbodygyro-mean-y
fbodygyro-mean-z
fbodygyro-std-x
fbodygyro-std-y
fbodygyro-std-z
fbodyaccmag-mean
fbodyaccmag-std
fbodybodyaccjerkmag-mean
fbodybodyaccjerkmag-std
fbodybodygyromag-mean
fbodybodygyromag-std
fbodybodygyrojerkmag-mean
fbodybodygyrojerkmag-std
```

Brackets are removed and names are set to lowercase for the feature names.

3) Read `activity_labels.txt` and store the data in a variable named "activities". Underscores are removed and names are set to lowercase for the activity names. Uses descriptive activity names to name the activities in the dataset. The 6 activities are as follows:
```
walking
walkingupstairs
walkingdownstairs
sitting
standing
laying
```

4) Merges `S`, `X` & `Y` to create a table named `cleaned` (10299x68 dataframe). First column `subject` contains subject IDs, second column `activity` contains activity names and the last 66 columns contain measurements that range between -1 to 1. Write the `cleaned` data to `merged_dataset.txt` file in the current working directory.

5) Creates another tidy dataset with the average of each variable for each activity and each subject. 30 subjects X 6 activities = 180 combinations. For each combination, the mean of each measurement is calculated with the corresponding combination (180x68 data frame). Writes the `result` to `averages_dataset.txt` file in the current working directory.