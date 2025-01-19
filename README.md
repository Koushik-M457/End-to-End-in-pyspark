# End-to-End-in-pyspark

This project leverages PySpark to process and analyze large datasets related to flight and airport information. The workflow demonstrates data preprocessing, exploratory analysis, and building a machine learning pipeline to predict flight delays. The project showcases PySpark's capabilities for big data processing and machine learning in distributed environments.

Features

Data Processing

Load and preprocess flight and airport datasets.

Handle missing values and cast columns to appropriate data types.

Add calculated fields such as duration_hrs (flight duration in hours) and plane_age (age of the airplane).

Data Exploration and Aggregation

Perform filtering and aggregation to identify patterns and trends in the dataset.

Example analyses:

Long flights (distance > 1000 miles).

Average flight times grouped by origin airport.

Feature Engineering

Encode categorical variables such as carrier and destination using:

StringIndexer for indexing.

OneHotEncoder for encoding into numerical vectors.

Assemble features into a single vector using VectorAssembler.

Machine Learning Pipeline

Build a pipeline for logistic regression to predict whether a flight is delayed.

Utilize cross-validation for hyperparameter tuning:

Regularization parameter (regParam).

ElasticNet parameter (elasticNetParam).

Evaluate the model using the area under the ROC curve (AUC).

Datasets

Flight Dataset: Contains flight information such as origin, destination, carrier, air time, and delay.

Airport Dataset: Provides metadata about airports.

Plane Dataset: Includes details about airplanes, such as their year of manufacture.

Prerequisites

Software Requirements

Python 3.7+

Apache Spark 3.0+ with PySpark

Python Libraries

Install the required libraries using the following command:

pip install pyspark numpy pandas

How to Run

Clone or Download the Repository:

git clone <repository-url>
cd <repository-directory>

Set Up PySpark:

Install Apache Spark and ensure it is accessible from your system.

Run the Notebook:
Open the Jupyter Notebook file (pyspark.ipynb) and execute the cells step by step.

Train and Evaluate the Model:

Follow the notebook to train the logistic regression model.

Use the test dataset to evaluate its performance (e.g., AUC score).

Key Results

Insights:

Identified significant trends in flight durations and delays.

Built a logistic regression model to predict delays with a high AUC score.

Future Enhancements

Explore additional machine learning algorithms such as decision trees or random forests.

Use more comprehensive datasets for better modeling.

Deploy the model as a REST API or integrate it with a visualization dashboard.

Acknowledgments

Apache Spark for providing a scalable and efficient framework for big data processing.

Python community for supporting PySpark libraries and tools.


