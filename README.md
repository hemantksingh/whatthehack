# What The Hack - Intro To Kubernetes

AKS deployment manifest for completing whatthehack challenges https://github.com/gfilicetti/WhatTheHack/blob/master/001-IntroToKubernetes/README.md

## Start 

```sh

kubectl create namespace hack
```


## Rolling deploy

```sh

kubectl -n hack set image deployment/content-api content-api=whatthehackmsft/content-api:v2

```