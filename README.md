# Promethheus and Grafana on Kubernetes Cluster

## Repo Structure:

 ## volumes:
       - contains file graf.yml and prom.yml, which will help in launching pvc
       - ### Note:
            Here i used the Kubernetes cluster: minikube which and used local storage,
            so you can change it according to your requirements size, storage

 ## deployment: 
       - contains file graf.yml and prom.yml, which will help in launching deployments and services 
       - Prometheus on port no. 31000 and   
       - Grafana on prot no. 32000

 ## prom_config.yml:
       - this is config Map file which is used to set **prometheus.yml configuration**
       - this is currently set according t my requirements so change it

 ## kustomization.yml:
       - this help you to set up the whole setup using a single command:
              - kubectl apply -k .

## To Launch the whole setup using a single command:

Use the below command inside the repo cloned

  command:  ## kubectl apply -k .