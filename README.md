#### Building

```bash
gvt fetch --branch master github.com/jroimartin/gocui
gvt fetch --revision v0.11.2 github.com/sirupsen/logrus
gvt fetch --revision v2.3.3 github.com/TykTechnologies/tyk

```

#### Kubernetes
```bash
# minikube only
eval $(minikube docker-env)

# redis
kubectl create -f _kubernetes/redis/redis-deployment.yaml
kubectl create -f _kubernetes/redis/redis-service.yaml

# gateway
kubectl create configmap tyk-gateway-conf --from-file=_kubernetes/gateway/tyk.conf
kubectl create -f _kubernetes/gateway/tyk-gateway-deployment.yaml
kubectl create -f _kubernetes/gateway/tyk-gateway-service.yaml
```

#### docker-compose
