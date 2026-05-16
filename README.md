# Gitops learning project

Project to learn ArgoCD and GitOps principles by moving existing services from manual to GitOps control, and also from VM's. Starting with setting up Argo itself, then looking into secrets and vaults, while moving Unifi Network Service.

Starting state is 3 node (including ControlPlane) cluster, running Talos OS vm's on Hyper-V. MetalLB for loadbalancer support and an NFS VM for persistent storage.

In the long run I'll move off Hyper-V and onto baremetal. What will be decided by som more research.

## Plan

1. remove devops-tools namespace contents
1. setup argoCD in devops-tools
1. Unifi put on hold for now. Doing metrics and monitoring first.

## Plan part 2.
So, the part above got partly scrapped. 

And some learning during Cilium install and config, caused a few full wipes. Good thing I'm running this on a hypervisor, I could use snapshots to revert to a pre bootstrap state.

Current status is as follows:

4 node Talos cluster(1 CP, 3 Worker), Cilium CNI and KubeProxy replacement, ArgoCD manages applications and systems, all except the Talosconfig, and itself so far.

Currently we have the following installed and running:
- CertManager
- Stirling-PDF
-

