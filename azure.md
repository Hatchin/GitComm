# Get Started

### Connect to Azure Instance

Create an instance, set the username and password, then (in Linux)
```
ssh [username]@public.ip.address
``` 
Then enter the password.

# Mount Data

### Mount Data from Local Machine
#### Upload Data to Online Driver
`File` -> `Site Manager` -> `New Site` enter the url

Select `password` mode and set username. Then connect and upload local file to online storage through FileZilla

#### Download Data to Virtual Machine
run 
```
sudo mkdir /mnt/data/
sudo mount -t cifs [url] /mnt/data -o [credentials]
```

or 
```
nano mount_data.sh
```
Then copy and paste. Then `CTRL + o` and `CTRL + x`

Change the mode
```
chmod +x mount_data.sh
```

### Mount Data from DataLake

Install Azure CIL in Linux

```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

Login

```
az login
```

Then run

```
az dls fs download --account [foldername] --source-path [target folder address within the foldername] --destination-path . --thread-count [# of example]
```

```
az dls fs download --account imagestore --source-path /Public/Abdomen/MICCAI_Challenge/label --destination-path . --thread-count 30
```

### Delete

Delete should be done via FileZilla.

### 
create a new instance?
An important setting


# Install Anaconda

```
cd /tmp/
curl -O https://repo.anaconda.com/archive/Anaconda3-2019.07-Linux-x86_64.sh
bash Anaconda3-2019.07-Linux-x86_64.sh
```
