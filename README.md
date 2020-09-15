# Prometheus and Grafana on Kubernetes Cluster

## Repo Structure:

 ### volumes:
       - Contains file graf.yml and prom.yml, which will help in launching pvc
       - Note:
            Here i used the Kubernetes cluster: minikube which and used local storage,
            so you can change it according to your requirements size, storage
       - If you are using minikube as Kubernetes cluster, it will work using your local storage(in this case you may need not to cahnge anything till you have some requirements)
       - I used 2GiB of storage for both PVC, but you can change

 ### deployments: 
       - Contains file graf.yml and prom.yml, which will help in launching deployments and services 
       - Prometheus on port no. 31000 and   
       - Grafana on port no. 32000

 ### prom_config.yml:
       - This is configMap file which is used to set *prometheus.yml configuration*
       - This is currently set according to my requirements so change it and specially the targets

 ### kustomization.yml:
       - this help you to set up the whole setup using a single command:
       - command: kubectl apply -k .
       

## Requirements: 
       - Kubernetes cluster (I used minikube, but will work on any K8S cluster after the changes mentioned)
       - kubectl should be configured


## Steps to be followed
       
### First change the prom_config.yml and the files in volumes according to your requirements

### Then to Launch the whole setup use the below command inside the repo cloned

     > kubectl apply -k . 
