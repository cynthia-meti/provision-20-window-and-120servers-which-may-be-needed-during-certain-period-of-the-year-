# provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-

This project is aimed  at showcasing the necessary  information a solution architect  will collect from a client who wants to  start using the cloud services  and its estimated that 20 windows and 120 servers will be needed during periods of  the year. And the project is also to practically demonstrate how this servers be provision


as a solution architect ask your client like

why they want to move to the cloud , this enable you to  know their reasons and finding solution to it by designing VPC with multiple availability zone for high availability requirements and deploy application to region closer to users to reduce latency.

what kind of load balencer are you using ; this enables you to undertand the kind of workload the customers are running. and from there you get to know the kind of load balencer to use be it  ALB or another load balencer depending on the workload.

what is their backup strategy.  as a solution architect you enable a backup strategy for disaster recovery.You could enable automatic snapshort of rds backup.

 find out were they store their application configuration details. to provision a solution, you could store details in private repository or aws secret manager for storing credential

DEMONSTRATION

i just created a VPC in a region which is closer to my client to reduce latency
![created vpc](https://github.com/cynthia-meti/provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-/assets/132440521/1afe6801-662f-42c1-a1c7-ba86f2bf61c6)
 in my vpc i created six subnet; two public and four private subnet in different availability zone 
 ![created 6 subnets, 2public and 4 private](https://github.com/cynthia-meti/provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-/assets/132440521/026bbe04-b16b-4544-9018-f903cd5ad351)
Creat internet gateway and attach it to vpc.It allows communication between the VPC and the internet  
![succesfully attached my IGW to my VPC](https://github.com/cynthia-meti/provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-/assets/132440521/4e8d9d9a-8cad-46bb-8a54-2b6674e23040)
create RTB ; Every vpc comes with a default route. the route table contains rules determining how network traffic will be directed within the vpc
.Bellow is the image of a public routable which is associated to an internet gateway.The public route table allows access from the public internet to the public subnets
![succesfully attached my IGW to my VPC](https://github.com/cynthia-meti/provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-/assets/132440521/6fdae2c5-387a-4e04-b80d-e7559d5e706a)
 ![updated public route and its been associted to the IGW](https://github.com/cynthia-meti/provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-/assets/132440521/2a26a8d7-b471-499e-9a9c-98c79b6b1007
I created a private subnet route table which is not connected  to the IGW. This implies that resources in the private subnet can not communicate with the internet
![private route table created](https://github.com/cynthia-meti/provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-/assets/132440521/f23fb51d-b7f7-4e52-be67-04a1329c9f00)
