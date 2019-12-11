
1. update package manager

   'sudo yum -y update'

2. install R

   'sudo yum install -y R

   sudo amazon-linux-extras install R3.4 '

3. install Rstudio-Server

   'wget https://download2.rstudio.org/server/centos6/x86_64/rstudio-server-rhel-1.2.5019-x86_64.rpm

   sudo yum install rstudio-server-rhel-1.2.5019-x86_64.rpm '

4. add user

    'sudo useradd yunmi

    echo yunmi:123456 |sudo chpasswd ' 

 *Use public IP address:port to access to the web