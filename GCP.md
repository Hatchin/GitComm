## Tensorboard

[link](https://cs.brown.edu/courses/csci1430/proj4/gcp-guide/)


## Transfer file
```
gcloud compute scp [vm_name]:/home/jupyter/marquette/rectum/model_train_rectum3.json local/path/to/folder/.

```
### Example
Transfer file from local vm to GCP vm
Whole process:
- Download gcp [(latest version)](https://cloud.google.com/sdk/docs/quickstart)
```
curl -O https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-344.0.0-linux-x86_64.tar.gz
   73  ls
```

- Unzip the downloaded file
```
gzip -d google-cloud-sdk-344.0.0-linux-x86_64.tar.gz 
```

- Install
```
./google-cloud-sdk/install.sh
```

- Initialize
```
./google-cloud-sdk/bin/gcloud init
```

- Activate PATH
```
source ~/.bashrc
```

- Generate SSH key ( Login )
```
gcloud beta compute ssh --zone "xx" "xx"  --project "xx"
```

- Transfer file
```
gcloud compute scp --recurse [source_path] [destination_path]
gcloud compute scp --recurse source/path  gcp_vm_name:absolution/path
```

If PERMISSION ERROR:
login to GCP and run
```
chmod 777 <GCP-destination-folder-name>
```
