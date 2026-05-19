# `HomeLab: the story`

## Inspiration/Motivation
Originally, my host and service definitions lived in a [Nix monorepo](https://github.com/simisimis/s).
It was ok the way I was using it. Traefik wired to services like Plex or Home Assistant with never changing configuration.
However if I wanted to play with configuration options, new versions, or just drop in a service to try out, this excessive bureaucracy was not very comfortable.

The way I like to work:
1. Deploy initial setup
2. Fine tune the changes until I see the output I expect
3. Catch the drift and commit it in a final version

In the meantime professionally I was doing just that.
And when it was time to replace my 10 year old Intel Nuc, I realized that it's a perfect time to make some changes.
Use nix to keep track of infra. Use GitOps to keep the state of the runtime.
As for the rest, let Kubernetes do it's `Eventual Consistency` thing.

## Shopping List
- free Cloudflare account
- a domain or two transferred to Cloudflare
- a couple of N150 boxes. The prices aren't as they used to be though 😭

## The Process / Pr(👹)ss

### Early days

Since I decided to do this, many things have changed. I just wanted to learn more about Cilium eBPF magic and I to be more motivated to complete it, like with most of the things - I made a project out of it.

As I started putting things together I wanted to be able to spread my boxes between a homes. Additionaly I had to consider the problems that arise from my ISP CGNAT limitations.

I wanted ArgoCD to pick up secrets from a secret manager, i.e. self hosted Vaultwarden instance. However after 2 weeks of deep diving into Bitwarden internals and trying to bend to its limitations I managed to get things working. Just to have my friend asking me - why not Vault?

Another big one was how to add an authentication layer like Authelia or Authentik. I had it on my old setup but since Cloudflare already something I decided to keep it simple and just use Cloudflare's.

### Up until now

I have migrated all the workloads from the nix expressions to helm charts/values. And oh what a joy it's giving me every day.

Moving Home Assistant was easy. Home Assistant has become a big Pandora's box and I think it's best if you just run it as a docker image and just mount your configurations. Comparing to all the work that had to be done to package it with nix.

Most of the services are stateless and they can move around the nodes. And for the ones that need access to particular disk or peripherals, `nodeSelector` does the job:
- Jellyfin mounts local storage and has access to hardware decoding.
- Zigbee stack is able to get to its USB coordinator.

Vault contains cluster related secrets. Because the secrets shouldn't live longer than the cluster, no need an external secrets manager.

And every time I need to drop in another service, I just template a helm chart, create a `HTTPRoute` resource and watch things come to life.

If I am playing with versions or config files, once I'm happy, check ArgoCD Web UI for the drift, commit the changes and bam.

### What is there for tomorrow

Even though I have been working with these things professionally for so many years, I was pleasantly suprised how rewarding can be creating your cluster vs terraforming an `aws` managed one. You're free to make your own choices, adapt to your own use case, go wild doing research and experiment unexplored concepts.

As of what comes next. Probably I will be replacing kube-prometheus-stack with something better suited for non enterprice environment. Like OpenTelemetry + Victoriametrics(logs/traces/vmalert) for metrics compatibility and storage retention.
