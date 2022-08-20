# Kustomize 101

Introduction to Kustomize

## The Phase Folders

- phase-0 - just ordinary kubernetes yaml files
- phase-1 - make app folder to Kustomizable
- phase-2 - play around with ConfigMap/Secret generator
- phase-final - introduce the overlay, override ConfigMap/Secret, change image tag and increase replicas in uat overlay

## The Basics

### Apply

```sh
kubectl apply -f app/deployment.yaml
kubectl apply -f app/service.yaml

# OR

kubectl apply -f app/
```

### Delete

```sh
kubectl delete -f app/deployment.yaml
kubectl delete -f app/service.yaml

# OR

kubectl delete -f app/
```

## The Kustomize

### Build

```sh
kubectl kustomize app

# OR

kustomize build app
```

### Apply

```sh
kubectl apply -k app

# OR

kubectl kustomize app | kubectl apply -f -

# OR

kustomize build app | kubectl apply -f -
```

### Delete

```sh
kubectl delete -k app

# OR

kubectl kustomize app | kubectl delete -f -

# OR

kustomize build app | kubectl delete -f -
```
