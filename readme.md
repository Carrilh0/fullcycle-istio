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

Para realizar o deploy canário pelo istio é bem simples. Pela dashboard no Kiali você consegue alterar todas as possiveis configurações.

### Stick Session | consistense hasg

Por padrão, um Application Load Balancer roteia cada solicitação de forma independente para um destino registrado com base no algoritmo de balanceamento de carga escolhido. No entanto, você pode usar o recurso de sessão persistente (também conhecido como afinidade de sessão) para permitir que o balanceador de carga associe a sessão de um usuário a um destino específico. Isso garante que todas as solicitações do usuário durante a sessão sejam enviadas para o mesmo destino. Esse recurso é útil para servidores que mantêm informações de estado para fornecer uma experiência contínua aos clientes. Para usar sessões fixas, o cliente deve oferecer suporte a cookies.