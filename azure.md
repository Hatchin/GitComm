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
### Upload
```
az dls fs upload --account imagestore --source-path "your_local_path" --destination-path /Public/Abdomen/TCIA_MultiOrgan_dicom --thread-count 30 --verbose --overwrite
```

### List

### Other commands
https://docs.microsoft.com/en-us/cli/azure/dls/fs?view=azure-cli-latest#az-dls-fs-list


### Switch subscription
`az account set --subscription <subscription-id>`

also refer to [link](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-directory-file-acl-cli)

### Delete

Delete should be done via FileZilla.

### 
create a new instance?
An important setting

# Run
### Install Anaconda

```
cd /tmp/
curl -O https://repo.anaconda.com/archive/Anaconda3-2019.07-Linux-x86_64.sh
bash Anaconda3-2019.07-Linux-x86_64.sh
```

### Create new environment

```
conda create -n [name] python=3.5 anaconda
```

### Install requirements

```
pip install -r requirements.txt
```


### Git


## Jupyter notebook
Install jupyter notebook [link](https://github.com/rgl/azure-content/blob/master/articles/virtual-machines/virtual-machines-linux-jupyter-notebook.md)
Azure and jupyterhub [link](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-ubuntu-intro)

## nbextension
```
pip install jupyter_contrib_nbextensions
jupyter contrib nbextension install --user
jupyter nbextension enable varInspector/main
jupyter nbextension enable codefolding/main
jupyter nbextension enable collapsible_headings/main
jupyter nbextension enable toc2/main
jupyter nbextension enable <nbextension require path>/main
```
[require path name](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions.html)


## Install new version of Cuda
  - `sudo apt remove cuda`
  - visit [pre installation](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#pre-installation-actions) and check for versions
  - download the newest [cuda tookit](http://developer.nvidia.com/cuda-downloads). If other versions are prefered, visit [cuda archive](https://developer.nvidia.com/cuda-toolkit-archive) to find the specific version
  - select equipment version(OS, architecture, distribution and version) and `Installer Type` as `deb(local)`
  - download the installer file
    - e.g. `wget https://developer.nvidia.com/compute/cuda/10.0/Prod/local_installers/cuda-repo-ubuntu1804-10-0-local-10.0.130-410.48_1.0-1_amd64`
   - run the installation instructions (go check the file name of the downloaded installer file, maybe the extension `.deb` is not required)

