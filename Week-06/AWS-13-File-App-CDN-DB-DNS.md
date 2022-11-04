# AWS File, AppSevices, CDN, DNS,DB
AWS offers a variety of services related to areas like the file system (EFS), application services (ElasticBeanStalk), Content Delivery Network(CloudFront), Domain Name System (Route 53), Data Bases(RDS/Aurora). 

## Key terminologies

Elastic File System (EFS) - Is a network file system mountable on many ec2 instances simultaneously with no set up fee. It is a serverless set and forget file system which is ideal for storage classes that need high durability and availability.Suitable for big data and analytics, web serving, content management etc. 

AWS RDS - Fully managed relational data service supporting mysql, PostgreSQL, MariaDB, SQL Server etc. It  also supports set up in multi AZ for disaster recovery, vertical and horizontal scaling, EBS backed storage etc.

AWS Aurora - A fully managed relational database service which supports both mySQL and Aurora DB.It is highly available , fault tolerant and self healing storage system that has 15 low-latency read replicas, point in time recovery, continuous back up of Amazon S3 and replications across 3 AZs. It costs more than the RDS but is more efficient.


## Exercise
1. Study ElasticBeanStalk, CloudFront, Route53

2. Assignment on EFS, RDS, Aurora
 
### Sources

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Tutorials.WebServerDB.CreateVPC.html

https://aws.amazon.com/rds/aurora/

https://aws.amazon.com/elasticbeanstalk/

https://aws.amazon.com/getting-started/tutorials/create-network-file-system/?pg=ln&sec=hs

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Tutorials.html#CHAP_Tutorials.ThisGuide

https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html

https://aws.amazon.com/cloudfront/

https://aws.amazon.com/route53/

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html

https://aws.amazon.com/getting-started/hands-on/create-high-availability-database-cluster/#

https://aws.amazon.com/getting-started/hands-on/building-serverless-applications-with-amazon-aurora-serverless/

https://aws.amazon.com/getting-started/hands-on/migrate-rdsmysql-to-auroramysql/

https://docs.aws.amazon.com/efs/latest/ug/installing-amazon-efs-utils.html

https://docs.aws.amazon.com/efs/latest/ug/efs-mount-helper.html



### Overcome challenges
Had to look up on how the AWS offers services in each of the different fields like file system, caching content, resolving the domain name to ip addresses, how to manage data bases and how to deploy applications quickly to cloud.


### Results
1) The services like Elastic Beanstalk, CloudFront and Route53 were studied. 

ElasticBeanStalk - Is a PaaS service intended to deploy applications on AWS with full control over configuration. Payment is done for the underlying infrastructure. It supports many platforms like python, go, single/multi container docker. It has the health agent checks app health, publishes health events.

CloudFront - Is a CDN network.The purpose of cloudfront is to replicate the resources to the AWS edge locations and to cache the requests resulting in low latency and thus enhancing the user experience. 

Route53 - Is a DNS(DDomain Name System) service. It translates the domain names to IP addresses. It can be combined with health checking services to route the traffic to healthy resources. Its globally distributed nature makes it highly available and low latent.

2)The hands-on tutorials on EFS, RDS and Aurora were done to gain insights into those services.

a) Two ec2 instances were launched in 2 different AZs and  a security group allowing NFS and ssh protocol. An EFS file system was created in which 3 AZs were selected a the mount points. In both the  ec2 instances, the nfs-utils were installed, a directory was created and mounted. Three files were created in one instance and they were accessible in the second instance.  

S.G. of the instances
##### ![AWS-13-EFS-00](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/AWS-13/EFS/00-SGOfec1-AZ1a.PNG)

Two instances launched
##### ![AWS-13-EFS-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/AWS-13/EFS/01-LaunchTwoInstancesIn2AZs-WithNFS-SG.PNG)

3 AZs chosen for mount point targets
##### ![AWS-13-EFS-02a](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/AWS-13/EFS/02a-ChooseEFS-SGIN3AZs.PNG)

EFS created
##### ![AWS-13-EFS-02b](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/EFS/02b-EFSCreated.PNG)

Mounting and file creation in one instance
##### ![AWS-13-EFS-03a](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/EFS/03a-efs-instance01-3filesCreated.PNG)

Mounting and file accessing in second instance
##### ![AWS-13-EFS-03b](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/EFS/03b-3filesaccessibleInserver.PNG)


b) An AWS aurora was created with no-replica option. The writer instance was created in AZ-1b. A reader replica was explicitly created in AZ-1c and it was set to tier zero for fail over priority. The writer instance was failed. After a few seconds, reader and writer instance was interchanged. The replica thus became the primary instance.  

No replication option chosen
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/01-NoReplicaOptionChosen.PNG)

Writer instance created 
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/02-WriterinstanceInAZ1b.PNG)

reader instance was created
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/03-readerInstanceCreated-tierzerowassetduringcreation-AZ1aChosen.PNG)

Writer instance fail over
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/04-FailWriterInstance.PNG)

Reader and writer instances exchanged
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/05a-ReaderAndWriterInterchanged.PNG)

Logs of current reader instance 
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/05b-LogofCurrentReaderInstance.PNG)

Logs of current writer instance
##### ![AWS-13-Aurora-01](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/Aurora/05c-LogOfCurrentWriterInstance.PNG)

c)An ec2 instance was launched in the default VPC(eu-central-frankfurt) in AZ-1b. A RDS of mySQL support engine was launched in AZ-1a and security group was attached to it. A sample database name (studentdb) was specified during the launch of the RDS instance . In the security group, in the inbound rule mySQL/Aurora was chosen as the type which has default port of 3306 and in the source type custom ip was chosen and the private ip of the ec2 instance was given. The ec2 instance was accessed via mobaxterm (SSH protocol) and mySQL was installed. In the CLI, appropriate linux command was given to connect with the mySQL instance which uses the username, password and end point of the DB instance. The sample database could be seen after connecting to it and a table was created in the same database to insert some values. 

creating mySQL RDS
##### ![AWS-13-RDS-01a](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/01a-mySQL-RDS-Created.PNG)

SG of the RDS
##### ![AWS-13-RDS-01b](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/01b-SGOfmySQLRDS.PNG)

ec2 instance in the same VPC
##### ![AWS-13-RDS-01c](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/01c-ec2InSameVPC.PNG)

Installing mySQL in the ec2 instance
##### ![AWS-13-RDS-02a](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/02a-installmysql.PNG)

Displaying the studentdb and creating table
##### ![AWS-13-RDS-02b](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/02b-enteringmySQL-displayStudentdb.PNG)

inserting values into the table
##### ![AWS-13-RDS-02c](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/02c-valueInsertion.PNG)

sample query
##### ![AWS-13-RDS-02d](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-06/RDS/02d-samplequery.PNG)