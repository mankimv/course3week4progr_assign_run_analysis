# course3week4progr_assign_run_analysis
course 3 week 4 program assignment run_analysis body motion Samsung Galaxy data 

Experimental design and background: 

An experiment was conducted by Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto (Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws). This experiment was aimed at Human Activity Recognition Using Smartphones Dataset and was focused on collecting statistical data on linear and angular body acceleration measured within a group of 30 volunteers. Each person performing six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING). The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

Further details of the experiment can be obtained from read.me available at 
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Raw data for the experiment: 

Accelerometer and gyroscope 3-axial raw signals (variables type 'time domain:  acceleration-along XYZ axis' and 'time domain: Gyro-along XYZ axis').

Data processed by the experiment:

1) Raw signals were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals ('time domain:  Body acceleration-along XYZ axis' and 'time domain: Gravity acceleration-along XYZ axis') using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

2) Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals ('time domain: Body accelerationJerk-along XYZ axis' and 'time domain: BodyGyroJerk-along XYZ axis'). Also the magnitudes of these three-dimensional signals were calculated using the Euclidean norm ('time domain: Body accelerationMag', 'time domain: Gravity accelerationMag', 'time domain: Body accelerationJerkMag', 'time domain: BodyGyroMag', 'time domain: BodyGyroJerkMag'). 

3) Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing 'frequency domain:  Body acceleration-along XYZ axis', 'frequency domain:  Body accelerationJerk-along XYZ axis', 'frequency domain:  BodyGyro-along XYZ axis', 'frequency domain:  Body accelerationJerkMag', 'frequency domain:  BodyGyroMag', 'frequency domain:  BodyGyroJerkMag'.

4) Estimation of additional variables including mean and standard deviation (only these 2 variables are relevant to the current work - please see reasoning below). Full set of variables estimated from these signals can be obtained from features_info.txt at 
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Raw data for the course project assignment.
Item 4 (above) variables representing mean and standard deviation of respective experimental raw and processed data.

The following additional variables were excluded from the current analysis, although they carry mean context in their descriptions:
a)meanFreq() (items nr 294-296 and 452-454 as per features_info.txt) as representing weighted average as opposed to average value as prescribed by the project requirements
b)all angle functions (items nr 555-561 as per features_info.txt) - being functions of Mean values, not mean values by themselves hence falling out of the project scope.
In total, by applying the above principles, the total number of variables in scope for further analysis is 66.

Script description:
1) Training and test data sets were merged together as per the assignment instructions
2) New data set was enriched - cbind() - by data coming from subject id number ('subjects' variable) and activity type ('activity' variable)
3) Enhanced descriptions to the variables were given as per the assignment instructions
4) Resulted data was grouped - group_by() - by 2 levels: 1st - by 'subjects' 2nd - by 'activity' 
5) All the variables in scope within corresponding groups were summarised - summarise() - and averaged through mean() function.

Tidy data:
Resulting data set needs to be tidy (as per the paper of Hadley Wickham, Tidy Data, Journal of Statistical Software August 2014, Volume 59, Issue 10.):

	1) Through the design of the data collection, processing and subsequent recording process each variable is stored in a separate column describing its parameters (e.g., domain, type of acceleration, axes etc). Thus, each variable forms a column and there are no duplicate columns.
	
	2) Through the design of the experiment, 30 volunteers each perfoming 6 activities several iterations. Having averaged by subject and then by activity the resulting dataset has dimensions of [180, 68] (please see rationale for 66 above in the Raw data) where each row represents an observation and only 1 observation is assigned to 1 row. Hence the dataset complies with the 2nd principle: Each observation forms a row.
	
	3) The unit of observation (body motion) is 'parsed' (i.e., split by components, like linear/angular acceleration, axes, etc)  within the only table and its design also avoids any duplication of the same data pertinent to body motion. This tackles an issue of having multiple types of observation units in 1 table. Hence the data set is automatically compliant with the 3rd principle of tidy data: Each type of observational unit forms a table.
