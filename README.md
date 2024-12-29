Your organization utilizes on-premises virtual machines within VMware vCenter and is looking to transition them to AWS using the AWS Application Migration Service. In order to facilitate this migration, you aim to employ the Application Discovery Service Agentless Collector to gather data on the current on-premises setup. What prerequisites need to be met for the successful utilization of the Agentless Collector to discover the VMware VMs? Select two answers from the options provided.
A)	
Make sure the security group of the Application Discovery Service allows the IP range of the on-premises network on port 443.
B)	
Login to the VMs and download the agent installation script (i.e. curl -o ./aws-discovery-agent.tar.gz https://s3-us-west-2.amazonaws.com/aws-discovery-agent.us-west-2/linux/latest/aws-discovery-agent.tar.gz).
C)	
Update the on-premises firewall settings to allow outbound access to the AWS domains that Agentless Collector requires (i.e. arsenal-discovery.us-west-2.amazonaws.com).
D)	
Create an IAM user with the predefined IAM policy "AWSApplicationDiscoveryAgentlessCollectorAccess" for the Agentless Collector to authenticate with AWS when forwarding the data.
E)	
Create an IAM role with the predefined IAM policy "AWSApplicationDiscoveryAgentAccess" and attach the role to the Agentless Collector.
A, D
---------
A company operates its essential portal within an on-premises data center utilizing Docker containers and a PostgreSQL database that is 40 TB in size. They aim to transition their current portal to AWS to improve user experience while reducing the demands of infrastructure management. What migration methods would be most suitable for them? Select two answers from the options provided.
A)	
They should run the PostgreSQL on top of EC2 Nitro Based system for better Database Performance
B)	
They should choose EC2 to deploy the containers on ECS and move the 40TB data using snowball on AWS
C)	
They should choose Fargate to deploy the containers on ECS and move the 40TB data using snowball on AWS
D)	
They should choose EC2 to deploy the containers on ECS and move the 40 TB data using 1Gbps Direct Connection Connection
E)	
They should use the RDS Aurora PostgreSQL Database in AWS
C, E
-------
As an AWS solutions architect overseeing a migration project from local servers to AWS, you have successfully configured AWS Server Migration Service to replicate numerous VMware virtual machines to EC2 AMI. SMS has been instrumental in generating CloudFormation templates for application migration. In addition to this, you have personally crafted multiple CloudFormation templates for the creation of AWS resources such as EC2 instances. Now, you are looking for a centralized service to manage these resources created by CloudFormation templates, allowing users to easily select and deploy specific products. This service should seamlessly integrate with IAM for access control. What would be the most optimal approach for you to adopt?
A)	
Create groups of CloudFormation templates in AWS Resource Groups. Assign related IAM permissions based on the group ARN
B)	
Manage resources in AWS Config via tags. Create resources and provide access control based on tags
C)	
Configure and manage all CloudFormation templates in AWS Resource Access Manager. Assign different permissions to IAM users or roles
D)	
Create portfolio and products in AWS Service Catalog. Use IAM permissions to grant users access to the portfolio
D
--------
You are tasked with establishing network connectivity between your current data centers and AWS. It is essential for the EC2 instances of your application to connect with the existing backend resources housed in your data center. Initially, the network traffic between AWS and your data centers will be minimal, but it is expected to increase to tens of gigabytes per second over the next few months. The timely launch of your application is crucial for its success. Which design options will best enable you to achieve these goals?
A)	
Quickly submit a Direct Connect request to provision a 1 Gbps cross-connect between your data center and VPC, then increase the number or size of your Direct Connect connections as needed
B)	
Quickly create an internal ELB for your backend applications, submit a Direct Connect request to provision a 1 Gbps cross-connect between your data center and VPC, then increase the number or size of your Direct Connect connections as needed
C)	
Allocate EIPs and an Internet Gateway for your VPC instances to use for quick, temporary access to your backend applications, then provision a VPN connection between a VPC and existing on-premises equipment
D)	
Provision a VPN connection between a VPC and existing on-premises equipment, submit a Direct Connect partner request to provision cross-connects between your data center and the Direct Connect location, then cut over from the VPN connection one or more Direct Connect connections as needed
D
-------
The company is seeking to relieve its teams from time-consuming database tasks by migrating their on-premises MariaDB database to AWS. They require built-in security, continuous backups, serverless compute, multiple read replicas, automated multi-Region replication, cost-effectiveness, and integrations with other AWS services. As a solution architect, you need to ensure a quick and secure migration to AWS while keeping the source database fully operational and minimizing downtime for applications relying on the database. What architectural changes would you recommend to meet these requirements?
A)	
Provision Amazon Aurora Serverless PostgreSQL as target DB instance in AWS. Provision Database Migration Service (DMS) replication instance and create DMS endpoints. Create DMS task, migrate data from the source database as on-premises MariaDB and perform validation.
B)	
Provision Amazon Aurora Mysql as the target DB instance in AWS. Provision Database Migration Service (DMS) replication instance and create DMS endpoints. Create DMS task, migrate data from the source database as on-premises MariaDB, and perform validation.
C)	
Provision DynamoDB as target DB instance in AWS. Provision Database Migration Service (DMS) replication instance and create DMS endpoints. Create DMS task, migrate data from the source database as on-premises MariaDB, and perform validation.
D)	
Provision Amazon Aurora Serverless MySQL as target DB instance in AWS. Provision Database Migration Service (DMS) replication instance and create DMS endpoints. Create DMS task, migrate data from source database as on-premises MariaDB and perform validation.
D
-----
Your organization intends to migrate an existing portal to AWS, which is currently hosted on-premises. This portal, developed using Java and MySQL 5.6, has been in operation for five years. The goal is to containerize the application and deploy it in a highly available AWS environment. Additionally, a serverless compute engine for containers is required to eliminate the need for server provisioning and management. What would be the most appropriate method to achieve this?
A)	
Containerize the Java based application, store Container image in ECR and deploy it in ECS with AWS Fargate Launch Type. Leverage Amazon Aurora MySQL for the database
B)	
Deploy the Application on Amazon ECS with EC2 Launch Type and leverage Amazon RDS MySQL for the database
C)	
Deploy the Application on Amazon EC2 and leverage the Amazon Aurora MySQL for the database
D)	
Containerize the Java based application, store Container image in Docker Hub and deploy it in ECS with EC2 Launch Type. Leverage Amazon Aurora MySQL for the database
A
------
As an AWS Solutions Architect, you are tasked with redesigning the company's internal dockerized Python web application and PostgreSQL database to utilize new AWS services without relying on EC2 instances. The plan is to set up an RDS Aurora database to host the PostgreSQL database and to ensure that the Python application is fast, simple, and cost-effective to deploy without the use of load balancers for traffic distribution. Additionally, the application should be able to auto-scale based on the maximum number of concurrent requests configured by users. How would you approach designing a solution to easily host the Python application?
A)	
Store the Docker images in ECR and host the application in AWS Elastic Kubernetes Service (EKS). Configure the max concurrency in the auto-scaling settings of EKS clusters
B)	
Store the Docker images in ECR and deploy the application using a new AWS Lambda function. Configure the max concurrency in the auto-scaling settings of the Lambda function
C)	
Store the Docker images in ECR and host the application in a new AWS App Runner service. Configure the max concurrency in the auto-scaling settings of the App Runner service
D)	
Store the Docker images in ECR and host the application in AWS ECS Fargate. Configure the max concurrency in the auto-scaling settings of ECS task definitions
D
-------
A large corporation offers a service designed to handle extensive clickstream data sets, typically generated by holiday shopping surges on retail websites or significant spikes in traffic on media and social networking platforms. Analyzing these clickstream datasets within their on-premise infrastructure is increasingly challenging. As the volume of sample data continues to expand, the number of applications capable of delivering timely insights diminishes. Currently, the service operates on a Hadoop cluster utilizing Cascading. What is the most effective strategy for migrating these applications to AWS?
A)	
Put the source data to a Kinesis stream and migrate the processing service to an AWS EMR cluster with Cascading. Enable EMR to read and query data from Kinesis streams directly. Write the output to Redshift
B)	
Put the source data to S3 and migrate the processing service to an AWS EMR Hadoop cluster with Cascading. Enable EMR to read and query data from S3 buckets directly. Write the output to the RDS database
C)	
Put the source data to a Kinesis stream and migrate the processing service to AWS lambda to utilize its scaling feature. Enable lambda to read and query data from the Kinesis stream directly. Write the output to the RDS database
D)	
Put the source data to an S3 bucket and migrate the processing service to AWS EC2 with auto-scaling. Ensure that the auto-scaling configuration has a proper maximum and minimum number of instances. Monitor the performance in the Cloudwatch dashboard. Write the output to the DynamoDB table for downstream to process
A
-------
A Big Data company stores all its raw data in Amazon S3. Over a few days in every quarter of the calendar year, the petabyte-scale of data needs to be processed to the analytical platform. This processed data gets analyzed during Company's Quarterly Business Review (QBR) meeting and again in the annual review meeting by the year-end. As part of this solution, they plan to run their S3 data through 10 nodes of the Amazon EMR cluster hosted on c5.xlarge EC2 instances and finally load the data to Amazon Redshift. You are a Solution Architect at the company, and the CTO tasked you to optimize the cost of the overall solution. Which one of the following will be your pick?
A)	
Store the raw data in S3 Standard Infrequent Access, host the EMR cluster on EC2 Reserved Instances for EMR and Reserved instances for Redshift.
B)	
Store the raw data in S3 Standard Infrequent Access, host the EMR cluster on EC2 On-Demand Instances and Reserved instance for Redshift.
C)	
Use S3 Intelligent Tier to store the raw data, host the EMR cluster on EC2 On-Demand Instances and Reserved instances for Redshift.
D)	
Store the raw data in S3 Standard, host the EMR cluster on EC2 Spot Instances and Reserved instances for Redshift.
---------
The customer aims to unify their various log streams, including access logs, application logs, and security logs, into a single system. After consolidation, they seek to perform real-time analysis of these logs using heuristics. Occasionally, the customer needs to verify these heuristics, necessitating a review of data samples from the past 12 hours. What would be the most effective strategy to address the customer's needs?
A)	
Setup Auto Scaling group of EC2 Syslog servers and store the logs S3 use EMR to apply heuristics on the logs
B)	
Send all the log events to Amazon SQS. Setup an Auto Scaling group of EC2 servers to consume the logs and apply the heuristics
C)	
Send all the log events to Amazon Kinesis Data Streams. Develop a client process to apply heuristics to the logs
D)	
Configure Amazon Cloud Trail to receive custom logs and use EMR to apply heuristics to the logs
C
------
A third-party auditor has been engaged to assess the security processes and configurations across all AWS accounts of a company. The company currently does not utilize any on-premises identity provider and instead depends on IAM accounts within each AWS account. The auditor requires read-only access to all AWS resources in each account. The auditor possesses an IAM user in their own AWS account. Considering these requirements, what is the most secure and straightforward approach to facilitate access for the security auditor?
A)	
Create a custom identity broker application that allows the auditor to use existing Amazon credentials to log into the AWS environments
B)	
Create an IAM user for each AWS account with read-only permission policies for the auditor, and disable each account when the audit is complete
C)	
Configure an on-premise AD server and enable SAML identity federation for single sign-on to each AWS account
D)	
Create an IAM role with read-only permissions to all AWS services in each AWS account. Allow the auditor IAM user to assume the ARN role for each AWS account
D
-------
An organization leverages AWS Organizations to oversee numerous accounts in the AWS cloud. Customers' data is stored in Amazon S3 buckets across these accounts, with encryption implemented using server-side encryption and customer-managed AWS KMS keys. The operations team aims to detect any sensitive personal information stored in any of the accounts within AWS Organizations. The solution must be able to adapt effortlessly to new accounts added to AWS Organizations without necessitating further modifications. How can a solution be crafted to fulfill these criteria?
A)	
Enable Amazon Macie within AWS Organizations. Turn off Amazon Macie Auto-enable settings. Deny the Macie service-linked IAM role in the AWS account permissions to decrypt the S3 objects
B)	
Enable Amazon Macie within AWS Organizations. Turn on Amazon Macie Auto-enable settings. Grant the Macie service-linked IAM role in the AWS account permissions to decrypt the S3 objects
C)	
Enable Amazon Macie within AWS Organizations. Turn off Amazon Macie Auto-enable settings. Grant the Macie service-linked IAM role in the AWS account permissions to decrypt the S3 objects
D)	
Enable Amazon Macie within AWS Organizations. Turn on Amazon Macie Auto-enable settings. Deny the Macie service-linked IAM role in the AWS account permissions to decrypt the S3 objects
------
As a Solution Architect in a Government research company, you have been tasked with developing a framework to ensure compliance for all AWS resources spread across multiple accounts and regions. This framework should include rules and remediation actions provided by the Cloud Security Officer, as well as a reporting aspect to reduce the time resources are left in a non-compliant state. What steps will you take to achieve this goal?
A)	
Define all the rules and remediation actions in AWS Config. Then use AWS Config Conformance Packs to deploy the AWS Config rules and remediation action as a single entity.
B)	
Include all the compliance rules from Cloud Security Officers to AWS Elastic Beanstalk while provisioning your resources.
C)	
Automate all your compliance checks and patching using AWS Systems Manager Run Command.
D)	
Suggest the Cloud Security Officers to write their rules in AWS Systems Manager Compliance service.
----

