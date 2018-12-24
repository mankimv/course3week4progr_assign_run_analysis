Experimental design and background: 

An experiment was conducted by Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto (Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws).

This experiment was aimed at Human Activity Recognition Using Smartphones Dataset and was focused on collecting statistical data on linear and angular body acceleration. 

Details of the experiment can be obtained from read.me available at 
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The current project assignment aims to extract mean and standard deviation variables from the experiment output, average them across subjects and their activities, ensuring the resulting data set is tidy as per the tidy data principles (Hadley Wickham, Tidy Data, Journal of Statistical Software August 2014, Volume 59, Issue 10.) 

Raw data for the assignment (please see readme file for details of arriving at these variables): 

 fBodyAccJerk-mean()-X; fBodyAccJerk-mean()-Y; fBodyAccJerk-mean()-Z; fBodyAccJerk-std()-X; fBodyAccJerk-std()-Y; fBodyAccJerk-std()-Z; fBodyAccMag-mean(); fBodyAccMag-std(); fBodyAcc-mean()-X; fBodyAcc-mean()-Y; fBodyAcc-mean()-Z; fBodyAcc-std()-X; fBodyAcc-std()-Y; fBodyAcc-std()-Z; fBodyBodyAccJerkMag-mean(); fBodyBodyAccJerkMag-std(); fBodyBodyGyroJerkMag-mean(); fBodyBodyGyroJerkMag-std(); fBodyBodyGyroMag-mean(); fBodyBodyGyroMag-std(); fBodyGyro-mean()-X; fBodyGyro-mean()-Y; fBodyGyro-mean()-Z; fBodyGyro-std()-X; fBodyGyro-std()-Y; fBodyGyro-std()-Z; tBodyAccJerkMag-mean(); tBodyAccJerkMag-std(); tBodyAccJerk-mean()-X; tBodyAccJerk-mean()-Y; tBodyAccJerk-mean()-Z; tBodyAccJerk-std()-X; tBodyAccJerk-std()-Y; tBodyAccJerk-std()-Z; tBodyAccMag-mean(); tBodyAccMag-std(); tBodyAcc-mean()-X; tBodyAcc-mean()-Y; tBodyAcc-mean()-Z; tBodyAcc-std()-X; tBodyAcc-std()-Y; tBodyAcc-std()-Z; tBodyGyroJerkMag-mean(); tBodyGyroJerkMag-std(); tBodyGyroJerk-mean()-X; tBodyGyroJerk-mean()-Y; tBodyGyroJerk-mean()-Z; tBodyGyroJerk-std()-X; tBodyGyroJerk-std()-Y; tBodyGyroJerk-std()-Z; tBodyGyroMag-mean(); tBodyGyroMag-std(); tBodyGyro-mean()-X; tBodyGyro-mean()-Y; tBodyGyro-mean()-Z; tBodyGyro-std()-X; tBodyGyro-std()-Y; tBodyGyro-std()-Z; tGravityAccMag-mean(); tGravityAccMag-std(); tGravityAcc-mean()-X; tGravityAcc-mean()-Y; tGravityAcc-mean()-Z; tGravityAcc-std()-X; tGravityAcc-std()-Y; tGravityAcc-std()-Z;

Description of the variables above:
- leading "t" or "f" designates time or frequency domain
- Body/Gravity designates linear or angular acceleration instigated either by physical body movement or gravity force
- Acc - linear acceleration signal
- Gyro - angular acceleration signal
- Jerk - linear or angular acceleration signal derived in time
- Mag - magnitudes of signals based on Euclidean norm calculation
- X, Y, Z - reference to respective 3 dimensions along which the linear/angular acceleration signals were measured

Processed data for the current work:
1) Training and test data sets were merged together as per the assignment instructions
2) New data set was enriched by data coming from subject id number ('subjects' variable) and activity type ('activity' variable)
3) Enhanced descriptions to the variables were given as per the assignment instructions:
 [1] time domain: Body acceleration-mean-along X axis                                    
 [2] time domain: Body acceleration-mean-along Y axis                                    
 [3] time domain: Body acceleration-mean-along Z axis                                    
 [4] time domain: Body acceleration-standard deviation-along X axis                      
 [5] time domain: Body acceleration-standard deviation-along Y axis                      
 [6] time domain: Body acceleration-standard deviation-along Z axis                      
 [7] time domain: Gravity acceleration-mean-along X axis                                 
 [8] time domain: Gravity acceleration-mean-along Y axis                                 
 [9] time domain: Gravity acceleration-mean-along Z axis                                 
