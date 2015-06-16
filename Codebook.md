# Course Project Codebook

1) Merges training and test sets to create one dataset (10299x561 data frame).
2) Extracts only the measurements on the mean and standard deviation for each measurement (10299x66 data frame).
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

3) Uses descriptive activity names to name the activities in the dataset.
```
walking
walkingupstairs
walkingdownstairs
sitting
standing
laying
```

4.) Appropriately labels the dataset (`merged_dataset.txt`) with descriptive activity names. 
5) Creates another tidy dataset (`averages_dataset.txt`) with the average of each variable for each activity and each subject. 30 subjects X 6 activities = 180 averages.