# Innovative Spotify Data Pipeline: Real-Time Music Analytics with AWS and Python

### Introduction
This project builds a Spotify ETL (Extract, Transform, Load) data pipeline using Python and AWS to collect music data from the Spotify API, process it, and load it into AWS for analysis. The pipeline is automated, scalable, and efficient, making it ideal for real-time analytics on music trends.

### Architecture
![Architecture Diagram.png](https://github.com/Saybik575/spotify-end-to-end-data-engineering-project/blob/main/Architecture%20Diagram.png)

### About Dataset/API
This project uses Spotify’s Web API to extract real-time music data, including songs, artists, albums, playlists, and track metadata - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a scalable cloud storage service for securely storing and retrieving any amount of data, commonly used for backups, archives, and data lakes.
   
2. **AWS Lambda:** AWS Lambda is a serverless compute service that runs code in response to events, automatically managing infrastructure and scaling as needed.

3. **Cloud Watch:** A monitoring service that collects and analyzes AWS metrics, logs, and events to track performance and operational health.

4. **Glue Crawler:** An AWS Glue crawler is an automated tool that discovers and catalogs data by scanning various data sources, extracting schema information, and storing metadata in the AWS Glue Data Catalog.

5. **Data Catalog:**A centralized repository in AWS Glue that stores metadata about data assets, enabling easy discovery and schema management.
   
6. **Amazon Athena:** Amazon Athena is a serverless query service that analyzes S3 data using SQL, eliminating the need for data loading or infrastructure management.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
1. The **Spotify Data Pipeline** follows an **ETL (Extract, Transform, Load)** process using AWS services for collecting, processing, storing, and analyzing music data.

2. **Data Extraction:** AWS Lambda retrieves songs, artists, albums, and playlist data from the Spotify API.

3. **Raw Data Storage:** Extracted JSON data is stored in an Amazon S3 bucket.

4. **Data Transformation:** AWS Lambda and Pandas clean and convert data into structured CSV format.

5. **Data Cataloging:** AWS Glue Crawlers scan and catalog the structured data.

6. **Processed Data Storage:** Transformed data is stored in a separate S3 bucket.

7. **Data Querying & Analysis:** Amazon Athena enables SQL-based querying without moving data.

8. **Metadata Management:** AWS Glue Data Catalog organizes and manages schema information.
