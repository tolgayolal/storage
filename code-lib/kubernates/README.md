# Kubernates codes

## Clear Evicted Pod
This code remove all "Evicted" status pods
```bash
kubectl get pod --all-namespaces -o json | jq  '.items[] | select(.status.reason!=null) | select(.status.reason | contains("Evicted")) | "kubectl delete pod/\(.metadata.name)"' | xargs -n 1 bash -c
```
Ref : https://gist.github.com/ipedrazas/9c622404fb41f2343a0db85b3821275d

## Delete All Pod
This code remove all pods
```bash
kubectl delete --all pods
```
Ref : https://stackoverflow.com/questions/33509194/command-to-delete-all-pods-in-all-kubernetes-namespaces


