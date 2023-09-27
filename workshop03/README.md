#

## Create a namespace
```
k apply -f namespaces.yaml
```

## Create configmaps and secrets
```
k apply -f configs.yaml
```

## Create volumes and volume claim
```
k apply -f volumes.yaml
```

## Create backend
```
k apply -f deploy.yaml
```

## Create ingress
```
k apply -f ingress.yaml
```

### To test the container
```
k port-forward svc/codeserver-svc 3000:8443 -ncodeserver
```




### Encoding password to base64
```
echo -n <password> | base64
```