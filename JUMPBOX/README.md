
# 1. Create VPC, public subnet, and private subnet
IP 10.0.0.0/16


IPv4 CIDR block: 10.0.1.0/24
![subnet1(public)](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/Public_subnet.png)

IPv4 CIDR block:10.0.2.0/24
![subnet2(private)](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/private_subnet.png)

# 2. Internate gateway &connect it to public subnet
![IGW](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/IGW.png)



# 3. NAT instance inside public subnet
AMI - Community AMI - search 'ami-00a9d4a05375b2763' - put under publiC subnet - public ip:enable - TAG: Name NAT_Instance -Create keypair: 'NAT_KEYPAIR'

![NAT instance](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/NAT_instance.png)
 
# 4. Create Jumpbox instance
save it in public subnet - add tag - create security group - create keypair 
![JB instance](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/JB_instance.png)

NAT instance - action - networking - change source/Dest.Check - Disable 
use putty to connect to JB 
# 5. Final instance
save it in private subnet - add tag - create security group - create keypair

![Final instance](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/FINAL_INSTANCE.png)

# 6. Route table
- route table - create route table - name :private_route_JB 
private subnet -(below) Route - choose NAT instance 
![Route table_public](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/route_table_public_subnet.png)

subnet - private - edit route table association - connected 'eni'
![Route table_private](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/route_table_private_subnet.png)

# 7. Securiy group
JB: SSH,   source everwhere 
Final: SSH,  source: custom use JB security group
NAT:All traffic, source custom, use final security group
![JB SG](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/JB_SG.png)
![FINAL_SG](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/FINAL_SG.png)
![NAT_SG](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/NAT_SG.png)

# 8. Ping googl.com
Use putty to connect to JB and move JB & final instance key to JB instance using WinSCP. And then access to final instance which is insde private subnet. From final instance, ping google.com using NAT instance 

*putty IP address: ec2-user@54.174.234.204

![PING google.com](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/JB_PING.png)


