# Machine-Learning-2

# Recommendation Engine with ALS Model - MovieLens Dataset

![flowchart](https://github.com/franketang/Machine-Learning-2/assets/29631514/864dd113-8395-4e97-bdc3-fa7e05ea07bf)


## Introduction

This repository contains a Python program that showcases the implementation of a powerful recommendation engine using the ALS (Alternating Least Squares) model on the MovieLens dataset. The MovieLens dataset is a widely recognized benchmark dataset in the world of recommendation systems. Our program utilizes PySpark, a Python library designed for distributed data processing, to conduct collaborative filtering. The end result? Personalized movie recommendations for users that can revolutionize the user experience.

![Google Slides Presentation](https://docs.google.com/presentation/d/1mula9arywAMuA7I4tyndwqpnv4cR1gbvFhmNFjGHQmo/edit?usp=drive_link)

## Design

Here's an overview of the key steps and design of our recommendation engine:

1. **Data Loading and Preprocessing**:
   - We load movie and rating data from CSV files.
   - Cleanse and preprocess the data, including type conversions and handling missing values.

2. **Data Analysis**:
   - Calculate the sparsity of the ratings dataset to understand data density.
   - Analyze the distribution of ratings by grouping data by userId and movieId.

3. **Model Building**:
   - Construct an ALS model using the PySpark ML library for collaborative filtering.
   - Configure hyperparameter tuning via cross-validation to optimize the ALS model.

4. **Training and Evaluation**:
   - Train the ALS model on the training dataset.
   - Select the best model based on evaluation metrics, enhancing recommendation accuracy.
   - Evaluate model performance on the test dataset using RMSE (Root Mean Squared Error).

5. **Recommendation Generation**:
   - Generate personalized movie recommendations for all users utilizing the best model.
   - Enhance interpretability by merging movie names and genres with the recommendation matrix.

6. **Presentation and Comparison**:
   - Display the recommendations.
   - Compare recommendations with actual ratings for a specific user.

## Implementation

### Prerequisites

Before you dive into running this recommendation engine, make sure you have the following:

- **Google Cloud Platform Account**: If you don't have one, sign up for a Google Cloud Platform account.

- **Google Cloud Storage Bucket**: Create a Google Cloud Storage (GCS) bucket to store your input data.

- **Dataproc Cluster**: Create a Dataproc cluster with the necessary configuration and access to your GCS bucket.

### Steps

1. **Upload Data to GCS Bucket**:
   - Upload the following dataset files to your GCS bucket:
     - `ratings.csv`
     - `movies.csv`
     - `tags.csv`

2. **Upload the Script**:
   - Upload the `recommendation_engine.py` script to the same GCS bucket.

3. **Create a Dataproc Cluster**:
   - Go to the [Google Cloud Console](https://console.cloud.google.com).
   - Select your project.
   - In the Navigation menu, click on "Dataproc" under the "Big Data" section.
   - Click on the "Create cluster" button to configure and create a new cluster.

4. **Submit a Job**:
   - In the Navigation menu, click on "Dataproc" under the "Big Data" section.
   - Click on the "Jobs" tab.
   - Click on the "Submit job" button to create a new job submission.
   - Provide job details, including the region, cluster, job type (PySpark), and the path to the `recommendation_engine.py` script in your GCS bucket.
   - Click the "Submit" button to run the job.

5. **Check the Output**:
   - Monitor the job progress and check the output for your personalized movie recommendations.

With these steps, you can harness the power of collaborative filtering and deliver exceptional movie recommendations to your users.

For more details, please refer to the [Google Slides Presentation](https://docs.google.com/presentation/d/1mula9arywAMuA7I4tyndwqpnv4cR1gbvFhmNFjGHQmo/edit#slide=id.p)https://docs.google.com/presentation/d/1mula9arywAMuA7I4tyndwqpnv4cR1gbvFhmNFjGHQmo/edit#slide=id.p) linked above.

Enjoy exploring and enhancing your recommendation engine!
