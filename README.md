# provision-20-window-and-120servers-which-may-be-needed-during-certain-period-of-the-year-

This project is aimed  at showcasing the necessary  information a solution architect  will collect from a client who wants to  start using the cloud services  and its estimated that 20 windows and 120 servers will be needed during periods of  the year. And the project is also to practically demonstrate how this servers be provision


as a solution architect ask your client like

why they want to move to the cloud , this enable you to  know their reasons and finding solution to it by designing VPC with multiple availability zone for high availability requirements and deploy application to region closer to users to reduce latency.

what kind of load balencer are you using ; this enables you to undertand the kind of workload the customers are running. and from there you get to know the kind of load balencer to use be it  ALB or another load balencer depending on the workload.

what is their backup strategy.  as a solution architect you enable a backup strategy for disaster recovery.You could enable automatic snapshort of rds backup.

 find out were they store their application configuration details. to provision a solution, you could store details in private repository or aws secret manager for storing credential

DEMONSTRATION

create a VPC
