# Twitter Data ETL Pipeline Using Airflow

## Description
This is End-To-End Data Engineering Project using Airflow and Python. In this project, we will extract data using Twitter API, use python to transform data, deploy the code on Airflow/EC2 and save the final result on Amazon S3

## Dataset/API
This API contains information about Tweets, User, Retweets, Tweets created at - [Twitter API](https://developer.twitter.com/en/docs/twitter-api)

## Services Used
1. **Apache Airflow:** Apache Airflow is an open-source platform designed to programmatically author, schedule, and monitor workflows. It is particularly well-suited for orchestrating complex data workflows, automating tasks, and managing dependencies between different tasks or processes.
2. **Amazon EC2:** Amazon Elastic Compute Cloud (Amazon EC2) is a web service offered by Amazon Web Services (AWS) that provides resizable compute capacity in the cloud. It allows users to launch and manage virtual servers, known as EC2 instances, to run applications and workloads.
3. **S3(Simple Storage Service):** Amazon S3 is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on thr web. It is commonly used to store and distribute large media files data backups and static website files.

## Install Packages
```
sudo apt-get update
sudo apt install python3-pip
sudo pip install apache-airflow
sudo pip install pandas 
sudo pip install s3fs
sudo pip install tweepy
```

## Project Execution Flow
Extract data from Twitter API  -> Run Extract Code -> Transform Json data into proper DF structure -> Store Data in Local -> Create EC2 Instance -> Deploy Airflow on EC2 machine -> Write DAG onto ETL code -> Store it in S3 bucket
