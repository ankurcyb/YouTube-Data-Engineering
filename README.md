# YouTube-Data-Engineering
Data Engineering and Analytics

This projects aims to create an analysis of YouTube trending videos based on the trending metrics via AWS cloud services to ingest, transform, analysis, and to report findings. This whole project is based on Amazon Web Services cloud using it's various services.


# Project Aim

1. Data Ingestion - Building a pipeline to extract raw data of various formats into the AWS S3 which is our repository.
2. AWS S3 -  This is the repository where we store data from different sources of various formats.
3. ETL - We are transforming the raw data into usable format.
4. Analysis - Analyzing the data to create insights about the trending metric.
5. Reporting - A dashboard where we can represent our finding through analysis.


# Dataset Used

This Keggle dataset includes data on daily trending YouTube videos which includes data for the US, GB, DE, CA, FR, RU, MX, KR, JP and IN regions (USA, Great Britain, Germany, Canada, France, Russia, Mexico, South Korea, Japan and India respectively) with upto 200 listed trending video per day.
Each region dataset includes:
- Video title, channel title, publish time, tags, views, likes and dislikes, descrption, and comment count.
- Each regions have seperate file (CSV format.
- Data includes category_id field which acts as primary key between regions which is stored in JSON format.

  Link to Dataset - https://www.kaggle.com/datasets/datasnaek/youtube-new

# AWS Services Used

1. AWS S3:  (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.
2. AWS IAM: Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can centrally manage permissions that control which AWS resources users can access. 
3. AWS Glue: It is a serverless data integration service that makes it easy for analytics users to discover, prepare, move, and integrate data from multiple sources. You can use it for analytics, machine learning, and application development. It also includes additional productivity and data ops tooling for authoring, running jobs, and implementing business workflows.
4. AWS Lambda: AWS Lambda is a serverless, event-driven compute service that lets you run code for virtually any type of application or backend service without provisioning or managing servers
5. Amazon Athena: Amazon Athena is an interactive query service that makes it simple to analyze data directly in Amazon S3 using standard SQL.
6. Amazon Quicksight: Amazon QuickSight is a very fast, easy-to-use, cloud-powered business analytics service that makes it easy for all employees within an organization to build visualizations, perform ad-hoc analysis, and quickly get business insights from their data, anytime, on any device.


# Process

1. First step involved downloading data from YouTube data set from keggle to our local machine. This dataset has data of trending YouTube videos of different regions and has different formats. 
Then we export the data from our local machine to the AWS S3 bucket that we created.
![image](https://github.com/ankurcyb/YouTube-Data-Engineering/assets/141453942/f22806a3-5a6c-44a4-93fd-de65d9a7f212)
![image](https://github.com/ankurcyb/YouTube-Data-Engineering/assets/141453942/eda20eec-acbc-4386-947d-7163b588bce8)


2. The second step involved creating AWS Glue as a central repository of metadata of all data sets that we exported from Keggle to understand the dataset better.
By running crawler in the dataset that we exported in the S3 bucket, we are able to understand it better by determining the schema of the raw data. The schema is replicated in the Glue Data catalogue.
![image](https://github.com/ankurcyb/YouTube-Data-Engineering/assets/141453942/9365b5a1-2de5-48f7-bf9d-db8ea6adbdc6)
Crawler
![image](https://github.com/ankurcyb/YouTube-Data-Engineering/assets/141453942/c491a1dc-e1f5-44a3-a9e5-b2f21ef299b4)
Schema


3. The next step is create AWS Lambda to run ETL job on our raw YouTube data to convert into Parquet from .json because AWS catalogue doesn't know what type of data that we want to work on. So, we will run an ETL job on the raw data and we will run the Crawler on the cleansed data.
![image](https://github.com/ankurcyb/YouTube-Data-Engineering/assets/141453942/010319a9-097b-45eb-8fff-e69860181c69)
Lambda Python function
![image](https://github.com/ankurcyb/YouTube-Data-Engineering/assets/141453942/48bf9d0f-3ecf-4ed8-80ff-af2afc8c3e2f)
Execution


4. The next step is to create a Dashboard using AWS quicksight to answer the questions related to YouTube data trending metric.




 