The client has set up AWS Storage Gateway using a gateway-cached volume at their primary location. You are tasked with recovering the Storage Gateway data in AWS. How do you plan to execute this process?
A)	
Create an Amazon EBS volume from a gateway snapshot and mount it to an Amazon EC2 instance
B)	
Use an HTTPS GET to the Amazon S3 bucket where the files are located
C)	
Restore by implementing a lifecycle policy on the Amazon S3 bucket
D)	
Make an Amazon Glacier Restore API call to load the files into another Amazon S3 bucket within four to six hours
------
As a Solution Architect of a startup company, to reduce costs and improve performance, you want to identify workload patterns based on the usage and cost for diverse workloads in AWS compute resources like Amazon EC2 instance types, Amazon Elastic Block Store (EBS) volumes, Auto Scaling Group, AWS Lambda functions, etc. and avoid overprovisioning and underprovisioning of those resources. You are expecting some kind of dashboard view in AWS that shows the savings and performance improvement opportunities at the account level, the estimated monthly savings and the possible savings for over-provisioned resources, and the bottleneck risk with the current configuration for under-provisioned resources. Which of the below services in AWS can serve your purpose?
A)	
There is no Dashboard available to capture these metrics. You need to create one in CloudWatch Dashboards manually. Based on the CloudWatch metrics, you optimize your services and resources.
B)	
Use AWS Compute Optimizer to avoid overprovisioning or underprovisioning the above-mentioned AWS resources based on the utilization and evaluate estimated savings and performance improvement opportunities at the account level.
C)	
Configure AWS Service Catalog with the AWS resources that you want to track based on their utilization and use the recommendation to optimize.
D)	
Use AWS Budgets to track AWS cost and usage, receive recommendations on resources based on the utilization and follow the recommendations to optimize your services and resources.
-----
Your organization operates a microservice-oriented application. DynamoDB is utilized for data storage, while AWS API Gateway manages the Rest APIs. Additionally, Lambda non-proxy integration is being used. A modification was made by the development team to a Rest API method, resulting in the API malfunctioning. You have been tasked with investigating the problem. What is the accurate statement?
A)	
You should change the Cache time-to-live (TTL) value and update the Lambda Code
B)	
You can't change the Rest API's in AWS API Gateway
C)	
As the development team has recently made a change in the method of the Rest API. They should re-deploy the API
D)	
As the development team has recently made a change in the stage of the Rest API. They should re-deploy the API
------

