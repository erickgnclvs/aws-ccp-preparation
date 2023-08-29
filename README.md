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

### AWS global infrastructure

### Resources for technology support

### Core services
#### Compute
* Amazon Elastic Compute Cloud - **EC2** (IaaS)
  * Virtual server running on AWS
  * Configure CPU, RAM, storage and network speed
  * Only charged for what you use
  * Deploy extremely scalable and reliable virtual servers in minutes 
* Elastic Beanstalk (PaaS)
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
 
* Lambda
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
 
  
#### Storage
* 
*

#### Database
*
*

#### Network and content delivery
*
*

#### Management tools
*
*
