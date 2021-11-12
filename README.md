# Parkinsons Disease Classification
##Semester project for Data Mining
The aim of our project is to learn how to classify if a patient has PD or not, given speech and hand-drawn image data specific to the patient. We try to assess if merging of different datasets using techniques like data imputation can help us train models with less bias which are more generalizable.

##Literature Review
Past work in the domain of PD classification includes the utilization of a wide variety of data- wearable-sensor data, data related to genetic factors, brain
MRI scans, data about gut microbiota, speech data, and data obtained from drawings. The trade-off however is data collection, and collecting large amounts of data is quite difficult. During our literature survey of the problem we observed that there are a lot of datasets, but all of them are small (< 200 subjects), and often have multiple samples from the same subject. This motivated us to ask if information from these small, multi-modal datasets be merged together for better generalizability on unseen data. 

##Novelty
We used Generative Aversarial Imputation Networks (GAINs) to merge the different datasets and then construcuted a hybrid model which combined the results obtained from a MLP classifier that had been trained on the speech dataset and a CNN which had been trained on the hand-drawn images dataset.

##Conclusion
We observed that using the imputed data gave better results and using the hybrid model, where we merged all 3 datasets (SL+MSR+HD), we were able to obtain an accuracy of 93.65%, which is higher than all the baseline models used before with any of the datasets. These experiments show that data imputation using GAIN is indeed a powerful tool as it allows merging of different types of data. The imputed data is more generalizable and gives better results.

## Future Work
In the future we could try to construct more complex GANs which would take in to account the different weightage of different features in the datasets, and impute the data using prior knowledge about the 2 datasets being merged to produce better results. There are also some video datasets for Parkinson’s which we have not used in this project. In the future we could also try imputing 3 different modes of data (video+speech+images) and hope to obtain even better classification accuracy.
