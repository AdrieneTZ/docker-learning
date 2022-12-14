#### Basic Cli
- `docker ps`: shows the running containers by default
- `docker ps -a | grep "container_name"`: find the running containers by name
- `docker stop "container"`: stops the container
- `docker rm "container"`: removes the container(s), this cli can remove mutiple containers at the same time
- `docker rmi "image"`: remove a docker image
- `docker build -t "image_name:tag(version)"`: builds an image
- `docker`

#### Options
- `-a`, `--all`
- `-d`, `--detach`
- `-t`, `--tag`: name and optionally a tag in the `name:tag(version)` format

#### Some notes
- tag:
  - like name and assign a version to the packaged image
  - each tag of an image has it own Dockerfile


- every image is based on another image
- Why I can build an image based on node:16-alpine, and as I use cli `docker images`, there is no image called `node`?

- What is "alpine"?

- `RUN` V.S. `CMD`
