# Docker image for ensime-node/ensime-atom CI
[![Build Status](https://drone.gitlab.woodenstake.se/api/badges/hedefalk/ensime-atom-docker/status.svg)](https://drone.gitlab.woodenstake.se/hedefalk/ensime-atom-docker)

To generate secret 

drone -s https://drone.gitlab.woodenstake.se -t __TOKEN__ secure --repo hedefalk/ensime-atom-docker --in ../drone-secrets/secrets.yml --out .drone.sec

First build:
```
docker build -t ensime/ensime-atom-ci .
docker login -u woodenstake -e hedefalk@gmail.com https://docker.woodenstake.se
docker tag ensime/ensime-atom-ci docker.woodenstake.se/ensime/ensime-atom-ci
docker push docker.woodenstake.se/ensime/ensime-atom-ci
```
