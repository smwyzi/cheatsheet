##### get pod name
```
kubectl -n default get pod -l app=${APP} -o 'jsonpath={.items[0].metadata.name}'
```