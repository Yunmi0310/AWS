# open '.py' script in virtual space

1. Launch instance (using Ubuntu)

  . Ubuntu Server 18.04 LTS (HVM), SSD Volume Type

  . public IP 54.159.96.117
  . host name: ubuntu@ec2-34-201-50-214.compute-1.amazonaws.com
  . use putty and wcp to connect to instance 

2. write script in text file and save it name.py

3. install python 

.  code python3 name.py
exit()

4. open it in python distant space(python3 filename.py)

. code : python3 name.py  

* sudo means admmin 
* yum is not working in ubundtu 

5. install pip

*update first before install 

.  code : sudo apt-get update -y

sudo apt-get install python3-pip

6. install jupyter 

. code: sudo pip3 install jupyter

jupyter notebook --ip=0.0.0.0

*if put 'local host:port' it is going to specific ip (looping) so put every IP possible in front of jupyter noteboook 

7. security group 'Custom TCP rule, port range:8888, source:everywhere'
paste 34.201.50.214:8888/?token=cd2c94afac7efb1d179cd90fdf015e6674c67983e284ee08
public_IP+8888/?token=cd2c94afac7efb1d179cd90fdf015e6674c67983e284ee08

. copy paste URL and open 

* prevent jupyter from being closed when terminal is closed (terminal is blocked by jupyter)

. code: nohub jupyter notebook --ip=0.0.0.0 &
* to stop it  
code : jupyter notebook stop

. cat nohup.out

*cat:display file in cmd 