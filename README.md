# What The Hack - Intro To Kubernetes

AKS deployment manifest for completing whatthehack challenges https://microsoft.github.io/WhatTheHack/001-IntroToKubernetes/

The exercise files can be found here https://github.com/gfilicetti/WhatTheHack/blob/master/001-IntroToKubernetes/README.md

## Start

```sh

kubectl create namespace hack
```

## Rolling deploy

```sh

kubectl -n hack set image deployment/content-api content-api=whatthehackmsft/content-api:v2

```

## Helm chart

```sh
# create the namespace outside helm using kubectl
kubectl create namespace thehack

# create helm chart
helm create langfacts

# install dry run 
helm install langfacts --dry-run --debug ./langfacts 

# upgrade app using local chart repository './' and chart 'langfacts'
helm upgrade --install langfacts --debug ./langfacts --set image.tag=v4
```