[10] time domain: Gravity acceleration-standard deviation-along X axis                   
[11] time domain: Gravity acceleration-standard deviation-along Y axis                   
[12] time domain: Gravity acceleration-standard deviation-along Z axis                   
[13] time domain: Body acceleration jerk signal-mean-along X axis                        
[14] time domain: Body acceleration jerk signal-mean-along Y axis                        
[15] time domain: Body acceleration jerk signal-mean-along Z axis                        
[16] time domain: Body acceleration jerk signal-standard deviation-along X axis          
[17] time domain: Body acceleration jerk signal-standard deviation-along Y axis          
[18] time domain: Body acceleration jerk signal-standard deviation-along Z axis          
[19] time domain: Body angular velocity-mean-along X axis                                
[20] time domain: Body angular velocity-mean-along Y axis                                
[21] time domain: Body angular velocity-mean-along Z axis                                
[22] time domain: Body angular velocity-standard deviation-along X axis                  
[23] time domain: Body angular velocity-standard deviation-along Y axis                  
[24] time domain: Body angular velocity-standard deviation-along Z axis                  
[25] time domain: Body angular velocity jerk signal-mean-along X axis                    
[26] time domain: Body angular velocity jerk signal-mean-along Y axis                    
[27] time domain: Body angular velocity jerk signal-mean-along Z axis                    
[28] time domain: Body angular velocity jerk signal-standard deviation-along X axis      
[29] time domain: Body angular velocity jerk signal-standard deviation-along Y axis      
[30] time domain: Body angular velocity jerk signal-standard deviation-along Z axis      
[31] time domain: Body acceleration magnitude-mean                                       
[32] time domain: Body acceleration magnitude-standard deviation                         
[33] time domain: Gravity acceleration magnitude-mean                                    
[34] time domain: Gravity acceleration magnitude-standard deviation                      
[35] time domain: Body acceleration jerk signal magnitude-mean                           
[36] time domain: Body acceleration jerk signal magnitude-standard deviation             
[37] time domain: Body angular velocity magnitude-mean                                   
[38] time domain: Body angular velocity magnitude-standard deviation                     
[39] time domain: Body angular velocity jerk signal magnitude-mean                       
[40] time domain: Body angular velocity jerk signal magnitude-standard deviation         
[41] frequency domain: Body acceleration-mean-along X axis                               
[42] frequency domain: Body acceleration-mean-along Y axis                               
[43] frequency domain: Body acceleration-mean-along Z axis                               
[44] frequency domain: Body acceleration-standard deviation-along X axis                 
[45] frequency domain: Body acceleration-standard deviation-along Y axis                 
[46] frequency domain: Body acceleration-standard deviation-along Z axis                 
[47] frequency domain: Body acceleration jerk signal-mean-along X axis                   
[48] frequency domain: Body acceleration jerk signal-mean-along Y axis                   
[49] frequency domain: Body acceleration jerk signal-mean-along Z axis                   
[50] frequency domain: Body acceleration jerk signal-standard deviation-along X axis     
[51] frequency domain: Body acceleration jerk signal-standard deviation-along Y axis     
[52] frequency domain: Body acceleration jerk signal-standard deviation-along Z axis     
[53] frequency domain: Body angular velocity-mean-along X axis                           
[54] frequency domain: Body angular velocity-mean-along Y axis                           
[55] frequency domain: Body angular velocity-mean-along Z axis                           
[56] frequency domain: Body angular velocity-standard deviation-along X axis             
[57] frequency domain: Body angular velocity-standard deviation-along Y axis             
[58] frequency domain: Body angular velocity-standard deviation-along Z axis             
[59] frequency domain: Body acceleration magnitude-mean                                  
[60] frequency domain: Body acceleration magnitude-standard deviation                    
[61] frequency domain: BodyBody acceleration jerk signal magnitude-mean                  
[62] frequency domain: BodyBody acceleration jerk signal magnitude-standard deviation    
[63] frequency domain: BodyBody angular velocity magnitude-mean                          
[64] frequency domain: BodyBody angular velocity magnitude-standard deviation            
[65] frequency domain: BodyBody angular velocity jerk signal magnitude-mean              
[66] frequency domain: BodyBody angular velocity jerk signal magnitude-standard deviation
4) Resulted data was grouped by 2 levels: 1st - by 'subjects' 2nd - by 'activity' 
5) Mean() function was applied to all the variables in scope within corresponding groups and, for consistency, 'mean' was appended - paste() - to the variable names above.
