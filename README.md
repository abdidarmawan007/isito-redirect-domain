# istio redirect domain with virtualservice
for example you need redirect user access abdidarmawan.id to abdidarmawan.com

kubectl apply -f redirect-id-to-com.yaml

## from http
```
curl -I http://abdidarmawan.id
HTTP/1.1 301 Moved Permanently
location: https://abdidarmawan.com
server: istio-envoy
```
## from https
```
curl -I https://abdidarmawan.id
HTTP/2 301
location: https://abdidarmawan.com
server: istio-envoy
```