You are setting up a URL whitelisting system for a company that wishes to limit outbound HTTPS connections to specific domains from their EC2-hosted applications. A single t2.micro EC2 instance is deployed to run proxy software, configured to accept traffic from all subnets and EC2 instances in the VPC. The proxy is set to only allow traffic to domains defined in its whitelist configuration. During a nightly maintenance window of 10 minutes, all instances fetch new software updates, each update being around 200MB in size. Despite most days running smoothly, you observe that certain machines are unable to download specific software updates within the maintenance window for a few days. The download URLs for these updates are correctly included in the proxy's whitelist configuration, and they can be accessed manually using a web browser on the instances. What could be causing this issue?
A)	
The route table for the subnets containing the affected EC2 instances is not configured to direct network traffic for the software update locations to the proxy
B)	
You are running the proxy on an undersized EC2 instance type. So network throughput is not sufficient for all instances to download their updates in time
C)	
You have not allocated enough storage to the EC2 instance running the proxy. So the network buffer is filling up causing some requests to fail
D)	
You are running the proxy in a private subnet but have not allocated enough EIP's to support the needed network throughput through the Internet Gateway (IGW)
------
The company recently introduced a mobile app that enables users to capture images of their daily meals, share them with others, and receive feedback to support a healthy eating regimen. These images are stored in S3 and distributed via CloudFront. The CEO believes that the storage is not efficiently optimized based on the expenses. He has requested access log reports to be generated and for the images to be transferred to a different storage if they are not frequently accessed. Although it is uncertain which images will be frequently accessed, historical data analysis indicates that usage declines after the initial 3-4 weeks. What would be the most effective approach to reduce costs while ensuring accessibility?
A)	
Store the images on EC2 EBS and serve it from there. EBS is highly optimized and cheap compared to S3. Put a lifecycle event to shift the unused images to S3 after 30 days
B)	
Use CloudFront Edge Locations and enable access logs. It will automatically optimize the storage cache based on the access pattern
C)	
Apply Lifecycle event to migrate from S3 Standard to Glacier after 3 weeks
D)	
Create an elastic load balancer, point to the CloudFront distribution, and enable the Access Logs. Use Kinesis to process the logs and shift the images to S3 Infrequent Access based on low usage
E)	
Store the images with S3 Intelligent Tier. It will automatically select the best storage class depending on the access pattern
----
A start-up company has installed thousands of sensors worldwide to monitor environmental changes. These sensors transmit a continuous data log, each under 4Kb, which requires real-time analysis, along with a summary of the environmental data for future reference. The company seeks a cost-effective managed solution to establish this system on AWS Cloud. The proposed solution must be highly scalable to accommodate potential future expansion. What solution can be developed to fulfill these needs?
A)	
Capture the streaming data using Amazon Kinesis Data Streams and send it to the Amazon EC2 instance. Use KCL libraries on the Amazon EC2 instance to analyze the data. Store the analyzed data in the Amazon S3 bucket.
B)	
Capture the streaming data using Amazon Kinesis Data Streams. Use Kinesis Data Analytics for Apache Flink for the analysis of streaming data and store processed data in Amazon S3.
C)	
Capture the streaming data using Amazon Data Pipeline. Use Kinesis Data Analytics for Apache Flink for analysis of streaming data and store processed data in Amazon S3.
D)	
Capture the streaming data using Amazon Data Pipeline. Store the data in Amazon S3 and analyze the data using Amazon Athena. Store the analyzed data in different Amazon S3 buckets.
------
You have launched a web application aimed at a worldwide audience across various AWS Regions using the domain name example.com. To optimize user experience, you opt for Route53 Latency-Based Routing, ensuring that web requests are directed to the nearest region. To maintain business continuity during server outages, you set up weighted record sets linked to two web servers located in different Availability Zones within each region. However, during a disaster recovery test, you observe that when all web servers in one region are disabled, Route53 fails to reroute all users to the alternative region. What might be the cause of this issue? Select two answers from the options provided.
A)	
You did not set "Evaluate Target Health" to "Yes" on the latency alias resource record set associated with example.com in the region where you disabled the servers
B)	
Latency resource record sets cannot be used in combination with weighted resource record sets
C)	
You did not set up an HTTP health check to one or more of the weighted resource record sets associated with the disabled web servers
D)	
The value of the weight associated with the latency alias resource record set in the region with the disabled servers is higher than the weight for the other region
E)	
One of the two working web servers in the other region did not pass its HTTP health check
----
One company has implemented Service Control Policies (SCP) within an AWS Organization to restrict the launch of any instance type other than t2.micro. The AWS Organization consists of a single Organizational Unit (OU) with two accounts: Production and Development. The Development account requires the ability to launch a c5.xlarge instance type for a month to conduct testing on a new application. After the testing phase, the Development account should be limited to launching only t2.micro instances. The Production account should always be restricted to launching t2.micro instances. What adjustments can be made to the SCP to fulfill these requirements?
A)	
Attach a new SCP to the Development account which will allow the launch of the c5. xlarge instance type. Make no changes is the existing SCP attached to the root of the Organizations.
B)	
Create a new OU named Development. Move the Development account to this OU. Create a new SCP allowing access to launch the c5. xlarge instance type. Make no changes to the existing SCP attached to the root.
C)	
Create a new OU named Development. Move the Development account to this OU. Create a new SCP allowing to launch c5. xlarge instance type and attach it to the new OU. Detach existing SCP from the root and attach it to the OU which has a Production account.
D)	
Detach existing SCP from the root of the Organization. Attach a new SCP which will allow the launch of the c5. xlarge instance type. Post testing phase, revert these SCP.
------
Your organization utilizes AWS Direct Connect for linking the on-premises network with an AWS VPC. The DNS records of AWS resources within the VPC are overseen by a Route 53 private hosted zone. To enable the resolution of records in the Route 53 private hosted zone within the on-premises network, you are now seeking to redirect DNS queries from the on-premise network to the Route 53 Resolver. What action should be taken to fulfill this requirement?
A)	
Include all the Route 53 domain names in the Route 53 Resolver so that the Resolver can automatically resolve domain names and answer DNS queries from the on-premises network.
B)	
Configure resolvers on the on-premises network to forward DNS queries to the domain name or the IP address of the Route 53 Resolver.
C)	
Create a Route 53 Resolver inbound endpoint in the VPC and configure resolvers on the on-premises network to forward DNS queries to the inbound endpoint.
D)	
Create a Route 53 Resolver outbound endpoint in the VPC and create one or more rules to specify the domain names of the DNS queries that you want resolvers on the on-premises network to forward to Route 53.
------
A manufacturing firm has implemented AWS Managed Microsoft AD to oversee a substantial user base within the AWS cloud environment. The Security team aims to collect event logs from the AD controller, including instances of failed login attempts and modifications to user groups. These logs need to be analyzed in real-time, and a dashboard should be developed to illustrate trends and insights related to each event. What is the most efficient way to design a solution that meets these requirements?
A)	
Stream event logs from AD controllers to Amazon Kinesis Data Analytics using Amazon CloudWatch Logs and Amazon Kinesis Firehose. Analyze the events in Amazon Kinesis Data Analytics and store the results in Amazon Redshift using Amazon Kinesis Firehose. Use Amazon QuickSight to create a dashboard for trends based on the data stored in Amazon Redshift.
B)	
Stream event logs from AD controllers to Amazon Kinesis Data Analytics using Amazon CloudWatch Logs and Amazon Kinesis Data Streams. Store the events analyzed in Amazon Kinesis Data Analytics in an Amazon S3 bucket using Amazon Kinesis Firehose. Use Amazon Quick Sight to create a dashboard for trends based on the data stored in Amazon S3.
C)	
Stream event logs from AD controllers to Amazon OpenSearch Service using Amazon CloudWatch Logs and AWS Lambda. Analyze events in Amazon OpenSearch Service and create a visualization in the Amazon OpenSearch dashboard.
D)	
Stream event logs from AD controllers to Amazon OpenSearch Service using Amazon CloudWatch Logs and Amazon Kinesis Firehose. Analyze events in Amazon OpenSearch Service and create a visualization in the Amazon OpenSearch dashboard.
--------
You are overseeing an AWS Organization that consists of several Organizational Units (OUs). The default Service Control Policy (SCP) named "FullAWSAccess" has been deleted from the Root, resulting in all actions across all services being implicitly denied. Custom policies have been applied to both the Root and the OUs to explicitly permit the services you wish to allow. Your current objective is to pinpoint the permitted services that have not been utilized for an extended period and subsequently remove them from the allowed list. What is the most effective method to accomplish this task?
A)	
Use AWS CLI "aws iam get-service-last-accessed-details" to retrieve service last accessed information for the IAM entities owned by the Organization. For the services that are not needed, remove them from the SCP allow list.
B)	
Detach the policies from an OU, monitor the failed APIs in CloudTrail, and identify the services required by the OU. Modify the policies to only allow the required services and reattach the policies in the OU.
C)	
View the last accessed information in "AWS IAM > Access reports > Organization activity". If there are services that are not accessed for a long time, remove them from the Organization Service Control Policies (SCPs).
D)	
In "AWS IAM > Policies > Access Advisor", check the "Last Accessed" column for the services that are not accessed. Remove them from the Organization SCP allow list.
----
You have recently joined a company and are responsible for managing an AWS Organization with multiple Organizational Units (OUs). The organization's Root has a "FullAWSAccess" SCP attached, allowing all services and actions. Additional policies are attached to OUs to restrict users from using specific AWS services or performing certain actions (e.g. deleting DynamoDB tables). Your manager tasks you with identifying the allowed AWS services that have not been accessed for 6 months in the Development OU. What is the easiest way to accomplish this?
A)	
In the AWS console, go to AWS Organizations > Development OU > Policies, select the applied SCPs, and review whether there are any services that are not accessed for 6 months.
B)	
In the AWS console, go to CloudTrail > Event history, and search for the services accessed within 6 months. Compare the services with the allowed services in the SCP. Identify the allowed services that are not accessed.
C)	
In the AWS console, go to IAM > Access analyzer, and create a new analyzer in the AWS Organization. Monitor the "Active findings" in the analyzer and identify the AWS services that are not accessed for 6 months.
D)	
In the AWS console, go to IAM > Access reports > Organization activity, select the Development OU, and check the last accessed information in the "Service access report" table.
----
In an AWS Organization, the Root is attached to a default Service Control Policy (SCP) that allows all actions on all resources, while other Organizational Units (OUs) or AWS accounts have SCPs with Deny lists. For instance, an SCP that denies cloudtrail:StopLogging is attached to an OU. You believe these Deny lists can be enhanced by including more unused services. How would you identify the AWS services that are permitted by the SCP but are never utilized?
A)	
In the IAM console, click the Organization activity and check the last accessed data to identify services that are never used
B)	
In the AWS Organization console, identify allowed services that are never used by AWS accounts
C)	
In the IAM credential report of AWS accounts, examine those services that are not required to be allowed by SCPs
D)	
In the AWS Config console, list the AWS services that are not used by IAM users
-----
A company has established several AWS accounts that are organized under AWS Organizations. The security team is tasked with implementing a unified security group for all Amazon EC2 instances across these accounts. Additionally, developers within each account should have the capability to create their own security groups for specific applications, in addition to the shared security groups. What solution can be recommended to meet this requirement?
A)	
Enable AWS Config on all accounts in the AWS Organizations. Create a primary security group under AWS Firewall Manager and create policies within AWS Firewall Manager that can be applied to individual application security groups by mapping to specific application name/value tags
B)	
Disable AWS Config from all member accounts in the AWS Organizations. Create a primary security group under AWS Organizations and create policies within AWS Firewall Manager that can be applied to individual application security groups by mapping to specific application name/value tags
C)	
Enable AWS Config on all member accounts in the AWS Organizations. Create a primary security group under AWS Organizations and create policies within AWS Firewall Manager that can be applied to individual application security groups by mapping to specific application name/value tags
D)	
Enable AWS Config on management account in the AWS Organizations. Create a primary security group under AWS Firewall Manager and create policies within AWS Firewall Manager that can be applied to individual application security groups by mapping to specific application name/value tags
---------
Your AWS Organization has below hierarchy. The OUs are attached with below SCPs:
Root: FullAWSAccess.
Admin_OU: Deny S3 upload action if without encryption.
DEV1_OU: Deny all S3 actions.
DEV2_OU: Allow all S3 actions.
An AWS Account is attached under DEV2_OU, and it has an IAM user Bob who is given full permissions to S3 resources. What will happen when the user Bob is trying to upload objects to an S3 bucket without encryption?
A)	
The action will be allowed as DEV2_OU is attached with an S3 Allow SCP policy, which takes priority
B)	
The action will be denied as the SCP in Admin_OU denies the operation
C)	
The action will be allowed as the SCP in the root has full AWS access, and Bob is attached with full S3 permissions
D)	
The action will be denied as SCP in DEV1_OU has an S3 Deny policy, which takes priority
---------
An organization has implemented a web application on the AWS cloud using Amazon EC2 instance and Amazon RDS. An outage was reported recently due to Amazon RDS DB instances running out of storage. The operations team restored the DB instance, but the team's leader has requested a proactive monitoring solution for the DB instance storage and notification system for low storage space. Additionally, the management team wants the RDS instance storage to automatically adapt to additional storage requirements without manual intervention due to unpredictable workload. What solution can be proposed to meet these requirements? Select two answers from the options provided.
A)	
Enable Storage autoscaling on an Amazon RDS DB instance
B)	
Deploy Amazon RDS on Amazon EBS optimized instance
C)	
Monitor available DB instance storage space by using the FreeStorageSpace metric in Amazon CloudWatch and create a notification if threshold values are exceeded
D)	
Enable Provisioned IOPS SSD storage type with Amazon RDS DB instance
E)	
Monitor available DB instance storage space by using the FreeLocalStorage metric in Amazon CloudWatch and create a notification if threshold values are exceeded
------
Your team is required to develop a new database for storing time series data obtained from EC2 instances' metrics such as CPU/memory usage, IOPS, network data, and more. This database will play a crucial role in the DevOps solution responsible for monitoring EC2 health and usage metrics, as well as analyzing data in near real-time to enhance performance and availability. Once the database is created, the next step involves configuring scheduled queries to process the data and store the query results in a distinct table. These scheduled queries are primarily utilized for real-time analytics. How do you plan to architect this solution in AWS?
A)	
Set up the time series database in an Amazon Timestream database. Use a Lambda function to perform the required real-time analytics. Invoke the Lambda function with a cron expression in a CloudWatch Event rule
B)	
Store the time series data in an Amazon DynamoDB NoSQL database. Set up scheduled queries through Amazon EventBridge and Lambda function
C)	
Store the time series data in Amazon Keyspaces which is a serverless Apache Cassandra database service. Use standard SQL commands to perform scheduled queries
D)	
Set up the time series database using Amazon Timestream. Use the scheduled query feature in Amazon Timestream to define the real-time analytics queries
-------
A trading consortium has established a private blockchain network utilizing Amazon Managed Blockchain with the Hyperledger Fabric framework. This network comprises several AWS accounts as its members. To facilitate resource access for all members, VPC Private endpoints have been implemented. They have partnered with a new distributor that must be integrated into this network. It is essential for distributors to join the network effortlessly and gain access to the Hyperledger Fabric resources. What series of actions should a solution architect undertake to fulfill these requirements? Select two answers from the options provided.
A)	
Create a proposal for inviting other AWS accounts to the blockchain network. Once a proposal is approved by current members of the network, other AWS accounts will receive the invite
B)	
Create a proposal for inviting other AWS accounts to the blockchain network. Once a proposal is approved by an administrator in the network, other AWS accounts will receive the invite
C)	
Create a new VPC PrivateLink endpoint from all the current member VPC to new account VPC to enable access to Hyperledger Fabric resources
D)	
Create a single VPC PrivateLink endpoint for all members in the AWS account from which Hyperledger Fabric resources will be accessed
E)	
Create multiple VPC PrivateLink endpoints for each member in the AWS account from which Hyperledger Fabric resources will be accessed
---------
As an AWS consultant, you are tasked with creating a solution for a new web application that focuses on video analysis. The application must be able to detect and identify objects and events within uploaded video files, such as trees, flowers, and parties. The analysis results will then be stored in a NoSQL database for future processing. Additionally, the application should be serverless and only incur charges when processing uploaded videos. Which option would you choose to meet these requirements?
A)	
Store the video files in S3 and trigger a Lambda function for S3 events. In the Lambda function, trigger Amazon Rekognition API "StartLabelDetection" to detect labels in the videos. Store the results of labels in a DynamoDB table
B)	
Store the video files in an Amazon Kinesis Video Stream. Configure an Amazon Rekognition Video stream processor to recognize attributes in the streaming video. Store the results in a DynamoDB table
C)	
Store the video files in S3 and create an event notification to trigger a Lambda function. In the Lambda function, trigger Amazon Textract APIs to detect attributes and events in the videos. Store the results in Amazon ElastiCache
D)	
Store the video files in an Amazon Kinesis Video Stream. Use a Lambda function to trigger Amazon Rekognition Video API "StartLabelDetection" to detect attributes in the Kinesis Video Stream. Store the results in a DynamoDB table
--------
Your team is in the process of creating a mobile application and intends to utilize the Amazon Cognito identity pool for issuing temporary credentials to the app in order to access AWS resources. The decision has been made to opt for the "enhanced authflow" feature of Cognito to streamline the process of obtaining credentials through network calls. Initially, the app will authenticate with a third-party identity provider such as Facebook, submit an ID token via a GetID request to the Amazon Cognito identity pool, and then swap the token for an identity ID. What is the appropriate choice for the subsequent authentication flow?
A)	
The identity ID is used in a GetCredentialsForIdentity request to the Amazon Cognito identity pool. If the identity ID is validated successfully, AWS API credentials will be returned.
B)	
The identity ID is used in a GetOpenIdToken request to the Amazon Cognito identity pool. A new OAuth 2.0 token is returned and used in an AssumeRoleWithWebIdentity request to retrieve AWS API credentials.
C)	
The identity ID is used in a GetOpenIdTokenForDeveloperIdentity request to the Amazon Cognito identity pool. A new OAuth 2.0 token is returned and used in an AssumeRoleWithWebIdentity request to retrieve AWS API credentials.
D)	
The identity ID is used in a GetCredentialsForIdentity request to the Amazon Cognito identity pool. If the identity ID is validated successfully, a new OAuth 2.0 token is returned. The app uses the new token in an AssumeRoleWithWebIdentity request to Cognito to retrieve AWS API credentials.
--------
You utilize AWS Cognito User Pool to set up a user directory for an application. The goal is to categorize users into readers, contributors, and editors of the app. Readers are limited to reading contents from AWS S3 buckets, contributors can add contents to Amazon S3 buckets, and editors have the authority to publish contents through an API in Amazon API Gateway. What is the most effective approach to meet this requirement in AWS Cognito?
A)	
Directly attach an IAM policy to each user in Amazon Cognito User Pool. Make sure each user has an appropriate IAM policy according to the user role
B)	
In IAM, add different groups and assign suitable IAM policies. In Amazon Cognito User Pool, assign users to the IAM groups
C)	
Configure different IAM roles in IAM for readers, contributors and editors. In Amazon Cognito User Pool, configure each user with an IAM role
D)	
In Amazon Cognito User Pool, create groups and assign IAM roles to them. Add users to the groups to assign the required permissions
--------
As a software engineer, you are in the process of developing a new web service on AWS focused on daily schedules that users can customize and retrieve. This service features an AngularJS front end that interacts with a DynamoDB table named "UserScheduleData," which has both read and write access. You intend to utilize API Gateway and Lambda for the backend functionality. Throughout the development phase, it is essential to conduct frequent integration tests using curl to verify the API endpoints. You have established a role called "ScheduleRoleLambda" specifically for the Lambda function. What steps should you take to ensure that Lambda has the required permissions within the service role? Select two answers from the options provided.
A)	
An IAM policy to allow DynamoDb access is needed for "ScheduleRoleLambda". The resource should be the arn of "UserScheduleData" and the actions should contain "dynamodb:GetItem" and "dynamodb:PutItem"
B)	
AWSXrayWriteOnlyAccess policy is needed for "ScheduleRoleLambda" so that a segment record with details about the function invocation and execution can be saved for tracking and debug purpose
C)	
"ScheduleRoleLambda" should have a policy for CloudWatch Logs including CreateLogGroup, CreateLogStream and PutLogEvents
D)	
"sns:publish" allow inline policy should be added into "ScheduleRoleLambda" for error handlings. For example, when exception appears, the message can be put into a dead letter queue via SNS publish
E)	
"ScheduleRoleLambda" should contain an inline policy to allow DynamoDb access. The resource should be "*" and the action should contain "dynamodb:FetchItem", "dynamodb:PutItem" and "dynamodb:Query"
---------
As an AWS solutions architect at your company, you are tasked with deploying AWS resources primarily in the us-east-1 region, which involves creating multiple VPCs and subnets. Additionally, the company aims to develop and operate applications on-premises using the same programming interfaces as AWS. To enable communication between local AWS compute instances and other instances within the same VPC in the AWS region, subnets must be established on the local network. How will you design a solution to fulfill these needs?
A)	
Set up AWS Outposts to run the applications on-premises. Connect Outpost to the AWS us-east-1 region with VPN connections. Create a new VPC with subnets on Outpost and establish the VPC peer connections between the Outpost VPC and AWS VPC.
B)	
Set up AWS Local Zone to run the applications on-premises. Connect Local Zone to the AWS us-east-1 region with Direct Connect. Create subnets on the Local Zone and launch on-premises AWS resources in the subnets.
C)	
Set up AWS Local Zone to run the applications on-premises. Connect Local Zone to the AWS us-east-1 region with VPN connections. Create a new VPC with subnets on the Local Zone and establish the VPC peer connections between the Local Zone VPC and AWS VPC.
D)	
Set up AWS Outposts to run the applications on-premises. Connect Outpost to the AWS us-east-1 region with Direct Connect. Create subnets on the Outpost and launch on-premises AWS resources in the subnets.
--------
You've obtained a new agreement from a customer to transfer all of their current infrastructures to AWS. You've observed that they are operating some of their applications using multicast, and they require it to remain operational as is when it is moved to AWS. You've found out that multicast is not supported on AWS, as you cannot handle multiple subnets on a single interface on AWS, and a subnet can only be associated with one availability zone. What would allow you to implement legacy applications on AWS that depend on multicast?
A)	
Create all the subnets on a different VPC and use VPC peering between them
B)	
Provide Elastic Network Interfaces to communicate between the subnets
C)	
Rely on a Transit Gateway, enable multicast, and create a multicast domain associated with the relevant subnets
D)	
Create all the subnets in a single VPC
---------
Your company has requested the development of a mobile application that utilizes DynamoDB as the backend and Javascript as the front end. While using the application, you have observed that write requests are occasionally throttled due to insufficient provisioned write capacity during daytime. What would be the most efficient way to address this DynamoDB issue?
A)	
Launch DynamoDB in Multi-AZ configuration with a global index to balance writes
B)	
Enable DynamoDB Auto Scaling to meet the requirements
C)	
Increase write capacity of DynamoDB to meet the peak loads
D)	
Use the SQS service to read messages in the queue and write these to DynamoDB
-----
Your company has requested the development of a mobile application that utilizes DynamoDB as the backend and Javascript as the front end. While using the application, you have observed that write requests are occasionally throttled due to insufficient provisioned write capacity during daytime. What would be the most efficient way to address this DynamoDB issue?
A)	
Launch DynamoDB in Multi-AZ configuration with a global index to balance writes
B)	
Enable DynamoDB Auto Scaling to meet the requirements
C)	
Increase write capacity of DynamoDB to meet the peak loads
D)	
Use the SQS service to read messages in the queue and write these to DynamoDB
Your team is in the process of creating a fresh Lambda function for a microservice element. The Lambda function must be packaged and deployed as a container image. This container image should be constructed using the python:buster image as a foundation, with additional dependencies and libraries included. To ensure the proper utilization of the container image for the Lambda function, what action needs to be taken?
A)	
Install the runtime interface client in the container image to make it compatible with Lambda
B)	
In the Dockerfile, assume the IAM role through the "aws sts assume-role" CLI for the Lambda function during runtime
C)	
Install the CloudWatch Log agent in the container image for the Lambda function to forward its logs to a CloudWatch Log group
D)	
Install the Amazon Elastic Container Registry (Amazon ECR) agent for the Lambda function to interact with ECR to fetch the Docker image

