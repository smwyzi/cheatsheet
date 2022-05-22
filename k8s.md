### get pod name by label
```
kubectl -n <ns> get pod -l app=<name> -o 'jsonpath={.items[0].metadata.name}'
```

### 强制删除无法删除的 ns
```
kubectl get namespace <ns> -o json \
  | tr -d "\n" | sed "s/\"finalizers\": \[[^]]\+\]/\"finalizers\": []/" \
  | kubectl replace --raw /api/v1/namespaces/<ns>/finalize -f -
```  
