# Podman

## basics
* `podman info`
* `podman system df` see space used

### OSX
We need podman to run QEMU vm under the hood so we have a place to run containers.

```bash
  podman machine init
  podman machine start
  podman machine stop
```

### start/stop
* `podman start name_or_hash`
* `podman stop name_or_hash`
* `podman rm name_or_hash`

### attach to an existing container
* `podman exec -i myapp bash`

### ps
* `podman ps` see running containers
* `podman ps -a` see all containers
* `podman ps -f status=exited` see exited containers using filter
* `podman ps --size` see disk space used

### to get information about the container or image
* `podman inspect name_or_hash`
* `podman inspect 680aba37fd0f | jq '.[].Config.Cmd'` get the start command from an image


## iteractive mode

open a shell inside a container

```sh
podman run -ti --rm registry.access.redhat.com/ubi8/httpd-24 bash

```
-t, --tty           Allocate a pseudo-TTY for container
-i, --interactive   Keep STDIN open even if not attached
--rm                Remove container (and pod if created) after exit


## see bound ports

```sh
podman port name_or_hash
```

## Images

### see image tree
```sh
podman image tree name_or_hash
```

### see diffs between layers
```sh
podman image diff myimage ubi8/httpd-24
```

