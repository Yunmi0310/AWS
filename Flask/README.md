# install Jupyter & model 

1. Launch 'first' instance(Ubuntu)

   Ubuntu 18 - storage 15 - tag Name:Jupyter ubuntu-SG:888

2. Use putty to connect

   Host name(Ubuntu@publicIP) and save

3. Install Python using conda

   go to Anaconda website and use 'copy link' of anaconda on linux 

   ` wget https://repo.anaconda.com/archive/Anaconda3-2019.10-Linux-x86_64.sh `

   ` bash Anaconda3-2019.10-Linux-x86_64.sh.1 -u `

   ` conda init `

   `jupyter notebook --ip=0.0.0.0 `

4. Replace with public IP & paste on web
  
     54.146.99.243:8891/?token=f2656234a9831ba3cbe023b49f5337eff352cb1ac8328be6

5. Create virtual env & connect to Jupyter

    ` conda create -n nameofyourenv python=3.6 `

    ` conda install nb_conda `

    ` conda activate nameofyourenv `

    ` conda install ipykernel `

    ` ipython kernel install --user --name=nameyouwanttodisplay `

6. Install git in jupyter (open terminal in jupyter)

   ` sudo apt-get install git `

7. Git clone address

   ` git clone https://github.com/leodsti/AWS_Tutorials.git `

   ` conda activate nameofyourenv `

8. Install Keras & Tensorflow

    ` pip install keras `

    ` pip install tensorflow `

# Web server  & deploy the webapp

1. Launch second instance (frontend) using Ubuntu 18

2. Install apache2  

   ` sudo apt-get update `

   ` sudo apt install apache2 `
3. Install git 

   ` sudo apt-get install git `

   ` git clone https://github.com/leodsti/AWS_Tutorials.git` 

   ` sudo mv AWS_Tutorials/MNIST/index.html /var/www/html/ `

   ` sudo mv AWS_Tutorials/MNIST/static /var/www/html/ `

copy & pase the public IP on web 

# Flask

1. Launch new instance in public subnet using Ubuntu 18 

   create backend security group 