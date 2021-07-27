# Kube Hunter

1. Install in minikube cluster:
``` minikube kubectl create -f https://raw.githubusercontent.com/aquasecurity/kube-hunter/main/job.yaml ```

2. Test the cluster:
``` minikube kubectl get all ``` 

3. See results. Replace `[pod_kubehunter_name]` with the value of your cluster:
``` minikube kubectl logs [pod_kubehunter_name] ``` 
