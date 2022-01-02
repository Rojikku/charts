# rclone helm chart

The health checks look for a file named "health" in the root of what is mounted. Please create such a file in order for it to pass health checks.

## Configuration

The following tables lists the configurable parameters of the rclone chart and their default values.

| Parameter                  | Description                         | Default                                                 |
|----------------------------|-------------------------------------|---------------------------------------------------------|
| `images.initContainer.repository`         | Image init container repository | `busybox` |
| `images.initContainer.tag`         | Image init container tag | `latest` |
| `images.container.repository`         | Image repository | `rclone/rclone` |
| `images.container.tag`                | Image tag. Possible values listed [here](https://hub.docker.com/r/rclone/rclone/tags).| `1.57.0`|
| `images.pullPolicy`         | Image pull policy | `IfNotPresent` |
| `rclone.remote`         | rclone remote to use based in rclone config | `drive:` |
| `rclone.path`         | rclone remote path to mount | `/mnt/rclone` |
| `rclone.readOnly`         | rclone read only file system | `false` |
| `rclone.additionalArgs`         | rclone additional arguments to pass for mount options | `See values.yaml` |
| `nodeSelector`             | Node labels for pod assignment | `` |
| `resources`                | CPU/Memory resource requests/limits | `{}` |

Read through the [values.yaml](values.yaml) file. It has several commented out suggested values.
