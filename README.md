# Sapark-Streaming-for-Tweets


Utilizing Spark Streaming to stream a corpus of tweets and their corresponding sentiment labels, this repository details the conduction of a study on the training and evaluation of multiple classification and clustering online/incremental learning ML models that are able to learn on batches of data streamed over time. Analysis is done on various performance metrics against varying hyperparameter and streaming batch size values; the corresponding trends are plotted for each combination of variables under analysis.

Machine Learning Pipeline


![image](https://user-images.githubusercontent.com/96236642/154924775-3077cacd-71e0-4d5f-a70d-f4c79f4f405a.png)


Current Repository Structure

.

├── Batch_1000
├── Batch_2000
├── Batch_2500
├── Batch_3000
├── Batch_4000
├── Batch_5000
├── classification_models
│   ├── logistic_regression.py
│   ├── multinomial_nb.py
│   ├── passive_aggressive.py
├── clustering_models
│   ├── kmeans_clustering.py
│   ├── birch_clustering.py
├── preprocessing
│   ├── preprocess.py
├── .gitignore
├── LICENSE
├── README.md
├── Sentiment Analysis Using Streaming Spark.pdf
├── batch_accuracy_MNB
├── batch_accuracy_PAC
├── batch_accuracy_SGD
├── batch_test_accuracies.py
├── hyper_test_accuracies.py
├── requirements.txt
├── test.py
└── train.py



About the Dataset


Two CSV files each for training (with 1520k records) and testing (with 80k records).
Each record has two columns, one for the sentiment, and the other, the tweet.
Sentiment is either 0 (negative) or 4 (positive).
Task Workflow
Streaming the data with Spark Streaming.
Cleaning and Preprocessing each RDD of input data.
Online/incremental training of the classification models.
Online/incremental training of the clustering models
Testing the classification and clustering models against cleaned and preprocessed RDDs of the test data stream.
Plotting graphs for analysis and evalutation of the models.
