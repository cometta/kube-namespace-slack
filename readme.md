This is a customization implementation of https://github.com/wongnai/kube-slack which needs a cluster role service account to work. This implementation is suitable for a developer that does not have an admin K8s account. Can only monitor per namespace for pods failure.

### How to deploy to a namespace
edit deployment.yaml change value for SLACK_URL, KUBE_NAMESPACES_ONLY, SLACK_USERNAME and SLACK_CHANNEL
```
kubectl apply -f deployment.yaml --namespace <the_namespace>
```

### Test
```
kubectl apply -f test.yaml --namespace <the_namespace>
```

