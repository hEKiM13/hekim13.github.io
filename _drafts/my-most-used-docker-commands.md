# My most used Docker commands

## Build

| Command | Description |
| ------- | ----------- |
| `docker build -t <image-name>:<tag> .` | Build, name and tag a Docker image and supply the current directory as the build context |

## Run

| Command | Description |
| ------- | ----------- |
| `docker run -d --rm -p <host-port>:<container-port> --name <container-name> <image-name>` | Run a detached `-d` container of the image `<image-name>` and name it `<container-name>`. Expose ports and remove it when the main process ends |
