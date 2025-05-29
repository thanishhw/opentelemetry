# opentelemetry
otel-jaeger-grafana-prometheous


Docker

git clone https://github.com/open-telemetry/opentelemetry-demo.git
cd opentelemetry-demo/
make start

K8s

helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts
helm install my-otel-demo open-telemetry/opentelemetry-demo
kubectl apply --namespace otel-demo -f https://raw.githubusercontent.com/open-telemetry/opentelemetry-demo/main/kubernetes/opentelemetry-demo.yaml
kubectl port-forward svc/my-otel-demo-frontendproxy 8080:8080

Web store: http://localhost:8080/
Grafana: http://localhost:8080/grafana/
Load Generator UI: http://localhost:8080/loadgen/
Jaeger UI: http://localhost:8080/jaeger/ui/

    •       Flagd configurator UI: http://localhost:8080/feature
