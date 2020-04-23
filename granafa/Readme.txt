pkill kubectl -9

kubectl port-forward prometheus-deployment-56f854c695-5g5vz 8080:9090 -n monitoring &
kubectl port-forward grafana-8467778df4-gxjw5 3000:3000 -n monitoring &
