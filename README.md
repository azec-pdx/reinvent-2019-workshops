# Workshops Notes From AWS Re:Invent 2019
<hr>
##1. Workshop: How to migrate to Amazon DocumentDB 
([DAT338-R](https://www.portal.reinvent.awsevents.com/connect/search.ww?csrftkn=I12J-IEX7-06DV-RG4G-U9VM-7SGC-WNYX-5PQL#loadSearch-searchPhrase=DAT338&searchType=session&tc=0&sortBy=abbreviationSort&p=) | Monday 1PM)


* **Workshop description:** Amazon DocumentDB is a fast, reliable, fully managed MongoDB-compatible database service. If you’re using MongoDB today, how can you move your workloads to Amazon DocumentDB? What do you need to think about before, during, and after migration? Which tools and approaches should you use to ensure a successful migration? Join us to learn how to migrate MongoDB workloads to Amazon DocumentDB, and also get a demo of using AWS Database Migration Service (DMS).
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
