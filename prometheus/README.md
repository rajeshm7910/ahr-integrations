# kubernetes-prometheus
Configuration files for setting up prometheus monitoring on Kubernetes cluster.


kubectl create clusterrolebinding cluster-admin-binding --clusterrole=cluster-admin --user=$(gcloud config get-value core/account)

kubectl create namespace monitoring

kubectl create -f clusterRole.yaml
kubectl create -f config-map.yaml
kubectl create  -f prometheus-deployment.yaml 

kubectl get pods --namespace=monitoring
kubectl apply -f prometheus-service.yaml
