## Data

Raw training and testing data sets contains various variables that were collected for 30 persons for 6 activities. Each row is one observation for one person and one activity and variables are in different columns.

Variable measures, person identification through subject id and activity identification for activity id are in seperate file

## Project Obective

Is to merge all the information which is present in different files to create a data set which has all variables information for all person and activities. After that a new data set has to be created for mean of different variables which are either means or standard deviation in nature from original data set

## Step 1

Script reads all the training and testing files seperately. It also reads global lookups like what does all columns stands for and what is the activity description.

It then provides the column names to various columns in different tables based on the information shared.

It then combines the subject ids and activity ids with respective training and testing data.

Finally training and testing data is merged together.

## Step 2

Script creates a list of column names from the merged data.

It then creates a logical vector to choose only the columns which are means and standard deviations in nature.

Based on the logical vector, it modifies the merged Data to remove the comlumns which not means and standard deviations in nature as final calculations will be done on these columns only

## Step 3

Script merged the modified merged data with activity lookup to get activity descriptions of all 6 activities


## Step 4

Agains creates a list of columns names which will be cleaned.

It then provides he description of various abbrevaitions used in column names to be more descriptive and meaningful.

Finally the column names of data set is replaced by cleaned names

## Step 5

Reshape library is loaded to use some functions out of it

Data is melted in rows by subject id and activity id giving a long format.

Melted data is the dcasted for all the variables, this time to get mean of all observations for a subject and activity.
