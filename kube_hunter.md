# Kube Hunter

1. Install in cluster:
``` kubectl create -f https://raw.githubusercontent.com/aquasecurity/kube-hunter/main/job.yaml ```

2. Test the cluster:
``` kubectl get all ``` 

3. See results. Replace `[pod_kubehunter_name]` with the value of your cluster:
``` kubectl logs [pod_kubehunter_name] ``` 
