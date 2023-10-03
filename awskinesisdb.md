# Conduct research and compile a comprehensive research report on how to configure an Amazon Kinesis Data Firehose delivery stream to transmit real-time analytics data to an Amazon DynamoDB table.

## Introduction: -
This is a cloud-based service offered by Amazon Web Services (AWS) for streaming large amounts of real-time data. Amazon Kinesis can collect and process hundreds of terabytes of data per hour from sources such as website clickstreams, financial transactions, social media feeds, IT logs, and location-tracking events. It offers several capabilities.
Amazon Kinesis Data Firehose is a fully managed service for streaming large amounts of data in real-time. One of its use-cases includes collecting, processing, and analyzing real-time data, which can then be loaded to other AWS services like Amazon S3, Redshift, Elasticsearch, and DynamoDB. This report will guide you on setting up an Amazon Kinesis Data Firehose delivery stream to transmit real-time analytics data to an Amazon DynamoDB table.

- **Kinesis Data Streams**: Captures, processes, and stores data streams.
- **Kinesis Data Firehose**: Loads data streams to other AWS services in real-time.
- **Kinesis Data Analytics**: Provides real-time analytics on the streams.
- **Kinesis Video Streams**: Captures, processes, and stores video streams.

## Amazon Kinesis Data Firehose Overview: - 

Amazon Kinesis Data Firehose is a fully managed service for delivering real-time streaming data to services like Amazon Simple Storage Service (Amazon S3), Amazon Redshift, Amazon Elasticsearch Service (Amazon ES), Splunk, and any custom HTTP endpoint or HTTP endpoints owned by supported third-party service users, including Datadog, MongoDB, and New Relic. Kinesis Data Firehose is a component of the Kinesis streaming data platform, in conjunction with Kinesis Data Streams, Kinesis Video Streams, and Amazon Kinesis Data Analytics. With Kinesis Data Firehose, you do not get to write applications or manage resources. You configure your data producers to send data to Kinesis Data Firehose, and it automatically delivers the data to the destination that you simply specified. You can also configure Kinesis Data Firehose to rework your data before delivering it.


![image](https://github.com/aayush6162/AWS-task/assets/137821023/d00edf23-aa79-40bf-8d07-0eba8d92a45c)

The design includes six written steps and some sets of illustrations to show how to capture, transform, and send streaming data using Amazon Kinesis Data Firehose.

## Configuration Of Kinesis:- 
1) A S3 bucket should be created in the same area as the Kinesis data stream.

![image](https://github.com/aayush6162/AWS-task/assets/137821023/a9870388-1104-49dc-b055-0394c71bedb6)


2)Than Select Kinesis Data Firehose from the Amazon Kinesis Dashboard by going there. Establish a delivery stream.

![image](https://github.com/aayush6162/AWS-task/assets/137821023/040771db-c329-417d-bea5-b2eccbf05db3)


3) Choose source and destination
Choosing Direct PUT as a source.
Destination: Enter the name of your choice for the Amazon S3 Delivery stream.

