# Code Book

`R_script` contains the data preperation and analysis steps.

- Download the dataset
Dataset downloaded with URL link and zip file is extracted to UCI HAR Dataset folder
- The `feature`, `activ`,`sub_test`,`x_test`,`y_test`,`sub_train`,`x_train` and `y_train` tables are created from related txt files in the UCI HAR Dataset folder with read table comment.

After getting tables from files, I started to follow the steps described in instructions.
#### 1. Merges the training and the test sets to create one data set
- `data_x`, `data_y` and `data_sub` are obtained by rbind of related train and test data.
- The `df_merge` is the data set that includes all of three data sets that is created above. cbind function is used for it.
#### 2. Extracts only the measurements on the mean and standard deviation for each measurement. 
In this step, `data_mean_sd` is created by selecting `sub_id`, `label`, the columns contains `mean` and `std` expressions.
#### 3. Uses descriptive activity names to name the activities in the data set
The `label` column of `data_mean_sd` is updated with the `activity_name` values in the `activ` data set by matching with `label` columns. 
#### 4. Appropriately labels the data set with descriptive variable names. 
- The label column is renamed as `activity_name`.
- The sub_id is renamed as `activity_name`
- The Acc expressions in the column names are coverted to `Accelerometer`.
- The Gyro expressions in the column names are coverted to `Gyroscope`.
- The BodyBody expressions in the column names are coverted to `Body`.
- The Mag expressions in the column names are coverted to `Magnitude`.
- The t expressions in the column names are coverted to `Time`.
- The f expressions in the column names are coverted to `Frequency`.
- angle and gravity are converted to `Angle` and `Gravity`.






