# Authors
Simone Di Luna, [@Giulio Cordova](https://github.com/zenith378), [@Lia Trapanese](https://github.com/lia-trapanese)

# Project Guidelines

* Module 1 - Imbalanced Learning, Dimensionality Reduction, Anomaly Detection
    1. Explore and prepare the dataset. You are allowed to take inspiration from existing notebooks you can find online and figure out your personal research perspective (from choosing a subset of variables to the class to predict…). You are welcome in creating new variables and performing all the pre-processing steps the dataset needs.
    1. Define one or more (simple) classification tasks and solve them with Decision Tree and KNN.
    1. Identify the top 1% outliers: adopt at least three different methods from different families (e.g., density-based, angle-based… ) and compare the results. Deal with the outliers by removing them from the dataset or by treating the anomalous variables as missing values and employing replacement techniques. In this second case, you should check that the outliers are not outliers anymore. Justify your choices in every step.
    1. Analyze the value distribution of the class to predict with respect to point 2; if it is unbalanced leave it as it is, otherwise turns the dataset into an imbalanced version (e.g., 96% - 4%, for binary classification). Then solve the classification task using the Decision Tree or the KNN by adopting various techniques of imbalanced learning.
    1. Exploit and tests different dimensionality reduction techniques for (i) visualization in two dimensions, (ii) improve classification performance, (iii) improve outlier detection.
    1. Draw your conclusions about the techniques adopted in this analysis.
* Module 2 - Advanced Classification Methods
    1. Solve the classification task defined in Module 1 (or define new ones) with the other classification methods analyzed during the course: Naive Bayes Classifier, Logistic Regression, Support Vector Machines, Neural Networks, Ensemble Methods, Gradient Boosting Machines and evaluate each classifier with the techniques presented in DM1 (accuracy, precision, recall, F1-score, ROC curve). Perform hyper-parameter tuning phases and justify your choices.
    1. Besides the numerical evaluation draw your conclusions about the various classifiers, e.g. for Neural Networks: what are the parameter sets or the convergence criteria which avoid overfitting? For Ensemble classifiers how the number of base models impact the classification performance? For any classifier which is the minimum amount of data required to guarantee an acceptable level of performance? Is this level the same for any classifier? What is revealing the feature importance of Random Forests?
    1. Select two continuous attributes, define a simple linear univariate regression problem and try to solve it using different techniques reporting various evaluation measures. Plot the two-dimensional dataset. Then generalize to multiple linear regression and observe how the performance varies. Solve it using linear regressions, regularized linear regressions (such as Lasso and Ridge) but also machine learning approaches such as Gradient Boosting Machines.
* Module 3 - Time Series Analysis
    1. Prepare a dataset on which you can run time series clustering; motif/anomaly discovery and classification.
    1. On the dataset created, compute classification with KNN based on Euclidean/Manhattan and DTW distances and compare the results.
    1. To perform the clustering you can choose among different distance functions and clustering algorithms. Remember that you can reduce the dimensionality through time series approximation. Analyze the clusters and highlight similarities and differences.
    1. Analyze the dataset for finding motifs and/or anomalies. Visualize and discuss them and their relationship with other features.
    1. Solve the classification task on the time series dataset(s) and evaluate each result. In particular, you should use shapelet-based classifiers and structural-based classifiers. Analyze the shapelets retrieved and discuss if there are any similarities/differences with motifs and/or shapelets.
* Module 4 - Sequential Patterns and Advanced Clustering
    1. Sequential Pattern Mining: Convert the time series into a discrete format (e.g., by using SAX) and extract the most frequent sequential patterns (of at least length 3/4) using different values of support, then discuss the most interesting sequences.
    1. Advanced Clustering: On a dataset already prepared for one of the previous tasks in Module 1 or Module 2, run at least one clustering algorithm presented in the advanced clustering lectures (e.g. X-Means, Bisecting K-Means, OPTICS). Discuss the results that you find analyzing the clusters and reporting external validation measures (e.g SSE, silhouette).
* Module 5 - Explainability
Try to use one or more explanation methods (e.g., TREPAN, LIME, LORE, SHAP, Counterfactual Explainers, etc.) to illustrate the reasons for the classification in one of the steps of the previous tasks.


# About the dataset

The experiments have been carried out with a group of **30 volunteers** within an age bracket of 19-48 years. Each person performed **six activities** (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a **smartphone** (Samsung Galaxy S II) on the waist. Using its embedded **accelerometer and gyroscope**, we captured 3-axial **linear acceleration** and 3-axial **angular velocity** at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained **dataset has been randomly partitioned into two sets**, where **70%** of the volunteers was selected for generating the **training data** and **30% the test data**. 

**The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window)**. The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. **From each window, a vector of features was obtained by calculating variables from the time and frequency domain**. See 'features_info.txt' for more details. 

For each record it is provided:
=================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.
- The units used for the accelerations (total and body) are 'g's (gravity of earth -> 9.80665 m/seg2).
- The gyroscope units are rad/seg.
- A video of the experiment including an example of the 6 recorded activities with one of the participants can be seen in the following link: http://www.youtube.com/watch?v=XOEN9W05_4A

For more information about this dataset please contact: activityrecognition '@' smartlab.ws

Feature Selection 
=================

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (**prefix 't' to denote time**) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

<details>
    
- tBodyAcc-XYZ
- tGravityAcc-XYZ
- tBodyAccJerk-XYZ
- tBodyGyro-XYZ
- tBodyGyroJerk-XYZ
- tBodyAccMag
- tGravityAccMag
- tBodyAccJerkMag
- tBodyGyroMag
- tBodyGyroJerkMag
- fBodyAcc-XYZ
- fBodyAccJerk-XYZ
- fBodyGyro-XYZ
- fBodyAccMag
- fBodyAccJerkMag
- fBodyGyroMag
- fBodyGyroJerkMag
    
</details>    

The set of variables that were estimated from these signals are: 

<details>
    
- mean(): Mean value
- std(): Standard deviation
- mad(): Median absolute deviation 
- max(): Largest value in array
- min(): Smallest value in array
- sma(): Signal magnitude area
- energy(): Energy measure. Sum of the squares divided by the number of values. 
- iqr(): Interquartile range 
- entropy(): Signal entropy
- arCoeff(): Autorregresion coefficients with Burg order equal to 4
- correlation(): correlation coefficient between two signals
- maxInds(): index of the frequency component with largest magnitude
- meanFreq(): Weighted average of the frequency components to obtain a mean frequency
- skewness(): skewness of the frequency domain signal 
- kurtosis(): kurtosis of the frequency domain signal 
- bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
- angle(): Angle between to vectors.
    
</details>
    
Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

- gravityMean
- tBodyAccMean
- tBodyAccJerkMean
- tBodyGyroMean
- tBodyGyroJerkMean

The complete list of variables of each feature vector is available in 'features.txt'

Reference
=========
For more information see: Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. A Public Domain Dataset for Human Activity Recognition Using Smartphones. 21th European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning, ESANN 2013. Bruges, Belgium 24-26 April 2013.
