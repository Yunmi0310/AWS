# Install Rstudio server

1. Launch the instance

   Security Group: RServer uses the port 8787


2. Update package manager

   'sudo yum -y update'

3. Install R

   'sudo yum install -y R

   sudo amazon-linux-extras install R3.4 '

4. Install Rstudio-Server

   'wget https://download2.rstudio.org/server/centos6/x86_64/rstudio-server-rhel-1.2.5019-x86_64.rpm

   sudo yum install rstudio-server-rhel-1.2.5019-x86_64.rpm '

5. Add user

    'sudo useradd yunmi

    echo yunmi:123456 |sudo chpasswd ' 

 *Use 'public IP address:port number' to access to the web