---
A financial institution recently experienced suspicious activity and intends to leverage Amazon Detective for streamlined analysis, investigation, and prompt identification of the underlying causes of security concerns or questionable behaviors. Given the substantial volume of data involved, the company is interested in managing multiple accounts with Amazon Detective. As an AWS Architect for the organization, which option would you recommend as the optimal solution?
A)	
Amazon Detective is a multi-account service that aggregates data from monitored member accounts under a single administrative account globally. Hence, it's possible to manage multiple accounts with Amazon Detective
B)	
Amazon Detective is a single-account service that aggregates data from monitored member accounts under a single administrative account globally. Hence, not possible to manage multiple accounts with Amazon Detective
C)	
Amazon Detective is a single-account service that aggregates data from monitored member accounts under a single administrative account within the same region. Hence, not possible to manage multiple accounts with Amazon Detective
D)	
Amazon Detective is a multi-account service that aggregates data from monitored member accounts under a single administrative account within the same region. Hence, it's possible to manage multiple accounts with Amazon Detective

--------------
The fintech company from Japan is currently utilizing AWS to run their mission-critical applications. They are seeking a solution to analyze the application logs through Amazon Redshift. The logs are being forwarded to a Kinesis Data Firehose. How would you recommend sending the records from Kinesis Data Firehose to Redshift?
A)	
Directly send the data to Amazon Redshift using a custom Lambda function
B)	
Configure Kinesis Data Firehose to deliver your data to the S3 bucket first and then issue an Amazon Redshift COPY command to load the data into your Amazon Redshift cluster
C)	
Use Amazon S3 to store raw data and send the data to Amazon Redshift using Load Command
D)	
Directly send the data to Amazon Redshift using an SQS queue
---------
As an AWS Solutions Architect in a large organization, you are currently faced with the challenge of managing AWS AMIs in a non-standardized manner across different teams. By implementing EC2 Image Builder, you can streamline the creation and management of AMIs. What advantages can you gain from using EC2 Image Builder? Select two answers from the options provided.
A)	
EC2 Image Builder pipelines are based on Packer so that Packer templates can be reused
B)	
EC2 Image Builder pipelines always use the latest operating system in which the latest security patches are installed
C)	
In an EC2 Image Builder pipeline, users can choose to install Amazon managed components such as the CloudWatch agent and the CodeDeploy agent
D)	
With an EC2 Image Builder pipeline, users can automatically deploy the AMIs in EC2 instances or Auto Scaling groups in different AWS Regions
E)	
In an EC2 Image Builder pipeline, the generated AMIs can be automatically distributed to multiple AWS Regions or shared with other AWS accounts
--------
The developer team has utilized Amazon API Gateway and AWS Lambda to create a new web application. They plan to use REST APIs to synchronously call the AWS Lambda function. With the expectation of a large client response, the team is seeking a secure authentication solution. What is the most effective solution that can be designed for this requirement?
A)	
Create an IAM user policy to invoke API. Attach this policy to Amazon API Gateway which will control access to the APIs.
B)	
Create a request parameter-based Lambda authorizer. Configure API Gateway to call Lambda authorizer to authenticate clients making a request using REST API.
C)	
Create users in Amazon Cognito user pools. Create an API Gateway authorizer with this user pool and enable the authorizer on the REST API.
D)	
Create resource policies matching specific users. Attach this resource policy to Amazon API Gateway which will control access to the APIs.
------
n your role as an AWS Solutions Architect for a prominent e-commerce company, you are responsible for creating a robust and scalable DNS solution capable of handling a high volume of queries. The company currently relies on Amazon Route 53 as its main DNS service, but there are concerns about potential single points of failure and the need for quicker query resolution. To address these issues, you opt to implement Amazon Route 53 Resolver, a feature that enhances query resolution speed and availability by offering both inbound and outbound DNS query capabilities. Which combination of options would best enable Amazon Route 53 Resolver for the company's DNS infrastructure, ensuring both high availability and scalability? Select two answers from the options provided.
A)	
Creating an outbound resolver endpoint in each availability zone and configuring Amazon Route 53 to forward all queries to the endpoint in the nearest region
B)	
Creating an inbound resolver endpoint in each availability zone and configuring Amazon Route 53 to forward all queries to the endpoint in the same availability zone as the client
C)	
Setting up a secondary hosted zone in Amazon Route 53 and configuring a failover routing policy to automatically switch to the secondary zone in case of failure
D)	
Using Amazon Route 53 Resolver Rules to forward queries to a specific set of IP addresses based on the query type, in order to optimize query resolution time
E)	
Enabling Amazon Route 53 Resolver for all VPCs within the company's AWS infrastructure, and using Route 53 Resolver to forward queries to on-premises DNS servers for resolution
----
18)	Your team is in the process of creating a new web application. Since the application is container-based, the decision has been made to utilize AWS ECS Fargate for its ease of use. Additionally, a straightforward and adaptable Elastic File System (EFS) volume is necessary due to the application's reliance on files for state persistence. An Amazon ECS Cluster and an EFS file system have already been established. In order to effectively mount the Amazon EFS file system on ECS Fargate, what conditions need to be satisfied? Select two answers from the options provided.
A)	
The EFS file system, Amazon ECS cluster, and Fargate tasks must be in the same VPC.
B)	
The security group of the EFS file system should allow the inbound connections on port 2049 from the ECS Fargate task or service.
C)	
The security group of the ECS Fargate task should allow the inbound connections on port 2049 from the EFS file system's security group.
D)	
The security group of the EFS file system should allow the outbound connections on port 80/443 to the ECS Fargate service.
E)	
The EFS file system, Amazon ECS cluster, and Fargate tasks must be in the same availability zone.
A,B
-----
A large engineering firm has deployed IoT sensors in multiple factories to collect equipment metrics. Analysts in the head office need to query equipment metrics in these locations to get the health status of the equipment and visualize metrics in near-real time. In the future, there would be thousands of sensors added in new factory locations which should be provisioned automatically for data ingestion and performance insights of the equipment. What solution can be suggested for this requirement?
A)	
Ingest data from IoT Core via MQTT protocol to AWS IoT Analytics. Use AWS IoT Analytics to get near-real-time visualization of the equipment's data. Use the Amazon CloudFormation template to automate the creation of resources for data ingestion
B)	
Ingest data from IoT Core via MQTT protocol to AWS IoT SiteWise. Use the AWS IoT SiteWise plugin for Grafana to get near-real-time visualization of the equipment's data. Use AWS IoT Device Management to automate the creation of AWS IoT SiteWise resources
C)	
Ingest data from IoT Core via MQTT protocol to AWS IoT SiteWise. Use the AWS IoT SiteWise plugin for Grafana to get near-real-time visualization of the equipment's data. Use the Amazon CloudFormation template to automate the creation of AWS IoT SiteWise resources
D)	
Ingest data from IoT Core via MQTT protocol to AWS IoT Analytics. Use AWS IoT Analytics to get near-real-time visualization of the equipment's data. Use AWS IoT Device Management to automate the creation of AWS IoT resources for data ingestion
----
As an AWS cloud engineer, you are responsible for overseeing a significant quantity of EC2 instances within AWS. The majority of these instances utilize customized RHEL 8 AMI. In order to effectively manage these instances within AWS Systems Manager, you have manually installed the SSM agents on the EC2 instances. However, there are instances where the SSM agents do not function properly. You are seeking to establish a service that will allow for easy viewing of the SSM agent logs and monitoring of the agent's running status. What steps would you take to configure this service?
A)	
In Change Manager of AWS Systems Manager, turn on the CloudTrail Lake event tracking to monitor all the management events from the SSM agents
B)	
Locate the SSM agent configuration file "/etc/amazon/ssm/seelog.xml.template" in EC2. Change the default logging by modifying the minlevel value from info to debug
C)	
Create a log group in CloudWatch Logs. Log into the instance through SSH and locate the SSM agent configuration file "/etc/amazon/ssm/seelog.xml.template" in EC2 and add an element to forward the SSM agent logs to the CloudWatch log group
D)	
Create a new trail in AWS CloudTrail and configure an Amazon SNS notification for the trail. View all the Systems Manager API calls as events in CloudTrail
------
When creating an AWS CloudFormation template, you may need to assign values to properties that are not available until runtime. In such cases, you can utilize intrinsic functions, but you may be uncertain about where in the template they can be applied. Which of the options accurately describes the current usage of intrinsic functions in an AWS CloudFormation template?
A)	
You can use intrinsic functions in any part of a template, except AWSTemplateFormatVersion and Description
B)	
You can use intrinsic functions in any part of a template
C)	
You can use intrinsic functions only in specific parts of a template. You can use intrinsic functions in resource properties, outputs, metadata attributes, and update policy attributes
D)	
You can use intrinsic functions only in the resource properties part of a template
--------------
A mobile application developer has created an app for both iOS and Android platforms that includes a step counting feature. To manage user access, he has implemented AWS Cognito, which allows users to authenticate and grants access to an AWS DynamoDB table. This table is utilized for storing subscriber information and step counts. The developer now seeks to integrate Cognito with Google to enable federated authentication, simplifying the login process for users by eliminating the need for additional credentials. What steps should the developer take to ensure proper authentication and authorization for users with the appropriate permissions in the iOS and Android app? Select two answers from the options provided.
A)	
Only IOS (Objective-C and Swift) works for federated identities if Google access is required for AWS Cognito. This can be done by configuration Cognito identity pools with a Google Client ID. Google federated access does not work for the android app
B)	
Amazon Cognito Identity pools (federated identities) support user authorization through federated identity providers including Amazon, Facebook, Google, and SAML identity providers. The developer just needs to set up the federated identities for Google access
C)	
Only Android works for federated identities if Google access is required for AWS Cognito. This can be done by configuring Cognito identity pools with a Google Client ID
D)	
Amazon Cognito User pools support user authentication through federated identity providers including Amazon, Facebook, Google, and SAML identity providers. The developer just needs to set up the federated identities for Google access in the Cognito User Pool

