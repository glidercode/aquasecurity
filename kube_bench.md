# Kube Bench
  
1. Install in minikube cluster:
``` minikube kubectl apply -f https://raw.githubusercontent.com/aquasecurity/kube-bench/main/job.yaml ``` 

2. Scan cluster:
``` minikube kubectl get all ``` 

3. See results. Replace `[pod_kubebench_name]` with the value of your cluster:
``` minikube kubectl logs [pod_kubebench_name] ```
