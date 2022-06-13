Applying ML approaches to real-world problems requires some extra steps in handling specific data artifacts. Some common challenges you may face are missing values, an imbalance of the labels, or heavy-tailed distributions in the data. These can be addressed through a specific choice of pre-processing and/or model components.

In this task, as an illustration of a real-world problem, you are asked to predict the evolution of hospital patients' states and needs during their stay in the Intensive Care Unit (ICU). For each patient, you are provided with the monitoring information collected during the first 12h of their stay. From the data, you first need to extract meaningful features describing this 12h stay. Then, for each sub-task, you should select an appropriate model to train on your pre-processed data. You will face the typical challenges of working with real medical data: missing features and imbalanced classification, predicting rarely-occuring events

The handout you download contains the following files:

train_features.csv training set features

train_labels.csv training set labels

test_features.csv test set features

sample.zip a sample submission file in the correct format, compressed

score_submission.py code to illustrate how the server calculates the score for a submission

The training (train_features.csv) and test set (test_features.csv) are both arranged in the same way. Each row contains the information for a patient at a given time identified by a unique patient ID and timestamp in columns pid and Time. The rest of the columns are medical information, either vital signs such as the Heart rate, or lab tests such as Calcium level in the patient blood. Finally, you are provided with the Age of the patient which is the same during the entire stay.

All medical measurements are not available at each timestep, meaning the data contains a lot of missing values, indicated with ‘nan’ in our case. To simplify the problem, the data is already re-sampled hourly. This means that we aggregate measurements by one-hour period, thus there are only 12 rows for a given patient in the corresponding .csv file.

The last .csv file, namely train_labels.csv, contains the ground truth labels of the training set for each subtask. Each row is identified by a unique pid corresponding to a patient from the training set.
