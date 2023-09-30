```
kubectl create secret generic f5-bigip-ctlr-login -n kube-system --from-literal=username=admin --from-literal=password=<password>
```

```
kubectl create serviceaccount bigip-ctlr -n kube-system
```

```
kubectl apply -f k8s_rbac.yaml
kubectl apply -f https://raw.githubusercontent.com/F5Networks/k8s-bigip-ctlr/master/docs/config_examples/customResourceDefinitions/customresourcedefinitions.yml
kubectl apply -f  cis_deploy.yaml
```
