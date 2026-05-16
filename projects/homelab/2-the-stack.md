---
title: "HomeLab: the stack"
date: "2026-05-14"
tags: ["k3s", "k8s", "kubernetes", "gitops", "argocd", "gateway-api", "homelab"]
slug: "homelab-the-stack"
summary: "Current state of the homelab stack managed from the repo."
status: "ongoing"
---

# `HomeLab: the stack`

## What is running today

### The drawing board

NixOS hosts with `services.k3s.enable` ([Heavily stripped](https://github.com/simisimis/s/blob/main/modules/k3s/default.nix)) + wireguard setup

The GitOps layout eventually matured to the following:
```
applications
├── applicationset.yaml
├── home-automation
│   ├── esphome
│   ├── hass
│   ├── mosquitto
│   └── zigbee2mqtt
├── mediaserver
│   ├── jellyfin
│   └── transmission
├── narbuto
├── utils
│   ├── actual-budget
└── vaultwarden
infrastructure
├── applicationset.yaml
├── controllers
|   ├── vault
│   └── argocd
├── monitoring
│   ├── kube-prometheus
│   └── metrics-server
├── networking
│   ├── adguard
│   ├── cert-manager
│   ├── cilium
│   ├── cloudflared
│   └── gateway
└── storage
    └── openebs
```

### Control plane and delivery model
- Ingress traffic over Cloudflare tunnel
- Repository layout is split into `applications/*` and `infrastructure/*`.
- Deployments are done by ArgoCD with Helmfile plugin. Instead of Helm + Kustomization.(Cilium and ArgoCD included)

### Infrastructure
- Networking:
  - Cloudflared
  - Cilium (+ Hubble)
  - Gateway API(Instead of Ingress)
  - AdGuard.
- Certificates: cert-manager with Cloudflare DNS-01.
- Storage: OpenEBS with ZFS-based storage classes.
- Observability:
  - kube-prometheus stack
  - metrics-server
- Platform control:
  - ArgoCD
  - Hashicorp Vault to render cluster secrets

### Routes and domain shape
- `Gateway` resource is configured with listeners for configured domain.
- Services exposed through `HTTPRoute` resources.

### Application workloads
- Home automation:
  - Home Assistant
  - Zigbee2MQTT
  - Mosquitto
  - ESPHome
- Media:
  - Jellyfin
  - Transmission.
  - TODO: Immich
- Utilities/apps:
  - Vaultwarden
  - Actual budget
  - Personal website