----
Which of the following statement about deletion of key from AWS Key Management Service (KMS) is true?
A)	
You need to apply for the deletion procedure from the admin account and then schedule for deletion, with a configurable waiting period of 24hrs
B)	
You can schedule an AWS KMS key and associated metadata that you created in AWS KMS for deletion, with a configurable waiting period from 5 to 20 days. You cannot cancel key deletion during the waiting period
C)	
You can schedule an AWS KMS key and associated metadata that you created in AWS KMS for deletion, with a configurable waiting period from 7 to 30 days. You can cancel key deletion during the waiting period
D)	
You can schedule an AWS KMS key and associated metadata that you created in AWS KMS for deletion, with a configurable waiting period of 24hrs. You can cancel key deletion during the waiting period
------
A start-up has transitioned its web application from an on-premises environment to an Amazon EC2 instance. They have established several accounts within AWS Organizations. The initial sizing of the EC2 instance was based on the specifications of the on-premises servers during the migration process. Now, six months post-migration, the Management team seeks to confirm that the Amazon EC2 instances are appropriately sized to ensure optimal application performance in the cloud. Furthermore, to mitigate security vulnerabilities across all accounts, they are specifically requesting critical security recommendations. What solutions can be proposed?
A)	
Use EC2 predictive scaling. Enable Organizational view for the AWS Trusted Advisor and use recommendations in AWS Trusted Advisor Priority aggregated across member accounts in your organization
B)	
Use AWS Cost Explorer EC2 Resource sizing Recommendations. Enable Organizational view for the AWS Trusted Advisor and use recommendations in AWS Trusted Advisor aggregated across member accounts in your organization
C)	
Use AWS Compute Optimizer EC2 instance-type recommendations with enhanced infrastructure metrics. Enable Organizational view for the AWS Trusted Advisor and use recommendations in AWS Trusted Advisor Priority aggregated across member accounts in your organization
D)	
Use AWS Compute Optimizer EC2 instance type recommendations with default infrastructure metrics. Enable Organizational view for the AWS Trusted Advisor and use recommendations in AWS Trusted Advisor Priority aggregated across member accounts in your organization
------------
You are tasked by your Senior Technical Manager to find a solution to reduce costs for a legacy application that currently runs on an m4.large instance size, cannot scale with Auto Scaling, and only operates at peak performance 5% of the time. This inefficiency is resulting in a significant waste of resources and money. Your goal is to maintain the legacy application with reduced memory requirements in the long-term. Which option below will help you achieve this objective?
A)	
Use t2.nano instance and add spot instances when they are required
B)	
Use a "t2.medium - 3 yr RI" burstable performance instance
C)	
Use a C4.large instance with enhanced networking
D)	
Use two t2.nano instances that have single Root I/O Virtualization
------------
Your security officer has informed you that there is a need to enhance the logging of all events happening on your AWS account. He requires the ability to swiftly access all account events across all regions in the most straightforward manner. Additionally, he wants to ensure that he is the sole individual with the most secure access to these events. What would be the most suitable solution to fulfill his requirements?
A)	
Use CloudTrail to log all events to a separate S3 bucket in each region as CloudTrail cannot write to a bucket in a different region. Use MFA and bucket policies on all the different buckets
B)	
Use CloudTrail to log all events to one S3 bucket. Make this S3 bucket only accessible by your security officer with a bucket policy that restricts access to his user only and adds MFA to the policy for a further security level
C)	
Use CloudTrail to log all events to an Amazon Glacier Vault. Make sure the vault access policy only grants access to the security officer's IP address
D)	
Use CloudTrail to send all API calls to CloudWatch and send an email to the security officer every time an API call is made. Make sure the emails are encrypted
----------
An auditor requires access to logs that document all API events on AWS. The organization operates several AWS accounts, and the auditor must have access to the logs across all these accounts. What is the most effective method to set up access for the auditor to review event logs from every account?
A)	
Configure the CloudTrail service in each AWS account and have the logs delivered to a single S3 bucket in a separate account. Provide the auditor to access only to this bucket
B)	
Configure the CloudTrail service in each AWS account, and make the logs delivered to an S3 bucket on each account, while granting the auditor permissions to the bucket via roles in the secondary accounts and a single primary IAM account that can assume a read-only role in the secondary AWS accounts
C)	
Configure the CloudTrail service in the primary AWS account and configure consolidated billing for all the secondary accounts. Then grant the auditor access to the S3 bucket that receives the CloudTrail log files
D)	
Configure the CloudTrail service in each AWS account and enable consolidated logging inside of CloudTrail
------
An enrollment company operates a 3-tier web application on AWS, with a NAT instance in the public Web tier for network address translation. There is sufficient capacity allocated for the anticipated workload during the upcoming fiscal year's benefit enrollment period, with some additional overhead. Enrollment was going smoothly for two days, but unfortunately, the web tier suddenly becomes unresponsive when we investigated using CloudWatch and other monitoring tools. There has been a surprising influx of inbound traffic from a group of 15 IP addresses over port 80, originating from a country where our benefits company does not have any customers. The web tier instances are experiencing such a heavy load that benefit enrollment administrators are unable to SSH into them. What activity could help in countering this attack?
A)	
Create an inbound NACL (Network Access Control List) associated with the web tier subnet with deny rules to block the attacking IP addresses
B)	
Create a custom route table associated with the web tier and block the attacking IP addresses from the IGW (Internet Gateway)
C)	
Change the EIP (Elastic IP Address) of the NAT instance in the web tier subnet and update the Main Route Table with the new EIP
D)	
Create 15 Security Group rules to block the attacking IP addresses over port 80
---------
The educational tech company is looking to enhance its development and operational processes as it transitions to the cloud. After experiencing a significant increase in monthly AWS spending, they discovered that some developers had mistakenly launched Amazon EC2 & RDS instances in unexpected Regions. Your role is to establish best practices to ensure developers have limited privileges and manage access to on-premises and AWS Cloud resources through Active Directory.
You are tasked with implementing a cost-control mechanism by restricting developer access to the AWS Management Console without hindering productivity. The company aims to restrict developers to launching EC2 and RDS instances only in the eu-west-1 region to better manage AWS costs. How can you assist the company in meeting the new security requirements while minimizing the workload on the DevOps team?
A)	
Set up SAML-based authentication tied to an IAM role that has a PowerUserAccess managed policy and a custom policy that denies all the developers access to any AWS services except AWS Service Catalog. Within AWS Service Catalog, create a product containing only EC2 and RDS service in eu-west-1 region.
B)	
Create an IAM user for each developer and add them to the developer IAM group that has PowerUserAccess managed policy attached to it. Attach a custom policy that allows developers to launch EC2 and RDS instances only in eu-west-1 region.
C)	
Set up SAML-based authentication tied to an IAM role that has the PowerUserAccess managed policy attached to it. Attach a custom policy that denies access to EC2 and RDS in any AWS Region except eu-west-1.
D)	
Set up SAML-based authentication tied to an IAM role that has a PowerUserAccess managed policy and a custom policy that denies all the developers access to any AWS services except AWS Config. Within AWS Config, create a product containing only EC2 and RDS service in eu-west-1 region.
--------
A licensed legacy application is bound to a specific MAC address. However, when launching new EC2 instances, each instance can be assigned a different MAC address. What measures can you implement to ensure that your EC2 instances retain a consistent MAC address for licensing purposes?
A)	
AWS cannot have a fixed MAC address; the best solution is to create a dedicated VPN/VGW gateway to serve data from the legacy application
B)	
Create an ENI and assign it to the EC2 instance. The ENI will have a static MAC address and can be detached and reattached to a new instance if the current instance becomes unavailable
C)	
Private subnets have static MAC addresses. Launch the EC2 instance in a private subnet and, if required, use a NAT to serve data over the internet
D)	
Configure a manual MAC address for each EC2 instance and report that to the licensing company
B
-------
our company has secured a contract to develop a search engine for public legal documents. The dataset is approximately 100TB in size and is accessible at the customer's data center in various formats. A portion of the dataset is archived on tapes, while the rest is stored on disks. Some of the data is quite old, dating back nearly 15 years, and is stored in a compressed format to conserve disk space. You have been tasked by management to devise a flexible and cost-effective plan to ingest the data and make it accessible for efficient searching by the front-end application. What are the two sequential steps you would select to achieve this objective? Select two answers from the options provided.
A)	
Set up a Direct Connect connection to transfer the data from on-premise servers to the S3
B)	
Set up the Snowball Edge Storage Optimized devices to migrate the data to S3
C)	
Configure the AWS Batch to process the data from S3, send it to Kinesis Firehose, and save it to Amazon OpenSearch Service
D)	
Set up a VPN connection and transfer the data to AWS S3 over the weekend
E)
Load the data to EFS and create Auto Scaling EC2 instances to read through the data and save it into the AWS RDS for querying

