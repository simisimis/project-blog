---
title: "HomeLab on Kubernetes (k3s)"
date: "2025-06-13"
tags: ["k3s", "k8s", "kubernetes", "gitops", "argocd", "homelab"]
slug: "homelab"
summary: "Vision and baseline goals for a GitOps-managed k3s homelab."
status: "ongoing"
---

# `HomeLab on Kubernetes (k3s)`

## Main objectives
- Create a multi-zone self hosted Kubernetes(k3s) cluster
- Migrate workloads

## Design requirements
- GITOPS, ArgoCD, workflows
- use wireguard to connect to wire locations
- domain zone control(let's encrypt)
- persistent storage available for all nodes
- metrics/alerting
- secrets

## Goals that define basic success
- A healthy multi-zone Kubernetes cluster(k3s)
- IaC on git(GitOps)
- Secrets store(Vault)
- DNS name issuing/signing(Cert-manager with CloudFlare)
- Wireguard
- Metrics/logs collected with OTLP collector and stored in Victoriametrics

## End goal of (un)achievable completion
- Can't think of any
