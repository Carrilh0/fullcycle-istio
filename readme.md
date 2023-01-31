### Comando para ativar o sidecar proxy

``kubectl label namespace default istio-injection=true``

### Repositorio de addons para o Istio

https://github.com/istio/istio/tree/master/samples/addons

Grafana 
https://raw.githubusercontent.com/istio/istio/master/samples/addons/grafana.yaml

Jaeger
https://raw.githubusercontent.com/istio/istio/master/samples/addons/jaeger.yaml

Kiali
https://raw.githubusercontent.com/istio/istio/master/samples/addons/kiali.yaml

Prometheus
https://raw.githubusercontent.com/istio/istio/master/samples/addons/prometheus.yaml

### Para aplicar todos os addons de uma vez

``kubectl apply -f https://raw.githubusercontent.com/istio/istio/master/samples/addons/grafana.yaml && kubectl apply -f https://raw.githubusercontent.com/istio/istio/master/samples/addons/jaeger.yaml && kubectl apply -f https://raw.githubusercontent.com/istio/istio/master/samples/addons/kiali.yaml && kubectl apply -f https://raw.githubusercontent.com/istio/istio/master/samples/addons/prometheus.yaml``