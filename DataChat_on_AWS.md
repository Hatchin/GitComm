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

   51  ./stop_dc.sh 
   52  ./start_dc_aws.sh -c
   -c is for https connection.
