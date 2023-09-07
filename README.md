# traefik-ingress-routes

Run `kubectl apply` for each file to create necessary deployments, services and ingress routes

Deploy collector example web app

```sh
kubectl apply -f collector/configmap.yaml
kubectl apply -f collector/deployment.yaml
kubectl apply -f collector/service.yaml
kubectl apply -f collector/traefik-ingress.yaml
```


Deploy iglu example web app

```sh
kubectl apply -f iglu/configmap.yaml
kubectl apply -f iglu/deployment.yaml
kubectl apply -f iglu/service.yaml
kubectl apply -f iglu/traefik-ingress.yaml
```

edit your `/etc/hosts` file and add in your traefik public IP (or nlb ip) and set the domains

```
<IP> collector.example.com
<IP> iglu.example.com
```

Testing path based routes

