# Financial Forensics: Exposing Malicious Transactions using AI

- The primary objective of this project is to detect fraud in a financial system as efficient as possible using AI. 

- Fraud is an important problem that impacts the whole economy. Currently, there is a lack of public research into the detection of fraud. One important reason is the lack of transaction data which is often sensitive.

## Dataset Overview

1. **Description :**
    - This dataset is based on synthetic transactional data that contains both: normal customer behaviour and fraudulent behaviour. 

    - These synthetic data points were generated from Multi Agent-Based Simulations (MABS) and were calibrated using real data from financial transactions.

    - Agents were developed that represent the clients and merchants in one simulator and customers and salesmen in another.

    - The normal behaviour was based on behaviour observed in data from the field, and is codified in the agents as rules of transactions and interaction between clients and merchants, or customers and salesmen.

    - Some of these agents were intentionally designed to act fraudulently, based on observed patterns of real fraud.

2. **Data Features and Attributes :**
    - The synthetic data consisted over 6.3 million rows which was further augmented to a data consisting of over 12.7 million data points to have an equal ratio of legitimate and fraud transactions. 

    - The attributes in the original synthetic data consisted of - type, amount, nameOrig, oldbalanceOrg, newbalanceOrig, newbalanceDest, isFraud, isFlaggedFraud, and many more. 

## Code Related

1. For running in the local machine - 
    - git clone <repo_name>
    - conda activate venv

2. Libraries (might) have to be installed - 
    - tensorflow
    - tensorflow-diretml-plugin (gpu-based)
    - fast_ml
    - imblearn

## Flow of the Project 

1. **Data Analysis, Preprocessing, Engineering:**
    - Addressed duplicates, missing values, null values, etc., ensuring its impact on business analysis.
    - Conducted in-depth analysis, including legitimacy of transactions involving accounts with zero balances, distributions of fraudulent transactions across transaction types and many more.
    - Performed logical data cleaning and transformation.
    - Augmented the dataset to over 12.7 million data points. 

2. **Models used for detection:**
    - Logistic Regression
    - XgBoost
        - vanilla
        - hyperparameter tuned
    - DeepNet

## Observations

1. All the models give more-or-less similar results in terms of accuracy. 
2. Emphasis was placed on the metric of Recall (False Negative), with close monitoring across all models.
3. The recall values of the models were as follows - 
    - Logistic model = 9538 (fastest execution)
    - Vanilla XgBoost = 1144
    - Tuned XgBoost = 283
    - DeepNet = 922
    - DeepNet tuned (HyperBand) = 768

## Results

- Based on the findings from this analysis, it is evident that fraudulent activities within financial transactions can occur regardless of the individual's account balance, highlighting the pervasive nature of fraud in the economy. 

- Despite the various models employed in the fraud detection process, the tuned XgBoost model stands out for its exceptionally low recall value of 283, indicating its ability to effectively identify fraudulent transactions with minimal false negatives. 

- This performance underscores the significance of hyperparameter tuning in enhancing model accuracy and reliability for financial fraud detection.


