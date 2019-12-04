# Part 1. 
# Open '.py' script in virtual space

1. Launch instance (using Ubuntu)

    . Ubuntu Server 18.04 LTS (HVM), SSD Volume Type

    . public IP 54.159.96.117
    
    . host name:     ubuntu@ec2-34-201-50-214.compute-1.amazonaws.com
    
    . use putty and wcp to connect to instance 

2. write script in text file and save it as name.py

3. install python 

    ` python3 `


4. open it in python distant space(python3 filename.py)

   `python3 name.py`  

    
5. install pip

    * update first before install 
    * sudo means admin 
    * yum is not working in ubundtu 

   `sudo apt-get update -y `

   `sudo apt-get install python3-pip`

6. install jupyter 

   `sudo pip3 install jupyter`

    `jupyter notebook --ip=0.0.0.0`

   *  if we put 'local host:port' in cmd it is going to specific IP (looping) so should put 'every IP possible' in front of jupyter noteboook (ip=0.0.0.0) 

7. adjust security group 


  Type           | Protocol | Port range |Source
  ---------------|----------|------------|--------
  Custom TCP rule|TCP       |8888        |everywhere 





. copy & paste 34.201.50.214:8888/?token=cd2c94afac7efb1d179cd90fdf015e6674c67983e284ee08

.public_IP:8888/?token=cd2c94afac7efb1d179cd90fdf015e6674c67983e284ee08

. copy & paste URL on the browser and open 

. prevent jupyter from being closed when terminal is closed (make terminal to be blocked by jupyter)

` nohup jupyter notebook --ip=0.0.0.0 & `


. to stop it  
 ` jupyter notebook stop `

. to display file in cmd

` cat nohup.out `

 

# Part 2. 
# Create virtual environment & link to jupyter 


1. Use pew - pew creates different folder(virtual environment)

 ` pip3 install pew` 

. pew creates different folder(virtual environment)

` pew new yunmipew `

. to exit

` exit `  

. to go back to yunmipew


` pew workon yunmipew`


. to check current virtual environment

` pew ls `

. to list everthing

` pip3 freeze `

. to install pandas

` pip3 install pandas ` 
 
1.2 Link to jupyter 

`pip3 install ipykernel `

` python3 -m ipykernel install --user --name=Yunmi `

. to store everything in txt file instead of listing

` pip3 freeze > myEnv.txt `

. to remove environment

` pew rm yunmi `

` exit `

. create new environmnet

 ` pew new yunmi2 `

 ` pip3 install -r myEnv.txt `

`python3 -m ipykernel install --user=yunmi2`

2 . Use conda

. make new directory


`mkdir tmp`

`cd tmp/`

.go to Anaconda website and copy the link of one of installer 

`curl -O https://repo.anaconda.com/archive/Anaconda3-2019.03-Linux-x86_64.sh`

. check with 'ls'

`bash Anaconda3-2019.03-Linux-x86_64.sh`

`conda create -n yunmi2`

`conda create -n yunmi2 python=3.7`

`conda activate yunmi2`

`pip3 install --user ipykernel`


`python -m ipykernel install --user --name=yunmi2`

. in order to remove virutal environment

`conda env remove -n yunmi2`


