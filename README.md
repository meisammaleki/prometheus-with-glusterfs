# prometheus-with-glusterfs
### steps to create a Prometheus instance in Kubernetes with Persistent disk.
****
You need to have a Kubernetes cluster 
You need to have a GlusterFS cluster
Link : https://github.com/meisammaleki/persistent-volume-with-GlusterFS

****

- kubectl apply -f clusterRole.yaml
- kubectl apply -f serviceAccount.yaml
- kubectl apply -f clusterRoleBinding.yaml

****

### Create a file with name prometheus.yml

cp prometheus.yml /"volume directory on main gluser server"/

### NOTE: You will need to edit this file to add more scrape configurations.
****
##### Create a persistent volume and persistent volume claim
- kubectl create -f prometheus-endpoint.yaml
- kubectl apply -f prometheus-pv-volume.yaml
- kubectl apply -f prometheus-pv-claim.yaml

****
- kubectl apply -f prometheus-deployment.yaml
- kubectl apply -f prometheus-service.yaml
  
  

  
  
