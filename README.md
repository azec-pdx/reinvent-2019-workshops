# Workshops Notes From AWS Re:Invent 2019
<hr>

## 1. Workshop: How to migrate to Amazon DocumentDB
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


## 2. Workshop: Build a single query to analyze data across Amazon Redshift & Amazon S3
([ANT404-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=96411&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Monday 4:00 PM)

* **Workshop Description:** Amazon Redshift offers a common query interface against data stored in fast, local storage (Amazon Redshift) and data stored in high-capacity, inexpensive storage (Amazon S3). This workshop covers the basics of this tiered storage model and outlines design patterns that you can leverage to get the most from large volumes of data. Learn how to build out your own Amazon Redshift cluster with multiple data sets to illustrate the trade-offs between the storage systems. Learn how to distribute your data and design your DDL to deliver the best data warehouse for your business.
* **Workshop Hands On Materials:** [Here](https://ant404.notebook.us-east-1.sagemaker.aws/tree)


## 3. Workshop: Building a scalable serverless application with AWS CDK
([DOP306-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=96826&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Monday 7:00 PM)

* **Workshop Description:** Dive into AWS and build a web application with the AWS Mythical Mysfits tutorial. In this workshop, you build a serverless application using AWS Lambda, Amazon API Gateway, and the AWS Cloud Development Kit (AWS CDK). Through the tutorial, you get hands-on experience using AWS CDK to model and provision a serverless distributed application infrastructure, you connect your application to a backend database, and you capture and analyze data on user behavior. Other AWS services that are utilized include Amazon Kinesis Data Firehose and Amazon DynamoDB.
* **Workshop Hands On Materials (Markdown):** [Here](https://s3.amazonaws.com/ee-assets-prod-us-east-1/modules/882416f812d947c09867fae6aa4a6502/v1/readme.md)


## 4. Workshop: Build full-stack apps in 15 minutes or less with AWS databases
([DAT330-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=95815&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Tuesday 7:00 PM)

* **Workshop Description:** With the AWS full-stack template, you can get a web application up and running in just a few clicks and customize it to create any application from a travel-booking tool to an enterprise SaaS application. Our AWS CloudFormation template automatically builds all of the infrastructure you need, including databases, authentication, CRUD APIs, and monitoring. In this workshop, you spin up both applications and make them your own. You also learn about the architectural decisions we made and how you can get your full-stack application up and running in minutes.
* **Workshop Hands On Materials:** [Here](https://github.com/awslabs/aws-full-stack-template/tree/master/workshop)


## 5. Workshop: AWS Identity: Using Amazon Cognito for serverless consumer apps
([SEC403-R1](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=96389&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Wednesday 9:15 AM)

* **Workshop Description:** In this workshop, you learn how to build a serverless customer-facing microservices application demonstrating end-to-end authentication and authorization using Amazon Cognito, Amazon API Gateway, AWS Lambda, and all things AWS Identity and Access Management (IAM). You have the opportunity to build an end-to-end functional app with a secure identity provider showcasing user authentication patterns. To participate, you need a laptop, an active AWS account, an AWS IAM administrator, and familiarity with core AWS services.
* **Workshop Hands On Materials:**
  - [Hands On Tutorial](https://serverless-idm.awssecworkshops.com/)
  - [Slides](https://serverless-idm.awssecworkshops.com/images/SEC403.pdf)


## 6. Workshop: Build and ship full-stack serverless apps with AWS Amplify
([MOB303-R](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=96313&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Wednesday 11:30 AM)

* **Workshop Description:** Learn how to use AWS AppSync and the AWS Amplify Framework to code, build, and deploy engaging full-stack serverless apps in React. We showcase how AWS AppSync provides data to your apps and lets you create robust, scalable GraphQL APIs to securely access and manipulate data from multiple sources, with both online and offline capabilities. See how the Amplify Framework simplifies building and connecting to a serverless backend with a powerful toolchain and resourceful library. Finally, learn how to deploy your app to the cloud using the AWS Amplify Console, which provides built-in hosting and out-of-the-box CI/CD capabilities. Please bring your own laptop.
* **Workshop Hands On Materials:**
  - [Hands On Tutorial](https://github.com/aws-samples/aws-reinvent-2019-mobile-workshops/tree/master/MOB303)
  - [Community](https://amplify.aws)


## 7. Workshop: Advanced design patterns for Amazon DynamoDB
([DAT334-R1](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=95818&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Wednesday 02:30 PM)

* **Workshop Description:** Join us for a practical hands-on workshop on using Amazon DynamoDB. This session is designed for developers, engineers, and database administrators who are involved in designing and maintaining DynamoDB applications. We begin with a walk-through of proven NoSQL design patterns for at-scale applications. Next, we use step-by-step instructions to apply lessons learned to design DynamoDB tables and indexes that are optimized for performance and cost. Expect to leave this session with the knowledge needed to build and monitor DynamoDB applications that can grow to any size and scale.
* **Workshop Hands On Materials:** [Here](https://ee-assets-prod-us-east-1.s3.amazonaws.com/modules/5c47b474e61a4b93a573f3187f6cfc0f/v2/guide/setup.html)


## 8. Workshop: Building applications on Amazon QLDB
([DAT352](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=97087&csrftkn=FDDX-2514-BOYY-RJBZ-CFEJ-26P0-PC90-EWK5) | Thursday 12:15 PM)

* **Workshop Description:** In this workshop, you build and review a sample Java application leveraging Amazon QLDB. You also learn how to use the different Amazon QLDB APIs and features, including learning how to write, query, and verify documents. Finally, we cover best practices for using this service. For this session, experience with Java is recommended but not required.
* **Workshop Hands On Materials:** [Here](https://amazon-qldb-assets.s3.amazonaws.com/setup-scripts/dmv-lab-guide.pdf)


## 9. Workshop: Get started with Open Distro for Elasticsearch
([OPN302-R1](https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=95519&csrftkn=UJXZ-T53K-5MMO-FS2M-3BH6-Y0A4-4FFO-4A8O) | Thursday 3:15 PM)

* **Workshop Description:** If you’re running any kind of software, in any capacity, you’re generating logs. In all likelihood, you have more logs than you could read through in several lifetimes. Buried among the noise, your logs contain important information that can help you tune and monitor your application, and find and fix security issues. In this workshop, you set up and configure Open Distro for Elasticsearch and its key plugins, including alerting, performance analyzer, security, and SQL. We will also walk through how you can manage your Elasticsearch cluster by setting up alerts, tracking cluster health metrics, and querying your data.
* **Workshop Hands On Materials:**
  - [Hands On Tutorial](https://reinvent.aesworkshops.com/opn302/)
  - [Community](https://github.com/opendistro-for-elasticsearch/community/tree/master/cloudformation-deployment)
