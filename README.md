# Workshops Notes From AWS Re:Invent 2019
<hr>
##1. Workshop: How to migrate to Amazon DocumentDB
([DAT338-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=95826&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Monday 1:00 PM)


* **Workshop Description:** Amazon DocumentDB is a fast, reliable, fully managed MongoDB-compatible database service. If you’re using MongoDB today, how can you move your workloads to Amazon DocumentDB? What do you need to think about before, during, and after migration? Which tools and approaches should you use to ensure a successful migration? Join us to learn how to migrate MongoDB workloads to Amazon DocumentDB, and also get a demo of using AWS Database Migration Service (DMS).
* **Workshop Hands On Materials:** [Here](http://d310sl6n0pru7e.cloudfront.net/verifydms_4.html)
* **Workshop Notes:**
  - Pitfalls for DMS:
    - the DMS for mongo engine doesn't support indexes migration (but it can do full&ongoing/onlin migration of data)
    - there is set of tools for DocumentDB that were designed to help out validation of manual indexes migration.
    - the very workshop example shows that currently DocumentDB doesn't support some MongoDB indexes (e.g. text and 2dsphere)
  - Pitfalls for DocumentDB:
    - Currently only supports 3.6 MongoDB
    - Users managed through IAM
  - Pros for DocumentDB:
    - Different architecture than MongoDB replication - HA and Resilliency enabled through “cluster volume” that spans few AZs.
    - All writes go to master/PRIMARY , and replication of the 3 copies of the data done through storage abstractions (so no real replication as with MongoDB)
  - Resources:
    - https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html
    - https://docs.aws.amazon.com/dms/latest/userguide/target.docdb.html


##2. Workshop: Build a single query to analyze data across Amazon Redshift & Amazon S3
([ANT404-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=96411&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Monday 4:00 PM)

* **Workshop Description:** Amazon Redshift offers a common query interface against data stored in fast, local storage (Amazon Redshift) and data stored in high-capacity, inexpensive storage (Amazon S3). This workshop covers the basics of this tiered storage model and outlines design patterns that you can leverage to get the most from large volumes of data. Learn how to build out your own Amazon Redshift cluster with multiple data sets to illustrate the trade-offs between the storage systems. Learn how to distribute your data and design your DDL to deliver the best data warehouse for your business.
* **Workshop Hands On Materials:** [Here](https://ant404.notebook.us-east-1.sagemaker.aws/tree)


##3. Workshop: Building a scalable serverless application with AWS CDK
([DOP306-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=96826&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Monday 7:00 PM)

* **Workshop Description:** Dive into AWS and build a web application with the AWS Mythical Mysfits tutorial. In this workshop, you build a serverless application using AWS Lambda, Amazon API Gateway, and the AWS Cloud Development Kit (AWS CDK). Through the tutorial, you get hands-on experience using AWS CDK to model and provision a serverless distributed application infrastructure, you connect your application to a backend database, and you capture and analyze data on user behavior. Other AWS services that are utilized include Amazon Kinesis Data Firehose and Amazon DynamoDB.
* **Workshop Hands On Materials (Markdown):** [Here](https://s3.amazonaws.com/ee-assets-prod-us-east-1/modules/882416f812d947c09867fae6aa4a6502/v1/readme.md)
