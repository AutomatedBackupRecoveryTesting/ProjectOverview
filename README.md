# Project Overview
The objective of this case study is to (1) choose a client, then (2) evaluate the client's needs with the ultimate goal of scaling their IT infrastructure for rapid growth. 

### (1) The client: 

A Property Tech startup specializing in 3D virtual renderings of homes, serving real estate, home inspection, and home appraisal industries. 

### (2) The client's needs:
Based on an analysis of the company's current IT infrastructure and operations, an unmet need was discovered in the form of a dependable system that ensures data integrity and facilitates swift disaster recovery for the company's spatial data, which is crucial to their core operations.

With the specific needs of the company identified, **the goal of this project is to assess and validate the effectiveness of the client’s current second-level recovery system. The proposed solution is an automated AWS framework that leverages AWS CloudFormation for infrastructure as code, AWS Lambda for serverless compute, and AWS Backup for data backup and recovery. The Lambda function, written in Python, employs the Boto3 library for AWS SDK integration, and it utilizes the AWS Simple Notification Service (SNS) for event-driven notifications.**

# System Selection
As a result of the fact that most of the client’s operations are hosted on AWS, the proposed solution should also be hosted on AWS. Furthermore, a DynamoDB table must be created for the purposes of backup and restore testing. AWS Backup will handle the brunt of the backup and restore operations, and in order to automate these operations, AWS Lambda will need to be employed. SNS backup should also be incorporated into the framework so that the user can receive updates about the status of Backup and Restore jobs once they are completed. 

The minimum viable product for this project will be a working AWS CloudFormation template which can be directly imported into the AWS environment for testing purposes. For the sake of keeping things as simple as possible in the creation of this framework, the validation criteria for AWS Lambda to employ when it attempts to validate the restore of the AWS Backup job will be limited to validating that the status of the restored DynamoDB table returns as “ACTIVE.” A stretch goal for this project will be determining other criteria that could be employed to validate the client’s databases in real-life disaster scenarios. Ultimately, the proposed solution may serve as a framework for the client to further “hand-fit” to their exact needs in validating their daily DB backups. 

# About the Project Owner 
This project was scoped, developed, and written by Elodie Rebesque. 

[Github profile](https://github.com/ElodieReb)

[LinkedIn profile](https://www.linkedin.com/in/elodierebsq/)

