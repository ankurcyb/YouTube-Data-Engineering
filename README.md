# YouTube-Data-Engineering
Data Engineering and Analytics

This projects aims to create an analysis of YouTube trending videos based on the trending metrics via AWS cloud services to ingest, transform, analysis, and to report findings. This whole project is based on Amazon Web Services cloud using it's various services.


# Project Aim

1. Data Ingestion - Building a pipeline to extract raw data of various formats into the AWS S3 which is our repository.
2. AWS S3 -  This is the repository where we store data from different sources of various formats.
3. ETL - We are transforming the raw data into usable format.
4. Analysis - Analyzing the data to create insights about the trending metric.
5. Reporting - A dashboard where we can represent our finding through analysis.


#Dataset Used

This Keggle dataset includes data on daily trending YouTube videos which includes data for the US, GB, DE, CA, FR, RU, MX, KR, JP and IN regions (USA, Great Britain, Germany, Canada, France, Russia, Mexico, South Korea, Japan and India respectively) with upto 200 listed trending video per day.
Each region dataset includes:
- Video title, channel title, publish time, tags, views, likes and dislikes, descrption, and comment count.
- Each regions have seperate file (CSV format.
- Data includes category_id field which acts as primary key between regions which is stored in JSON format.

  Link to Dataset - https://www.kaggle.com/datasets/datasnaek/youtube-new
