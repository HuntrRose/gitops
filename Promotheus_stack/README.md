#  Kube-Prometheus-stack

[[https://artifacthub.io/packages/helm/prometheus-community/kube-prometheus-stack]]

And for metrics from Talos: https://docs.siderolabs.com/kubernetes-guides/monitoring-and-observability/deploy-metrics-server

https://docs.siderolabs.com/kubernetes-guides/monitoring-and-observability/etcd-metrics

## Helm output. 

NAME: prometheus-stack
LAST DEPLOYED: Fri May 15 11:43:11 2026
NAMESPACE: monitoring
STATUS: deployed
REVISION: 1
DESCRIPTION: Install complete
TEST SUITE: None
NOTES:
kube-prometheus-stack has been installed. Check its status by running:
  kubectl --namespace monitoring get pods -l "release=prometheus-stack"

Get Grafana 'admin' user password by running:

  kubectl --namespace monitoring get secrets prometheus-stack-grafana -o jsonpath="{.data.admin-password}" | base64 -d ; echo

Access Grafana local instance:

  export POD_NAME=$(kubectl --namespace monitoring get pod -l "app.kubernetes.io/name=grafana,app.kubernetes.io/instance=prometheus-stack" -oname)
  kubectl --namespace monitoring port-forward $POD_NAME 3000

Get your grafana admin user password by running:

  kubectl get secret --namespace monitoring -l app.kubernetes.io/component=admin-secret -o jsonpath="{.items[0].data.admin-password}" | base64 --decode ; echo


Visit https://github.com/prometheus-operator/kube-prometheus for instructions on how to create & configure Alertmanager and Prometheus instances using the Operator.