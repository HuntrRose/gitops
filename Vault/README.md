# Secrets Vault
Starting here since all other applications needs this in one form or another.

## Alternatives

AI Overview
Self-hosting a secrets manager on Kubernetes (K8s)
involves deploying a centralized vault that can securely inject credentials into your workloads. Below are the leading self-hosted solutions and the tools used to integrate them with K8s. 
Top Self-Hosted Secrets Managers

    HashiCorp Vault: The industry standard for enterprise-grade secret management. It supports dynamic secrets, encryption-as-a-service, and complex access policies.
    Infisical: A developer-friendly, open-source platform that simplifies secret syncing and offers a user-friendly dashboard. It includes a native Infisical Kubernetes Operator for automatic secret delivery and deployment reloads.
    OpenBao: A community-led, open-source fork of HashiCorp Vault (MPL-licensed) created after Vault's license change. It serves as a drop-in replacement for those seeking a fully open-source alternative to Vault.
    CyberArk Conjur (Open Source): Tailored for cloud-native and container environments, it provides robust identity-based access for non-human identities and integrates via a dedicated Secrets Provider for K8s.
    Bitwarden Secrets Manager: While primarily known for password management, Bitwarden offers a dedicated secrets manager with a Kubernetes Operator to sync secrets into K8s at configurable intervals.

 