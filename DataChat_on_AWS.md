# Setting up for DataChat on AWS

The file describe detailed setting up process for DataChat on AWS. After launching an AWS ubuntu instance, follow the steps to set up datachat.

## Download docker-ce

[Official Instruction](https://docs.docker.com/v17.09/engine/installation/linux/docker-ce/ubuntu/)

`$ sudo apt-get remove docker docker-engine docker.io`

`$ sudo apt-get update`

`$ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common`
  
`$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

`$ sudo apt-key fingerprint 0EBFCD88` For verification

`$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) stable"`

`$ sudo apt-get update` should update again for previous new setting

`$ sudo apt-get install docker-ce`


## Manage docker as a non-root
[Official Instruction](https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user)

`$ sudo groupadd docker`

`$ sudo usermod -aG docker $USER` e.g sudo usermod -aG docker sangyu

`$ docker run hell0-world` for verification

## Install unzip

`sudo apt-get unzip`


## Set up DataChat

1. Make a datachat folder

` mkdir datachat; cd datachat`

2. Move the DataChat files from local to remote, do the .zip file

`scp -i /path/to/pem /path/to/files ubuntu@aws.address:~/datachat` do this on local bash

3. Unzip the .zip file

`unzip dc_deploy..`

4. Start datachat

`$ bash stop_dc.sh`

`$ bash purge_dc.sh`

`$ bash start_dc.sh`

To check if it runs successfully, do `docker ps`, see if there is any container running. 

## Move csv file to datachat folder

Move the fies to datachat/dc/user/data/



# New Version

1  sudo yum update
    2   sudo yum update -y
    3  sudo yum install docker
    4  sudo service docker start
    5  sudo usermod -a -G docker ec2-user
    6  sudo reboot
    7  sudo yum install -y mod_ssl
    8  ls /etc/pki/tls/private/localhost.key
    9  ls /etc/pki/tls/certs/localhost.crt
   10  docker info
   11  exit
   12  history
   13  cat /etc/pki/tls/private/localhost.key
   14  sudo cat /etc/pki/tls/private/localhost.key
   15  history
   16  sudo cat /etc/pki/tls/certs/localhost.crt
   17  hostname
   18  ls
   19  ./start_dc_aws.sh
   20  docker ps
   21  ./stop_dc.sh
   22  vim start_dc_aws.sh
   23  ./start_dc_aws.sh
   24  docker ps
   25  exit
   26  ls
   27  lks
   28  ls
   29  dc
   30  ls dc
   31  ls
   32  sudo bash stop_dc.sh
   33  sudo bash start_dc_aws.sh
   34  sudo stop_dc.sh
   35  sudo bash stop_dc.sh
   36  cd dc
   37  ls
   38  cd user_8888/
   39  ls
   40  cd credentials/
   41  ls
   42  cd ..
   43  ls
   44  cd user_8888/
   45  cd data/
   46  ls
   47  sudo ./start_dc_aws.sh
   48  cd ..
   49  ls
   50  sudo bash start_dc_aws.sh
   51  ls
   52  ./start_dc_aws.sh
   53  ls
   54  clear
   55  ls
   56  pwdd
   57  pwd
   58  clear
   59  pwd
   60  ls
   61  ssh
   62  history
