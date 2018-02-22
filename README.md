# sails-docker

Dockerfile for the [`jaysong/sails:9.5-beta`](https://hub.docker.com/r/jaysong/gradle/)
Docker Hub image which contains Node and Sails.

## Feature:

- [node:9.5](https://hub.docker.com/_/node/)
- [Sails 1.0 beta](https://sailsjs.com/documentation/upgrading/to-v-1-0).
- Expose the port `1337`.
- Create a mount point at `/app`.
- Set the working directory to `/app`.

## How-To:
Work with the current directory which contains a Sails app:
```
docker run -it --name sails -p 1337:1337 -v $(pwd):/app jaysong/sails:9.5-beta bash
```

Run a sails command directly:
```
docker run -it --rm -p 1337:1337 -v $(pwd):/app jaysong/sails:9.5-beta sails lift
```