----------
A team is working on a feature designed to identify celebrities. Users of the app will have the ability to upload images and search for celebrities within those images by simply pressing a button. Additionally, they can upload multiple photos to track the instances in which a specific celebrity has appeared. The team aims to deploy the app on AWS while minimizing costs. What is the most effective option to implement that maintains both availability and stability?
A)	
Implement the App in an M4 large EC2 instance with Autoscaling and Elastic Load Balancer. Build the application via a Cloudformation template. Use the App to call Rekognition API "SearchFaces" to get the information. Process the JSON result in the backend service and return the result to the frontend with a Cloudfront CDN
B)	
Create the frontend and backend in a T2 medium EC2 instance to use its burstable capability. Call Rekognition API "RecognizeCelebrities" to fetch the information in a JSON format. Process the JSON result in the backend service and return the result to the frontend UI
C)	
Develop the App in a serverless lambda to use Rekognition API "SearchFaces" to search a Celebrity. The input image can be base64-encoded bytes or an S3 object. After the API has been returned, present the result to clients
D)	
Use the AWS Rekognition service. Implement the App in a lambda to call Rekognition API "RecognizeCelebrities" to fetch the information required in a JSON format. Process the information in Lambda and return the result to end-users. Use S3 for clients to upload photos
-----------
Your organization possesses a self-managed directory within Microsoft Active Directory (AD) for overseeing employee identities. The objective now is to implement AWS IAM Identity Center (the successor to AWS Single Sign-On) for managing SSO access to AWS accounts and cloud applications in the AWS access portal. Additionally, you aim to direct directory requests to the self-managed AD without the necessity of caching information in AWS. What is the appropriate method to configure this setup?
A)	
In "AWS Identity Center > Settings > Identity source > Change identity source", select the self-managed directory and connect it to the IAM Identity Center.
B)	
Configure an Active Directory (AD) Connector in the AWS Directory Service as a directory gateway to forward directory requests. Connect IAM Identity Center to the self-managed Active Directory by using the AD Connector.
C)	
Create an AWS Managed Microsoft AD and establish two-way trust relationships between the self-managed directory and AWS Microsoft AD in the AWS IAM Identity Center.
D)	
In the AWS IAM Identity Center, configure a one-way trust relationship between AWS Microsoft AD and the self-managed directory to redirect the directory requests.
------

