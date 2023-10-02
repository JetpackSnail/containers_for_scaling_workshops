#

## Create a namespace
```
k apply -f namespaces.yaml
```

## Create configmaps and secrets
```
k apply -f configs.yaml
```

## Create backend
```
k apply -f deploy.yaml
```

## Create ingress
```
k apply -f ingress.yaml
```
