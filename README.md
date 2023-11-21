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




 
