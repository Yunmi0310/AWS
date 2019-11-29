
#  - create VPC
IP 10.0.0.0/16

#  - create public subnet
IPv4 CIDR block: 10.0.1.0/24
![Image of VPC](https://github.com/Yunmi0310/AWS/blob/master/JUMPBOX/pictures/Public_subnet.png)
# - create internate gateway
# 4. connect IGW to public subnet

# - create private subnet
IPv4 CIDR block:10.0.2.0/24

# 6. create NAT instance inside public subnet

# 7. AMI - Community AMI - search 'ami-00a9d4a05375b2763' - put under publiC subnet - public ip:enable 
TAG: Name, NAT Instance  -Create keypair: 'NAT_KEYPAIR'