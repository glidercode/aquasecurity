# Tfsec

1.Copy the sample Terraform file [main.tf](https://github.com/glidercode/aquasecurity/blob/main/main.tf) to a scan directory

2.Pull docker image>

``` docker pull tfsec/tfsec:latest ```

3.Run a test:

``` docker run --rm -it -v "$(pwd):/src" tfsec/tfsec /src ```

> Replace `src` with the directory containing the files to scan
