## Gloo Portal with custom Routetable and logRequestResponseInfo

This example shows how you can use custom routetables with `logRequestResponseInfo`

```
k apply -f petstore-routetable.yaml
```

```
k apply -f petstore-apiproduct-customrt.yaml
```

Create an httpbun upstream
```
glooctl create upstream -i
```

```
apiVersion: gloo.solo.io/v1
kind: Upstream
metadata:
  creationTimestamp: "2023-06-20T09:09:23Z"
  generation: 2
  name: httpbun
  namespace: gloo-system
  resourceVersion: "186761"
  uid: d2422eab-21ee-4e90-92da-f4b3c96179c7
spec:
  static:
    hosts:
    - addr: httpbun.org
      port: 443
```
