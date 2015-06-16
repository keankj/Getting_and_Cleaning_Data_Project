# Explanation for `run_analysis.R`

1. Merges  training and  test sets to create one dataset.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the dataset.
4. Appropriately labels the dataset (`merged_dataset.txt`) with descriptive activity names. 
5. Creates another tidy dataset (`averages_dataset.txt`) with the average of each variable for each activity and each subject.