# start minikube
```
minikube start --driver=docker
```

# forward port of app
```
k port-forward svc/react-app 3001:80 -n gitopstutorial
```

# forward ports of argocd
```
kubectl port-forward svc/argocd-server -n argocd 8080:443 &
```

# get password
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```
