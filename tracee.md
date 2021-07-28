# Tracee

1.Pull docker image:

``` docker pull aquasec/tracee:latest ```

2.Run OS monitoring:

``` docker run --name tracee --rm --privileged -v /lib/modules/:/lib/modules/:ro -v /usr/src:/usr/src:ro -v /tmp/tracee:/tmp/tracee -it aquasec tracee:latest ```
