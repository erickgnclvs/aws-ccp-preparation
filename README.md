# AWS Certified Practioner Exam - preparation
``test date: September 13th``

### TODO: 
* Run system check - [Person OnVUE](https://wsr.pearsonvue.com/testtaker/registration/ExamRegistrationDetailPage/AWS?previousPage=previousToDashboard&clientCode=AWS&conversationId=878817&regId=456667563)
  
### Links:
* [AWS Certification page](https://aws.amazon.com/pt/certification/certified-cloud-practitioner/)
* [AWS CCP Exam Guide](https://d1.awsstatic.com/pt_BR/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf)
* [AWS Training](https://www.aws.training/)
* [AWS Skill Builder](https://explore.skillbuilder.aws/pages/16/learner-dashboard)
* [My Exam Guide](EXAMGUIDE.md)
* [AWS in Plain English](https://expeditedsecurity.com/aws-in-plain-english/)
* [13h of video about AWS CCP](https://www.exampro.co/clf-c01)
* [Flashcards](https://www.brainscape.com/l/dashboard/aws-ccp-12178727/decks)

# Study notes:

## Domain 1: Cloud concepts
### 6 advantages of Cloud Computing
* Trade fixed expense for variable expense
* Benefit from massive economies of scale
* Stop guessing capacity
* Increase speed and agility 
* Stop spending money running and maintaining data centers
* Go global in minutes

### 3 Cloud Computing models (SIP)
* SaaS
* IaaS
* PaaS

### 3 Cloud Computing deployments (PHO)
* Private cloud
* Hybrid cloud
* Online cloud

### 6 Pillars of a Well-Architected Framework (CROPSS)
* Cost optimization
* Reliability
* Operational excellence
* Performance efficiency
* Security
* Sustainability

## Domain 2: Security
### Shared responsibility model
* User responsibility: Security **IN** the Cloud
    * Security patchs
    * Proper permissions
* AWS responsibility: Security **OF** the Cloud
    * Securing physical hardware

### Security pillar of Well-Architected Framework
* IAM
* Detective controls
* Infrastructure protection
* Data protection
* Incident response

### Principle of least privilege
* Only provide necessary access to perform
* No more or no less than optimal level of access
* Use Identity and Access Management for defining roles

### Compliance concepts
* Know where to find compliance programs
* [aws.amazon.com/compliance](https://aws.amazon.com/compliance)
  
### Security services
#### Identity and Access Management - **IAM**
  * Free
  * Manage access to services and resources with granular permission sets
  * Set access permissions for users or other services to a resource
  * Create and manage IAM roles with specific permission sets
  * Don't manage permissions manually, avoid inconsistencies
  * Use identity federation for existing users in non-AWS services
    
#### Web Application Firewall - **WAF**
  * Firewall for web applications
  * Protects from common web exploits thus can protect AWS usage bill
  * Improve traffic visibility
  * Can be deployed in minutes
    
#### AWS Shield
  * Detection and automatic mitigation against DDoS attack
  * Standard tier:
    * Free and automatic
    * Protects agains majority DDoS attacks   
  * Advanced tier:
    * 24/7 access to AWS DDoS response team
    * Detects and mitigates sophisticated DDoS attacks
    * Financial protection against DDoS-related resource usages
       
#### Amazon Inspector
  * Automated security assessment
  * Automatically assesses apps for exposure, vulnerabilities and derivation from best practices
  * Generate detailed reports
  * Define standards or use AWS standards
     
#### AWS Trusted Advisor
  * Guides provisioning to align with AWS best practices
  * Advises how your infrastructure is or is not following AWS best practices in 5 categories:
    * Optimization
    * Performance
    * Security
    * Fault tolerance
    * Service limits
  * Recommends how to follow the best practices
  * 7 core Trusted Advisor checks are free
  * Full Trusted Advisor checks are free with Business Support plans and above

#### Amazon GuardDuty
  * Threat detection service that monitors malicious or unauthorized behaviour 24/7
  * Identifies and prioritizes potential threats
  * Quick to deploy
 
## Domain 3: Technology

### Methods of deploying and operating in the AWS Cloud
* AWS Management Console
  * GUI that supports most AWS services
  * User-friendly  
* AWS CLI
  * Access AWS via the command line 
  * Can create scripts
* AWS Software Development Kits
  * Use programming languages to deploy
    
### AWS global infrastructure
* Availability Zones (AZs)
  * AWS data centers around the world
  * Independent from each other
  * About 102 AZs currently
* Region
  * The closer the smaller latency 
  * 2 or more AZs
  * Currently 32 regions
* High availability
  * Duplicate copies in multiple regions or availability zones
  * Resiliency: Ability to provide uninterrupted performance, even during natural disasters
  * Redundancy: Having multiple copies of data in different data centers
  * TIP: Architect your AWS Cloud infrastructure to protect against downtimes caused by natural disasters or power outages
    
### Core services
#### Compute
* Amazon Elastic Compute Cloud - **EC2** (IaaS)
  * Virtual server running on AWS
  * Configure CPU, RAM, storage and network speed
  * Only charged for what you use
  * Deploy extremely scalable and reliable virtual servers in minutes
    
* Elastic Beanstalk (PaaS / Infrastructure as Code)
  * Handles the deployment process
  * Acomodate services using Java, .NET, PHP, Node.js, Python, Ruby, Go and Docker
  * You can retain control over resources ar all times
  * Free to use
  * Pay only for other AWS resources consumed to deploy
  * Automatic scales up and down
  * Freedom to select AWS resources
  * You can get manual access back whenever needed
  * Provisions and operates infrastructure
    
* Elastic Load Balancing
  * Automatically distributes incoming traffic across servers to avoid overloading
  * Fault tolerant
  * Scalable and secure
  * Monitor health of servers
 
* Lambda (Infrastructure as Code)
  * Runs code in response to an event
  * Automatically runs uploaded code and scales applications
  * Pay only for the time the code is running and each event trigger 
  * No need to provision and maintain servers - serverless code

* Lightsail
  * Simple workloads and quick deployments
  * Pre-configured and ready-to-use OS, web apps and development stacks
  * Scalable
  * Cost-effective monthly fees
  * One-click-to-launch services
  * Examples: Ubuntu, Windows, Wordpress, Node.js


> Infrastructure as Code:
> * Write code that deploys AWS services
> * Elastic Beanstalk, Lambda, CloudFormation

#### Storage
* AWS S3
  * Store each file as an entity (object)
  * High availability, security, performance and scalability
  * 99,9999999% durable (0,0000001% of chance of corrupting data)
  * Upload files (objects) from 0 byte to 5 terabytes 
  * Use for website files, mobile apps, backup, archiving, enterprise applications, IoT, big data analytics
  * Easy-to-use management features to fine-tune access controls
  * Storage classes:
    1. Standard
    2. Intelligent-Tiering
    3. Standard-Infrequent Access
    4. One Zone-Infrequent Access
    5. Glacier
    6. Glacier Deep Archive

* Elastic Block Store (**EBS**)
  * Use if need more storage for EC2's without rebooting 
  * Raw, unformatted block device attached to an EC2 instance
  * Can add multiple EBS volumes to one EC2 instance
  * Use on EC2 as file systems or hard drives
  * Dynamically change configurations to attached volumes via management console
  * Automatically replicated within its availability zone
  * Different types for needs and budgets
  * Persistent volumes: don't disappear after EC2 reboot
  * Can be encrypted
  * Exist independently of EC2 so can be moved around like an HD

* AWS Snowball
  * Upload big data to AWS
  * Data migration tool - they send you a huge data traveler and you send them back
  * Physical device
  * Transfer up to 50 terabytes with a Snowball
  * And up to 100 petabytes with a Snowmobile (it's a truck!!!!)
  * Free for 10days of onsite usage with extra fees for extra days
  * Service fee starts at $200 dollars
  * Pay for S3 storage, but not transfer fee
  * Snowmobile: fucking expensive

* AWS Storage Gateway
  * Hybrid storage solution
  * Connect S3 storage to local network storage through a VM
  * Low latency data transfer
  * Files stored as objects in S3
  * 3 types of storage solutions:
    * File Gateway
      * Stored as objects in S3 (files)
      * One-to-one representation of each file
      * Updates S3 objects
      * Local cache provided to acces recent files with low latency

    * Volume Gateway 
      * Stores files as blocks (just like hard drives)
      * Backed up as point-in-time snapshots and stored as EBS snapshots
      * 2 types:
        * Stored volume: complete copy on-premises, sends snapshots to AWS
        * Cached volume: keeps most recently accessed data on-premises, complete copy on AWS
      
    * Tape Gateway
      * Use existing tape-based backup infrastructure to back up to virtual tapes
      * Data stored locally then uploaded to S3
      * Data can be archived using Amazon Glacier
      * Pay for storage and to access stored data
      * The quicker you can access the data, the more expensive the solution
      * Example: data stored via tape gateway is cheaper saved to S3 Glacier Deep Archive than S3 Glacier (because you can wait more if it's on Deep Archive)
     
       
#### Database
* DynamoDB
  * NoSQL database
  * Secure, scalable, fast, flexible
  * Serverless: dont need to provision nor manage servers
  * Virtually unlimited storage
  * Automatically scales tables up and down
  * Pay for specific worload or pay for what you use

* RDS
  * Relational Database System
  * Only pay for what you use or reserve at on-deman pricing - cheaper
  * AWS takes care of provisioning monitoring and maintaining
  * Highly scalable
  * Compatible with Postgres, MySQL, MariaDB, Oracle, SQL Server, Aurora
  * Existing databases can be migrated with AWS Database Migration Tool

* Aurora
  * **SQL** database managed by AWS RDS
  * One of the RDBS supported by AWS RDS
  * No administration or provisioning necessary
  * Monitorable through AWS alerting services
  * MySQL and PostgreSQL compatible, but **faster** and **cheaper**
  * Database can auto scale up to 64TB per instance
  * Hosted on distributed, fault tolerant, self healing storage systems with low latency
  * Existing databases can be migrated with AWS Database Migration Service

* Redshift
  * Fully managed, petabyte-scale **data warehouse** service
  * Super cheap, super fast
  * Pay only for what you use
  * Fully integrated with your data lakes
  * Deploy new data warehouses in minutes
  * Secure
  * Data encryption on compliance with many compliance programs

#### Network and content delivery
* Amazon Virtual Private Cloud - **VPC**
  * Isolated section in the cloud to provision resources
  * Flexible and secure
  * Allow control over almost every aspect of your virtual network
  * Automatically provisioned at AWS account signup
  * Auto configured subnets, IP ranges, route tables and security groups
  * VPC is like home network where the ISP is AWS and devices are AWS services

* CloudFront
  * Content Delivery Network - CDN  
  * Make things faster
  * Deliveries websites and applications fast
  * Uses closest server to give the files for example cached data
  * Scalable
  * Automatically provisioned and managed
  * No minimum commitment
  * Pay as you go

* Route 53
  * Domain picker
  * Connects user requests to infrastructure running on AWS
  * Routes users to infrastructures outside of AWS like a DNS service
  * Integrated with other AWS services like EC2 instances or S3 buckets
  * Simple to set up, fast, secure, and cost-effective
  * Charged for only what you use
  * Automatically scale to handle large query volumes
  * Domain registration
  * Domain name system - DNS
  * Health check of web apps
  * Auto Naming for service discovery
  * Create websites/apps with high availability

#### Management tools
* CloudFormation
  * Recipe to build infrastructure
  * Templates to deploy in AWS
  * Free to use
  * Pay for the resources only
  * Provision multi-region multi-tier quick
  * Through JSON or YAML files (Infrastructure as Code)
  * Update or manage the templates (stacks) through AWS Console, CLI or SDK
  * Version control available

* CloudTrail
  * Logs user activity and API usage
  * Compliance and security
  * Provide Event history
  * Discovery/troubleshoot security and operational issues
  * Provide visibility into user/resource activities
  * Automatically respond to security threats
  * Track actions taken through Console, SDK or CLI
  * Deliver reports to S3 buckets or CloudWatch logs and events
  * Free review of account activities for the past 90 days
  * Logging of data events have small fees

* CloudWatch
  * Monitoring and management system
  * Natively integrated with most AWS services
  * Gain system visibility into resource utilization, app performance and operational health
  * Get notification in real time on data, metrics and events
  * Pay only for what you use, no upfront commitment
  * Set alerts and automatically make changes using preconfigured triggers

## Domain 4: Billing and Pricing
### Billing concepts
#### Billing and Cost Management Dashboard
  * Estimate and plan your AWS costs
  * Consolidated billing: simple accounting for multiple AWS accounts
  * Alert when you're nearing usage thresholds
  * Cost explorer - view as graphs
  * Forecast based on historical usage data
  * Generate billing reports by time, date, tags
   
### Types of charges
#### Pay-as-you-go Model of Cloud Computing
  * No huge upfront costs
  * Billed only for the consumed resources
  * Easily scale up or down

#### Fundamental Drivers of Cost
  * Compute
    * Pay hourly from launch to termination
    * EC2 - pay for time server is running
      
  * Storage
    * Pay per GB of storage used
    * S3 - upload photos and pay for storage used
      
  * Outbound data trasnfer
    * Pay to transfer data out of AWS
    * Usually no charge for data into AWS or transfering between AWS services
   
* Pricing Model Example: Storage Types (S3)
  * Standard storage - $0.023 per GB
  * Glacier storage - $0.004 per GB
  * Glacier Deep Archive storage - $0.00099 per GB

* Pricing Model Example: Data Input/Output (Aurora)
  *  Data in/Data out - $0.20 per 1 million requests

### Consolidated billing
#### AWS Consolidated Billing
* Create a payer account to view and pay combined billing charges from linked accounts in an organization
* Independent, but can't use any other services
* Cannot deploy services into the linked accounts
* All resource usage becomes consolidated as usage from one large entity - may be eligible for volume discounts
* Free

### Cost calculators
* How much does it cost?
#### AWS Total Cost of Ownership (TCO) Calculator
* Get reports on estimated savings from moving on-premises IT infrastructure onto AWS Cloud
* Total Cost of Ownership includes upfront hardware/infrastructure costs and maintenance costs
* TCO can be reduced by moving to the cloud because no upfront infrastructe purchases

#### AWS Pricing Calculator
* Estimate cost of a cloud architecture solution you want to build
* Add services to the calculater to get a report of estimated costs per service, service group and infrastructure
* Compare service costs per region, reduce EC2 spend, find right EC2 instance to fit your needs, or estimate overall AWS cloud spend

#### AWS Cost Explorer - part of Billing and Cost Management Console
* View and analise usage
* Get recommendations on how to spend less
* Predict how much you are going to spend

### AWS Free Tier
* Always free
  * Always free, like DynamoDB with 25gb of storage or Lambda with 1 million requests

* 12 months
  * 12 months free, like EC2 750 hours or Amazon S3 5gb

* Trials
  * Short term trial offers
    
### Support Plans

