
# 1. create VPC
IP 10.0.0.0/16

# 2. create public subnet
IPv4 CIDR block: 10.0.1.0/24

# 3. create internate gateway
# 4. connect IGW to public subnet

# 5. create private subnet
IPv4 CIDR block:10.0.2.0/24

# 6. create NAT instance inside public subnet

# 7. AMI - Community AMI - search 'ami-00a9d4a05375b2763' - put under publiC subnet - public ip:enable 
TAG: Name, NAT Instance  -Create keypair: 'NAT_KEYPAIR'