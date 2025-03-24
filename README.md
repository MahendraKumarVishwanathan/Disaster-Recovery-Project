
AMS: Front End - Ec2
POC : Back End - Ec2
Database: Mysql 8.1 - RDS

Highly available + Highly Sclable + Security + Cost Optimization
Calculate application running time, Occording that we can create infrastructure
Domain Specific Infrastricture
Security : SG / ACL
High Available : Multi availablity Zone
Scalable: ASG

Ec2 -> Front End (Static Files) -> Backed(Php Application) -> RDS (DC/ DR)

DC-> Mumbai
DR-> North Virgenia

Route 53 -> Once DC down Traffic move to DR

Purchase Domain from Go Daddy or Route 53 -> Server in different Zone -> Load Balancer for balance load -> Static Content in S3.

Disastor Recovery:

Stategies available to your aws, 4 different DR Statagies, low cost and low complexity of making backup to more complex stategies using multiple active regions

Active and passive stategies use an active sites in onbe region and sites to host the workloads and server trafics, The passove sites are used for recovery and that was not share trafic untill active goes down.

Backup and restore
Pilot Light
Warm Stand by
Multi-site active/active
Backup and Restore : migrating against the dataloss and corruption
Region replication : Repliocating data from one to another

S3 DR: High Availablity
As an additional disaster recovery strategy for your Amazon S3 data, enable S3 object versioning. 
Object versioning protects your data in S3 from the consequences of deletion or modification actions by retaining the original version before the action. 
 If you are using S3 replication to back up data to your DR region

S3: Security
Multi Factor Authentication: An additional layer of security that requires multi-factor authentication for changing Bucket Versioning settings and permanently deleting object versions. 

DR statagies we can select bashed on business requirement,

If the new project ariving in your company
Cloud Architech -> Collect Requirement and Make designing -> Then provisioning resources

Start Project:

Need to purchase Domain from GoDaddy -> Purchased as bootlabsmahi.shop -> The need to purchase certificate for serve https request ->

GoDaddy -> ACM or CA (Certificate Authority – Its kind of bonofied certificate) -> Aws Route 53 -> Create Hosted Zone -> Exchage Name server to GoDaddy - > RDS -> Roles -> Ec2 Instance -> User Date

Application Architect :

Data Center: From one Region We can done set up couple of Availablity Zone
https://bootlabsmahi.shop -> Route 53 (Hosted Zone  -> GoDaddy -> ) -> Load Balancer -> Ec2 (Php Application) deployment -> RDS (Applicatiom Data’s are stored in RDS)

The same we have do backup to S3 Bucket

Disastor Recovery : From another Region We can done set up couple of Availablity Zone
https://bootlabsmahi.shop -> Route 53 (Hosted Zone  -> GoDaddy -> ) -> Load Balancer -> Ec2 (Php Application) deployment -> RDS (Applicatiom Data’s are stored in RDS)
