Before begin, see https://github.com/glidercode/aquasecurity/wiki

1. Pull docker image:
``` docker pull aquasec/trivy:latest ``` 

2. Run image test. Replace `[image_name]` with the name of an image:
``` docker run --rm -v /var/run/docker.sock:/var/run/docker.sock \ -v $HOME/Library/Caches:/root/.cache/ aquasec/trivy:latest [image_name] ```
