# Talos configuration files

All Talos OS / Kubernetes config files that does not contain secrets.
Those are generated when setting up the cluster.


 - patch.yaml: Removes existing CNI (Flannel) from config, and preps for Cilium replacement for kubeProxy
    - for later I add Metricsserver deployment to this [as per documentation](https://docs.siderolabs.com/kubernetes-guides/monitoring-and-observability/deploy-metrics-server)
    - for now I run the kubectl commands instead.
 - etcd-metrics-patch.yaml: patch to expose the etcd metrics endpoint. This so I can monitor this with Prometheus. Following [Sidero documentation](https://docs.siderolabs.com/kubernetes-guides/monitoring-and-observability/etcd-metrics)

## Upgrade image
Use the following image for upgrading:
factory.talos.dev/metal-installer/613e1592b2da41ae5e265e8789429f22e121aab91cb4deb6bc3c0b6262961245:v1.13.4

Schematic ID: 613e1592b2da41ae5e265e8789429f22e121aab91cb4deb6bc3c0b6262961245


Next steps: 
Secure your control plane IP addresses to prevent public access. See the [Ingress Firewall](https://docs.siderolabs.com/talos/v1.10/networking/ingress-firewall) guide for instructions on securing your control plane.

