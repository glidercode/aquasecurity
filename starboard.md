# Starboard

1.Install starboard plugin with krew:

``` kkubectl krew install starboard ```

More information about commands:

``` kubectl starboard help ```

3.To begin with, execute the following one-time setup command:

``` kubectl starboard init ```

The init subcommand creates the starboard namespace, in which Starboard executes Kubernetes jobs to perform scans. It also sends custom security resources definitions to the Kubernetes API:

```
kubectl api-resources --api-group aquasecurity.github.io
NAME                   SHORTNAMES    APIGROUP                 NAMESPACED   KIND
ciskubebenchreports    kubebench     aquasecurity.github.io   false        CISKubeBenchReport
configauditreports     configaudit   aquasecurity.github.io   true         ConfigAuditReport
kubehunterreports      kubehunter    aquasecurity.github.io   false        KubeHunterReport
vulnerabilityreports   vulns,vuln    aquasecurity.github.io   true         VulnerabilityReport
```

4.As an example let's run in the current namespace an old version of nginx that we know has vulnerabilities:

```kubectl create deployment nginx --image nginx:1.16```

5.Run the vulnerability scanner to generate vulnerability reports:

```starboard scan vulnerabilityreports deployment/nginx```

6.Get the latest vulnerability reports for this workload:

```starboard get vulnerabilities deployment/nginx -o yaml```

7.Once you scanned the nginx Deployment for vulnerabilities and checked its configuration you can generate an HTML report of identified risks

```
starboard get report deployment/nginx > nginx.deploy.html
open nginx.deploy.html
```
