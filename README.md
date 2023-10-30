# Project Overview
The objective of this case study is to (1) choose a client, then (2) evaluate the client's needs with the ultimate goal of scaling their IT infrastructure for rapid growth. 

### (1) The client: 

A Property Tech startup specializing in 3D virtual renderings of homes, serving real estate, home inspection, and home appraisal industries. 

### (2) The client's needs:
Based on an analysis of the company's current IT infrastructure and operations, an unmet need was discovered in the form of a dependable system that ensures data integrity and facilitates swift disaster recovery for the company's spatial data, which is crucial to their core operations.

With the specific needs of the company identified, **the goal of this project is to assess and validate the effectiveness of the client’s current second-level recovery system. The proposed solution is an automated AWS framework that leverages AWS CloudFormation for infrastructure as code, AWS Lambda for serverless compute, and AWS Backup for data backup and recovery. The Lambda function, written in Python, employs the Boto3 library for AWS SDK integration, and it utilizes the AWS Simple Notification Service (SNS) for event-driven notifications.**

For a more detailed explanation of the AWS framework, please refer to the following system diagram:
![Proposed Solution System Diagram](https://github.com/AutomatedBackupRecoveryTesting/ProjectOverview/blob/main/ABRT_Project_System_Diagram.png).

# System Selection
As a result of the fact that most of the client’s operations are hosted on AWS, the proposed solution should also be hosted on AWS. Furthermore, a DynamoDB table must be created for the purposes of backup and restore testing. AWS Backup will handle the brunt of the backup and restore operations, and in order to automate these operations, AWS Lambda will need to be employed. SNS backup should also be incorporated into the framework so that the user can receive updates about the status of Backup and Restore jobs once they are completed. 

The minimum viable product for this project will be a working AWS CloudFormation template which can be directly imported into the AWS environment for testing purposes. For the sake of keeping things as simple as possible in the creation of this framework, the validation criteria for AWS Lambda to employ when it attempts to validate the restore of the AWS Backup job will be limited to validating that the status of the restored DynamoDB table returns as “ACTIVE.” A stretch goal for this project will be determining other criteria that could be employed to validate the client’s databases in real-life disaster scenarios. Ultimately, the proposed solution may serve as a framework for the client to further “hand-fit” to their exact needs in validating their daily DB backups. 

To manage all tasks related to the design and creation of the AWS framework, as well as any other tasks related to the creation and editing of relevant documentation for the project, [GitHub Projects](https://github.com/orgs/AutomatedBackupRecoveryTesting/projects/1/views/1) will be used. 

# Project Deliverables
1. [Disaster Recovery SOP](https://docs.google.com/document/d/134BKGJC0GGLEFZaAlhS-TpnfAJQt9G_y8yzPOLMjgMo/edit?usp=sharing) - Summarizes the client's existing second-level recovery procedure
2. AWS CloudFormation Template Code - See [CloudFormationTemplate Repo](https://github.com/AutomatedBackupRecoveryTesting/CloudFormationTemplate) 
3. AWS Lambda Function Code - See [LambdaFunction Repo](https://github.com/AutomatedBackupRecoveryTesting/LambdaFunction)
4. [Project Presentation Slides](https://docs.google.com/presentation/d/1NBKmaXIWkKxM6ZueqAklBSy1j14hkImGL3CYffFkavk/edit?usp=sharing) - Meme included! :)
5. [Presentation Recording](https://zoom.us/rec/share/m7TutNfN4g_ICvy5SYJUKvRWSxR__aeKGW7VYx7n1NWm89PPicVK24OWslJGKfdD.9cQO-6o_5XjfPaFB)

# About the Project Owner 
This project was scoped, developed, and written by Elodie Rebesque. 

[Github profile](https://github.com/ElodieReb)

[LinkedIn profile](https://www.linkedin.com/in/elodierebsq/)

Elodie graduated from Washington University in St. Louis this past May with a degree in Mechanical Engineering. Originally from Palo Alto, CA, she claims to have grown up in a "tech incubator" which ultimately influenced her decision to pursue a career in Cybersecurity. Well, that, and the prospect of a never-ending supply of challenging problems to solve that the industry provides. Her ultimate goal is to become a Cybersecurity Product Manager, as her love for problem-solving can only be matched by her love of building camaraderie among technical and non-technical parties, leading others, and being part of a diverse, supportive team. In June, Elodie began her Cybersecurity journey as an ops student at Code Fellows, and as an Operations Strategist at InsideMaps Inc., the "client" of her case study.

<b> "The combination of learning new material both inside the virtual classroom and outside of it," </b> she says, <b> "has been a real treat - and I’m excited to show you all what I have come up with in my first big project!" </b>
