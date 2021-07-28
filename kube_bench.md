# Kube Bench
  
1.Install in cluster:

``` kubectl apply -f https://raw.githubusercontent.com/aquasecurity/kube-bench/main/job.yaml ```

2.Scan the complete cluster:

``` kubectl get all ```

3.See results:

``` kubectl logs [pod_kubebench_name] ```

> Replace `[pod_kubebench_name]` with the value of your cluster.
