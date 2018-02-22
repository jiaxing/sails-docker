# sails-docker

Dockerfile for the [`jaysong/sails:latest`](https://hub.docker.com/r/jaysong/gradle/)
Docker Hub image which contains Node and Sails.

## Feature:

- [node:9.5](https://hub.docker.com/_/node/)
- [Sails 1.0 beta](https://sailsjs.com/documentation/upgrading/to-v-1-0).
- The port `1337` is exposed.
- A mount point is created at `/app`.
- The working directory is set to `/app`.

## How-To:
Work with the current directory which contains a Sails app:
```
docker run -it --name sails -v $(pwd):/app jaysong/sails:latest bash
```

Start the server directly:
```
docker run -it --rm -p 1337:1337 -v $(pwd):/app jaysong/sails:latest sails lift
```
