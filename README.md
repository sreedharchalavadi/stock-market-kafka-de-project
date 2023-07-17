# Stock Market Kafka Real Time Data Engineering Project

### Overview 
In this project, I have executed an End-To-End Data Engineering Project on Real-Time Stock Market Data using Kafka.
I have used different technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

### Architecture
![Architecture diagram](https://github.com/sreedharchalavadi/stock-market-kafka-de-project/blob/main/Architecture.jpg)

### Technology Used
- Programming Language - Python
- Amazon Web Service (AWS)
- Apache Kafka

### Services used

1. **AWS S3 (Simple Storage Service) :** Its an object storage service that provides manufacturing scalability, data availability, security, and performance. Its a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web.It is commonly used to store and distribute large media files, data backups and static website files.
2. **AWS IAM :** This is nothing but identity and access management which enables us to manage access to AWS services and resources securely.
3. **AWS Glue :** A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
4. **AWS Glue Crawler :** AWS Glue Crawler is a fully managed service that automatically crawls the data sources, identifies data formats and infers schemas to create an AWS Glue Data Catalog.
5. **AWS Glue Data Catalog :** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. We can use the Glue Data Catalog with other AWS services, such as Athena
6. **AWS Athena :** Athena is an interactive query service that makes it easy to analyze data in amazon s3 using standard SQL. We can use Athena to analyze data in Glue Data catalog or in other s3 buckets

### Dataset Used
This contains the information about the stockmarket dataset used in this project.
[Stock Market Dataset](https://github.com/sreedharchalavadi/stock-market-kafka-de-project/blob/main/indexProcessed.csv)

### Project Execution Flow
Loaded the indexProcessed.csv into python dataframe --> Kafka Producer keeps on generating the sample rows from this dataframe with the latency of 2s through topic : sreetopic1  --> Kafka Consumer consumes these messages using the same topic : sreetopic1 --> Kafka consumer also writes the data into s3 in json format with increasing count --> Glue crawler creates the data catalogs on s3 data --> Query this stock market data using Athena
