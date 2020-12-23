# What's next for Calvinverse

- .NET core builds
- Containers for all the things that don't store data
  - Logstash
  - Grafana
  - proxy
- Additional services
  - Backup
  - Watchdog
  - Deployment
  - Authentication automation
  - Orchestration
  - Provisioning
- Infrastructure
  - Nomad
  - file storage
  - kubernetes(?)
  - Update Linux base
  - Update Windows base
  - Update hashi.server
  - Update hashi.ui
  - Update secrets
  - Update artefacts

- Define environments
  - Meta - Contains
    - Consul servers
    - Consul UI
    - Vault - This is the only one that needs to be manually unsealed. All others
      use this cluster to unseal themselves
    - Deployment service
  - Observation - Contains
    - Influx
    - Elasticsearch
    - Jaeger
    - Consul cluster
    - Vault cluster
  - Work clusters - Contain
    - Consul cluster
    - Vault cluster
    - Services needed for this specific cluster to do work. Services may
      differ per environment


## Other things

- Builds need to be .NET core
  - nBuildKit replacement?
- Generators -> .NET Core

# What's next for me?

- Blogging about cool things you make
- Put calvinverse on Azure
  - then azure-ify it (containers, websites, azure functions etc.)
- Try the same with AWS and google compute