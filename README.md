# Twitter Data ETL Pipeline: Orchestrating with Airflow and AWS

## Project Overview
This project demonstrates an end-to-end data engineering solution using **Apache Airflow** and **Python**. It focuses on extracting data from the **Twitter API**, transforming it using Python, and deploying the workflow on **Amazon EC2** with the final output stored in **Amazon S3**. The project showcases how to effectively orchestrate and automate data pipelines for real-time data extraction and storage.

## API and Dataset
The project extracts data from Twitter, including information about:
- Tweets
- Users
- Retweets
- Timestamps

**Twitter API**:  
For more details, visit the official documentation: [Twitter API](https://developer.twitter.com/en/docs/twitter-api)

## Services Used

1. **Apache Airflow**:  
   Airflow is used to orchestrate and automate the data pipeline. It allows for scheduling and monitoring workflows, making it ideal for managing ETL processes.

2. **Amazon EC2**:  
   EC2 provides scalable compute capacity for deploying Airflow and running the Python scripts. This cloud infrastructure ensures the pipeline can handle large-scale data extraction and processing.

3. **Amazon S3**:  
   S3 is used for storing the final transformed data. This highly scalable object storage service is ideal for saving data backups and static files for future analysis or distribution.

---

## Installation

To set up the project, follow these steps to install the necessary dependencies:

```bash
sudo apt-get update
sudo apt install python3-pip
sudo pip install apache-airflow
sudo pip install pandas 
sudo pip install s3fs
sudo pip install tweepy
```

---

## Project Execution Flow

1. **Extract Data from Twitter API**:  
   Using the **Tweepy** library, the project connects to the Twitter API and extracts relevant data (Tweets, users, retweets, etc.).

2. **Transform Data**:  
   The raw JSON data from the API is transformed into a structured DataFrame using **Pandas**. This ensures the data is cleaned and ready for storage.

3. **Local Storage**:  
   The transformed data is temporarily stored in a local directory before being uploaded to the cloud.

4. **Create EC2 Instance**:  
   An **Amazon EC2** instance is launched to host the Airflow environment, where the entire pipeline is deployed and managed.

5. **Airflow DAG Setup**:  
   A Directed Acyclic Graph (DAG) is written in Airflow to orchestrate the ETL process, automating the execution of extraction, transformation, and loading tasks.

6. **Store in S3**:  
   Finally, the cleaned and structured data is stored in an **S3 bucket** for long-term storage and future analysis.

---

## Future Enhancements
- **Real-time Data Streaming**: Integrate **AWS Kinesis** for real-time data streaming and processing.
- **Data Visualization**: Use **Amazon QuickSight** or **Tableau** to create dashboards from the data stored in S3.
- **Error Handling & Logging**: Improve pipeline resilience by adding better error-handling mechanisms and detailed logging in Airflow.

---

## Conclusion
This project highlights the use of Apache Airflow for orchestrating an ETL pipeline, leveraging **Amazon EC2** for computation and **S3** for storage. It demonstrates a scalable approach to collecting and managing Twitter data for analysis and reporting.