![image](https://github.com/aayush6162/AWS-task/assets/137821023/74fbcb1d-7402-40d5-901b-7f3b54b0bcae)


Choose the S3 bucket you already created.

![image](https://github.com/aayush6162/AWS-task/assets/137821023/d0a7919f-7030-4238-a4ab-96bab67db187)


Create a delivery stream (It will take si=one minute)

![image](https://github.com/aayush6162/AWS-task/assets/137821023/8ea8ab4c-83bb-4389-a8ed-7650a7654043)



## TESTING FIREHOSE
Than to send demo data, expand the Test with demo data and then do so.

![image](https://github.com/aayush6162/AWS-task/assets/137821023/40a1ce83-2460-4bbc-a87f-e30deff79497)


Now open your bucket and verify the data.

![image](https://github.com/aayush6162/AWS-task/assets/137821023/a7a20f2a-ece9-4b73-a578-b8b855e31a56)


## Benefits by AWS Kinesis Data Firehose:- 
**Integrated with AWS services and service providers** : Amazon Kinesis Data Firehose is integrated with Amazon S3, Amazon Redshift, and Amazon Elasticsearch Service.

**Serverless data transformation** : It can easily convert raw streaming data from your data sources into formats like Apache Parquet and Apache ORC required by your destination data stores, without having to build your own data processing pipelines.

**Near real-time** : Users can load new data into their destinations within 60 seconds after the data is sent to the service. As a result, you can access new data sooner and react to business and operational events faster.

**Pay only for what you use** : With Amazon Kinesis Data Firehose, users need to pay only for the volume of data they transmit through the service, and if applicable, for data format conversion.

## Overview of Amazon DynamoDB

DynamoDB is a fast NoSQL Database that is managed by Amazon Web Services (AWS). It was developed by Amazon Web Services (AWB). DynamoDB is sometimes referred to as a key-value store, but it also has Streams, Global and Local Secondary Indexes, Multi-region and Multimaster replication with enterprise-grade security, and in-memory caching for large scale. Because it uses a pay-per-use basis and interfaces well with AWS Lambda and other AWS services, DynamoDB is an excellent choice for Serverless apps.

- Connect to AWS services to get more out of your data. Utilize the built-in tools to conduct analytics and extract.
- Able to accommodate peak throughputs of more than 20 million requests per second while handling more than 10 trillion requests per day.
- Protect your data with encryption at rest, automatic backup and restoration, and a service level agreement (SLA) that offers up to 99.999% uptime.
- Concentrate on innovation and reduce costs with a fully managed serverless database that scales up and down automatically to meet your needs.

## Configure Table in DynamoDB

1)DynamoDB Dashboard --> Create table
*Table name: give a name of your choice.
*Partition key: give a name and type related to your table.
*Create table and than 

2)Enter table data if you want to add an Attribute name
*Click Add a new attribute
*Select Type enter details

![image](https://github.com/aayush6162/AWS-task/assets/137821023/59eeb475-6256-4d22-bf32-87b251cf3496)



## Real-time Analytics and Data Streaming

Real Time data streaming and analytics is a process that mainly focuses on the data produced or consumed, or stored within a live environment. The scope of analytics can be from multiple sources. We can import or fetch the data, store it within a system, and execute data analysis algorithms.

Some real-life examples of streaming data include use cases in every industry, including real-time stock trades, up-to-the-minute retail inventory management, social media feeds, multiplayer games, and ride-sharing apps.

## Integration and Data Flow

Making many systems or applications operate as one cohesive unit is known as integration. It seeks to establish a unified setting that allows for seamless sharing of both processes and data.

## Types of Integratio

Integrating data with applications
Process Integration in Business



### Key Components 

**Connectors:** Interface elements that make it easier for systems to communicate with one another.

**Middleware:** Computer program that connects different programs and enables data sharing and communication.

**APIs (Application Programming Interfaces):** These guidelines outline how various software components should communicate with one another.

### Data Stream

The transfer of data from one place or application to another is referred to as data flow. It includes the whole data flow across a system.

### Basic Concepts

Source: The place or program from which data comes.
Data modification or conversion as it travels through the system is referred to as transformation.
Destination: The place or program where the data will ultimately live.


### Flow of Data

- Data entry into a system is called ingestion.
- Processing is the act of manipulating or changing data as it flows through a system.
- Keeping information on hand for reference or future use.
- Analyzing data to draw conclusions or patterns.
- Visualization: Making data comprehensible for analysis or decision-making.



## Best Practices:- 

To prevent throttling while partitioning a DynamoDB table, use a partition key that evenly distributes write activity among all of the partitions.
To accommodate the throughput offered by Kinesis Data Firehose, enable auto-scaling on your DynamoDB database.
To optimize the batch size that is written to DynamoDB, configure the buffering size and buffering interval.
To save failed records in S3, enable S3 backup in Kinesis Firehose under error handling.
**IAM Role** : Always adhere to the concept of least privilege. Give Kinesis Data Firehose only the rights it needs to access DynamoDB.


## Use Cases and Examples:

**Real-time Dashboard** : Real-time analytics data streaming to a DynamoDB database enables a live dashboard to display metrics like user activity, sales information, etc.

**IoT Data Collection** : Telemetry data from devices is streamed to Kinesis, where it is stored in DynamoDB for analysis and reporting.

**Logging & Monitoring** : Stream logs from applications to DynamoDB for real-time monitoring and alerting.


## Challenges and Considerations:

**Cost** : Both Kinesis and DynamoDB have expenses. Think about the volume of data being sent and stored.
**Write Capacity** : DynamoDB's write capacity should be able to handle the influx of data from Kinesis.
**Data Transformation** : AWS Lambda with Kinesis Firehose may be used if data needs to be modified before being put in DynamoDB.
**Data Retention** : Due to its high price, DynamoDB is rarely used for long-term storage. Take into account how long you need to keep the data.
**Item Size Limit** : The item size cap for DynamoDB is 400KB. Make sure that the records don't go beyond this.

## Conclusion: 
Real-time data ingestion and analytics are made possible by using Amazon Kinesis Data Firehose to send data to an Amazon DynamoDB table. Optimizing setups is crucial, though, as is being conscious of expenses and potential bottlenecks.


## References:

[Amazon Kinesis Data Firehose Developer Guide](https://docs.aws.amazon.com/firehose/latest/dev/what-is-this-service.html) <br>
[Amazon DynamoDB Developer Guide](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html) <br>
[Amazon S3](https://docs.aws.amazon.com/firehose/latest/dev/s3-prefixes.html) <br>
[Kinesis Firehose Integration with DynamoDB]

**Appendices:**

Appendix A: Sample AWS CloudFormation template for setting up the Kinesis to DynamoDB pipeline.
Appendix B: Cost optimization strategies for both Kinesis and DynamoDB.










