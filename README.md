# AWS-Task-2
Set up a VPC with an Internet gateway, create a public subnet with 256 IP addresses, a private subnet with 256 IP addresses, make a route table connecting the Internet gateway and the subnets, and launch a Linux EC2 instance by using the above VPC and public subnet.
AWS Task-2

Task Description:

Set up a VPC with an Internet gateway, create a public subnet with 256 IP addresses, a private subnet with 256 IP addresses, make a route table connecting the Internet gateway and the subnets, and launch a Linux EC2 instance by using the above VPC and public subnet.

Solution :
Created a VPC
Name: MyVPC 
 IPv4 CIDR: 10.0.0.0/16

 <img width="940" height="419" alt="image" src="https://github.com/user-attachments/assets/2740b2d9-5fd9-44e2-bf40-4da20d4d3b44" />


Created Subnets : Public and private CIDR: 10.0.1.0/24

 
<img width="940" height="326" alt="image" src="https://github.com/user-attachments/assets/a4e98578-31e8-48f4-b28e-11b2fdcfcbd0" />



Created Internet Gateway attached to VPC
<img width="929" height="270" alt="image" src="https://github.com/user-attachments/assets/9c160129-6d84-4a81-8871-9ab9933bf40e" />

 

Create Route Table 
Destination: 0.0.0.0/0 
Target: Internet Gateway

 <img width="940" height="273" alt="image" src="https://github.com/user-attachments/assets/f00d3be7-ad36-403f-8db4-64988ffcfc6b" />


Subnet associations : publicsubnet

 
<img width="940" height="335" alt="image" src="https://github.com/user-attachments/assets/05b9ce3f-7fed-43b8-a599-c938c6d6de81" />





Enabled Auto Public IP in Public subnet
 <img width="940" height="416" alt="image" src="https://github.com/user-attachments/assets/7c099a46-d2c8-4699-b078-83c2f92fccc8" />


Launched EC2 Instance : chose keypair .pem and network settings to MyVPC public subnet and allowed SSH port 22 my IP and HTTP port 80 to anywhere

 
 <img width="940" height="423" alt="image" src="https://github.com/user-attachments/assets/bc74bd87-b85f-4b7e-b8f6-81f682e41333" />
<img width="940" height="281" alt="image" src="https://github.com/user-attachments/assets/268574fa-1e6e-485a-8bd8-71486e21fdaf" />






Connected to EC2 from local machine using .pem key and SSH connection built using public ip of EC2

 <img width="935" height="480" alt="image" src="https://github.com/user-attachments/assets/60e8dd64-9446-4694-8ee3-f2a94433871a" />


Accessed the internet to download and install a web server 

 <img width="942" height="300" alt="image" src="https://github.com/user-attachments/assets/bef07954-d32e-4f4f-a977-e27d74465a9e" />

 <img width="1090" height="583" alt="image" src="https://github.com/user-attachments/assets/d40fe10e-129c-4585-9606-84c7e4dbd2b8" />

 




