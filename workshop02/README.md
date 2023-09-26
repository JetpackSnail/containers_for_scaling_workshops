## Running a netshoot debug pod in default namespace
```
k run debug --rm -it --image=nicolaka/netshoot -- /bin/bash
```

### Service domain name

`<service_name>.<namespace>.svc.cluster.local`