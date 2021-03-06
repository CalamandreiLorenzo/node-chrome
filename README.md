# Node + Chrome Docker Container

[![pipeline status](https://gitlab.com/lorenzocalamandrei/node-chrome/badges/master/pipeline.svg)](https://gitlab.com/lorenzocalamandrei/node-chrome/-/commits/master)

This repo is also mirrored on GitHub.
But GitHub is used only to deploy on DockerHub, using automated build.

- [GitHub Repo - Node Chrome Container](https://github.com/CalamandreiLorenzo/node-chrome)
- [GitLab Repo - Node Chrome Container](https://gitlab.com/lorenzocalamandrei/node-chrome)
- [Docker Hub - Node Chrome Container](https://hub.docker.com/r/lorenzocalamandrei/node-chrome)

## Requirements

- Docker

## How to run

Run this container whit the following command: 

```bash
docker container run --rm -ti -p 8000:8000 -v $(pwd):./ --user node lorenzocalamandrei/node-chrome:x-node-x bash
```

Or use it in a `docker-compose.yml` in this way:

```docker-compose
services:
    node:
        image: lorenzocalamandrei/node-chrome:1.0-node-13.8.0
        volumes:
            - ./:/home/node/app
        ...
```

*__Be careful__*, to use this image you will need to configure your project to use chrome headless.

For example, if you are dealing with a stencil application you will need to follow this guide: https://stenciljs.com/docs/end-to-end-testing#caveat-about-e2e-tests-automation-on-cd-ci

## Contributors

- Lorenzo Calamandrei <nexcal.dev@gmail.com>
