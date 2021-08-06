# Wafer_Fault_Detection
 Problem Statement was to build classification methodology to predict the quality of wafer sensors based on the given training data.
 
# Data Description
1.Data will contain Wafer names and 590 columns of different sensor values for each wafer. The last column will have the "Good/Bad" value for each wafer.
2. "Good/Bad" column will have two unique values +1 and -1.
3. "+1" represents Bad wafer and  "-1" represents Good Wafer.

# Data Validation
- We validate the name of the files based on the given name in the schema file. We have created a regex pattern as per the name given in the schema file to use for validation. After validating the pattern in the name, we check for the length of date in the file name as well as the length of time in the file name. If all the values are as per requirement, we move such files to "Good_Data_Folder" else we move such files to "Bad_Data_Folder."

# Model Training 
- Clustering - KMeans algorithm is used to create clusters in the preprocessed data. The optimum number of clusters is selected by plotting the elbow plot, and for the 
dynamic selection of the number of clusters, we are using "KneeLocator" function. The idea behind clustering is to implement different algorithms, to train data in 
different clusters. The Kmeans model is trained over preprocessed data and the model is saved for further use in prediction.

# Prediction 

-  Clustering - KMeans model created during training is loaded, and clusters for the preprocessed prediction data is predicted.
-  Prediction - Based on the cluster number, the respective model is loaded and is used to predict the data for that cluster









