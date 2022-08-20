# Kustomize 101

Introduction to Kustomize

## The Phase Folders

- phase-0 - just ordinary kubernetes yaml files

## The Basics

```sh
# Applying resources
kubectl apply -f app/deployment.yaml
kubectl apply -f app/service.yaml

## OR
kubectl apply -f app/

# ----------------------

# Deleting resources
kubectl delete -f app/deployment.yaml
kubectl delete -f app/service.yaml

## OR
kubectl delete -f app/
```
