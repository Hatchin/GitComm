## Docker list containers
``` sudo docker ps -a```

## Docker stop/remove container
``` sudo docker stop <container id>```
``` sudo docker rm <container id>```

## Docker run container with ports open
``` sudo docker run -it -p <ip1>:<ip2> -p <ip3>:<ip4> --name <container name> <image name> --port=<ip> --rest_api_port=<ip> --container_config=<..>  