You are tasked with establishing network connectivity between your current data centers and AWS. It is essential for the EC2 instances of your application to connect with the existing backend resources housed in your data center. Initially, the network traffic between AWS and your data centers will be minimal, but it is expected to increase to tens of gigabytes per second over the next few months. The timely launch of your application is crucial for its success. Which design options will best enable you to achieve these goals?
A)	
Quickly submit a Direct Connect request to provision a 1 Gbps cross-connect between your data center and VPC, then increase the number or size of your Direct Connect connections as needed
B)	
Quickly create an internal ELB for your backend applications, submit a Direct Connect request to provision a 1 Gbps cross-connect between your data center and VPC, then increase the number or size of your Direct Connect connections as needed
C)	
Allocate EIPs and an Internet Gateway for your VPC instances to use for quick, temporary access to your backend applications, then provision a VPN connection between a VPC and existing on-premises equipment
D)	
Provision a VPN connection between a VPC and existing on-premises equipment, submit a Direct Connect partner request to provision cross-connects between your data center and the Direct Connect location, then cut over from the VPN connection one or more Direct Connect connections as needed
---------

As an AWS Solutions Architect, you are currently employed in a role where the company is undertaking multiple new projects within the AWS Cloud. The development team is seeking your expertise to determine the most suitable AWS database service for these projects. In which of the given scenarios would you recommend the utilization of Aurora serverless as the database service? Select two answers from the options provided.
A)	
A MySQL database for a proof-of-concept project that is idle most of the time and you want to pay on a per-second basis for the database capacity.
B)	
A Relational Database for a Java application. The peaks of the database activities are hard to predict. You want to automatically scale up and down the database without the need to manage the database capacity manually.
C)	
A high-performance in-memory data store for gaming leaderboards with microsecond latencies and caching capabilities.
D)	
A fast, flexible, and high-performance database to store key-value pairs for an eCommerce system.
E)	
A MySQL compatible database that stores application usage data with stable and predicted workload. The DB instance class should be memory optimized.
-----
The financial company has initiated a project to transition its on-premises legacy applications to AWS. The main goal of this migration is to enhance agility and enhance business continuity, leading to discussions about breaking down monolithic applications into microservices. As the solution architect hired to assist with this migration, you intend to leverage AWS serverless services for developing the microservices. What is the most suitable migration strategy for this scenario?
A)	
Rehost
B)	
Relocate
C)	
Replatform
D)	
Refactor
