In this Given Project, I am Implementing a 3 tier aweb application over AWS service and for that the source code have been provided from aws workshop studio,
This project have been done only for personal experience and no other benefit.

Step 1 : Creation of S3 bucket for storing the Code which will be fetched later on by the Instances.

![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/44e718f4-2ac3-4176-9da9-96b03434df71)

Step 2 : Creatiion of IAM EC2 Instance Role to attach to EC2 instance.


![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/073e11ac-1829-4064-82a4-94ccab1ffa72)


Step 3 : Building out the VPC networking components as well as security groups that will add a layer of protection around our EC2 instances, Aurora databases, and Elastic Load Balancers.
- Creating VPC
![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/cc115475-740f-48b4-9e0c-0ea7de5934a6)

- Creating Subnets, Subnets are divided into 2 availibility zone.
![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/3d232bba-5da7-4f2b-b0aa-b257085fff67)

- Building Internet connectivity by IGW.
![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/8d9c51b4-d8bc-485c-ac55-938f8f4070b7)

- Creating NAT gateway, In order for our instances in the app layer private subnet to be able to access the internet they will need to go through a NAT Gateway.
![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/1be8ed28-fa25-4e02-aaf4-45cf106aa5c3)

- Routing Configuratoins
![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/f1c7e1af-ce72-4e15-84fd-d6650094d6a9)

-Creating 2 more route tables, one for each app layer private subnet in each availability zone. These route tables will route app layer traffic destined for outside the VPC to the NAT gateway in the respective availability zone

![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/5e29fa99-efab-4e27-9efc-82ce63c09a35)

- Creating Security Groups, Security group act as a firewall for EC2 instance as well as the Load balancer and allow the traffic i.e allowed inside the inbound rules.

![image](https://github.com/aepandit/AWS_Three_Tier_Application_Setup/assets/90674495/fddf0585-6c0e-4fc8-98e9-1ec8c1f1ea0f)












        


