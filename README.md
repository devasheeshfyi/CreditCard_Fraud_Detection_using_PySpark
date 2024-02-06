# Credit Card Fraud Detection

### GROUP NAME: THE DATA ALCHEMISTS
###  Group Number: 05

AKASH DEEP SAHA, SID: 862395008  Email: asaha037@ucr.edu

ANKIT MANE, SID: 862393644 Email: amane011@ucr.edu 

POOJA CHAKKARWAR, SID: 862396037 Email: pchak009@ucr.edu

SHUBHAM SHARMA, SID: 862394567 Email: sshar180@ucr.edu 

DEVASHEESH VAID, SID: 862395097, Email: dvaid003@ucr.edu 

## Instructions

This Jupyter Notebook contains code for credit card fraud detection using Spark and PySpark.


## Overview

The notebook performs the following tasks:
- Setup: Install necessary dependencies and set up a Spark session.
- Data Loading: Read credit card data from a CSV file.
- Data Exploration: Check for null values and explore the distribution of classes (fraudulent and non-fraudulent).
- Over and Under Sampling: Implement over and under-sampling to address class imbalance.
- Machine Learning: Use different machine learning algorithms (Logistic Regression, Random Forest, Naive Bayes, Gradient Boosting) for fraud detection.
- Model Evaluation: Evaluate the models using accuracy and F1 score.

## Prerequisites

Before running the code, make sure you have the following prerequisites installed:

- Java Development Kit (JDK) 8
- Apache Spark
- Python with required libraries (pyspark)


## Usage

### Compilation and Execution
1. Ensure that Java 8 is installed on your system.
2. Install PySpark by running the following command:
    ```bash
    !pip install pyspark
    ```

3. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/../credit-card-fraud-detection.git
    ```
    **OR**

3. Download the project as a .zip or .tar.gz file
    - Extract the downloaded file to your local machine.

4. Navigate to the project directory:
    ```bash
    cd credit-card-fraud-detection
    ```

5. Run the code in a Python environment (e.g., Jupyter Notebook, Colab) that supports PySpark.

### Setting up Spark on Colab

```python
# Install Java and PySpark
!apt-get install openjdk-8-jdk-headless -qq > /dev/null
!pip install pyspark

# Import necessary libraries
from pyspark.sql import SparkSession

# Create a Spark session
spark = SparkSession.builder.appName("CreditCardFraudDetection").getOrCreate()

# Load the dataset
file_path = "/content/creditcard.csv"
df = spark.read.csv(file_path, header=True, inferSchema=True)

# Explore the dataset
df.printSchema()
```

### Author Contributions

- **AKASH DEEP SAHA:**
  - Implemented data loading and preprocessing.
  - Conducted exploratory data analysis.

- **ANKIT MANE:**
  - Implemented oversampling for fraud class.
  - Contributed to the machine learning section.

- **POOJA CHAKKARWAR:**
  - Implemented undersampling for non-fraud class.
  - Worked on the machine learning model evaluation.

- **SHUBHAM SHARMA:**
  - Implemented logistic regression for classification.
  - Contributed to the model evaluation.

- **DEVASHEESH VAID:**
  - Implemented random forest classifier for classification.
  - Conducted additional model evaluation using F1 score.




