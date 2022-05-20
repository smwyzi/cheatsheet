#### get pod name
```
kubectl -n default get pod -l app=${APP} -o 'jsonpath={.items[0].metadata.name}'
```

#### 强制删除无法删除的 ns
```
kubectl get namespace ${NS} -o json \
  | tr -d "\n" | sed "s/\"finalizers\": \[[^]]\+\]/\"finalizers\": []/" \
  | kubectl replace --raw /api/v1/namespaces/${NS}/finalize -f -
```  