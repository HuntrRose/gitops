# Gitops learning project

Project to learn ArgoCD and GitOps principles by moving existing services from manual to GitOps control, and also from VM's. Starting with setting up Argo itself, then looking into secrets and vaults, while moving Unifi Network Service.

Starting state is 3 node (including ControlPlane) cluster, running Talos OS vm's on Hyper-V. MetalLB for loadbalancer support and an NFS VM for persistent storage.

In the long run I'll move off Hyper-V and onto baremetal. What will be decided by som more research.

## Plan

1. remove devops-tools namespace contents
2. setup argoCD in devops-tools
3. Implement Unifi Network Server through Argo
