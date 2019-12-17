## Guide to deploye a Kubernetes cluster and deployed a multi-container application to it. 

1. Open Azure Cloud Shell

```
az group create --name IntegrationMondayAKSdemo --location eastus
```

```
az aks create --resource-group IntegrationMondayAKSdemo --name IntegrationMondayAKSClusterAKSdemo --node-count 1 --enable-addons monitoring --generate-ssh-keys
```
```
az aks get-credentials --resource-group IntegrationMondayAKSdemo --name IntegrationMondayAKSClusterAKSdemo
```

```
kubectl get nodes
```

```
code
```


save file as azure-vote.yaml

```
kubectl apply -f azure-vote.yaml
```

CTRL-C  to stop the kubectl watch process

Go to the IP Address and verify that the application is up and running
