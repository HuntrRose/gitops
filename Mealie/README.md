# Mealie setup plan

1. Set subdomain to point at cluster.
1. Create certmanager ClusterIssuer
1. Add certificate for subdomain
1. Add GateWay listener for subdomain:443
1. Install and basic config of Mealie package.
    * PGSQL
    * Secrets in Vault
    * 
1. Add HTTPRoute