# `HomeLab on kubernetes(k3s)`

## Main objectives
- Create a multi-zone self hosted k3s cluster
- Migrate workloads

## Design requirements
- GITOPS, ArgoCD, workflows
- use wireguard to connect to other locations
- domain zone control(let's encrypt)
- persistent storage available for all nodes
- metrics/alerting
- secrets

## Goals that define basic success
- A healthy multi-zone k3s cluster
- IaC on git
- Secrets management
- DNS name issuing/signing
- wireguard

## End goal of (un)achievable completion
- TBD
