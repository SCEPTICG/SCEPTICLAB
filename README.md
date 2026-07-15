# SCEPTIC-LAB

**Following the build of my homelab — rebuilt from scratch on Kubernetes (k3s) — in the open.**

[![license](https://img.shields.io/github/license/SCEPTICG/SCEPTICLAB?style=flat-square&logo=gnu&logoColor=white)](https://www.gnu.org/licenses/gpl-3.0.html)
[![stars](https://img.shields.io/github/stars/SCEPTICG/SCEPTICLAB?logo=github&logoColor=white&color=gold&style=flat-square)](https://github.com/SCEPTICG/SCEPTICLAB)

This is the public **progress page** for SCEPTIC-LAB, my home lab: a self-hosted Kubernetes cluster built one piece at a time, documented here and through videos I record along the way. The code lives in a separate repository while the project matures; the full, **fork-ready template** will be published here when it reaches **v1.0**.

> **What is a homelab?**
>
> A homelab is a lab at home where you can self-host services, experiment with new technologies, practice for certifications, and so on. See the [r/homelab introduction](https://www.reddit.com/r/homelab/wiki/introduction) and the [Home Operations Discord community](https://discord.gg/home-operations) for more context.

## Progress

What the project does, phase by phase. Ticked items are done; the rest is the roadmap, marked off as it lands.

- [x] Interactive menu — create main node · add node · exit
- [x] **Create main node** — provision a VM on Proxmox (Terraform + cloud-init) and install k3s as the first server (`--cluster-init`)
- [x] Store the cluster IP and join token automatically
- [x] Guided assistant for the Proxmox connection, reused from v1
- [x] Fetch the kubeconfig to the control machine
- [ ] **Add node** — provision another VM and join it to the cluster as a worker *(in progress)*
- [ ] Networking — MetalLB + Traefik
- [ ] GitOps with ArgoCD
- [ ] Storage — Longhorn + NFS from the NAS
- [ ] Secrets — Sealed Secrets
- [ ] TLS + DNS — cert-manager + external-dns
- [ ] Observability — Prometheus + Grafana + Loki + Tempo
- [ ] Apps — migrate the self-hosted services (Jellyfin, *arr, Vaultwarden, Forgejo, n8n, Mealie, Homepage...)
- [ ] Scale from 1 to 5 nodes on real hardware

## Milestones

- **v0.1-beta** — first single-node k3s cluster created end to end from the menu.

## Background

The previous version of the lab (v1) ran on Proxmox with LXC + Docker, provisioned with Terraform + Ansible. v2 keeps Proxmox and Terraform underneath (to create the node VMs) but runs every service on Kubernetes.

## License

[GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html)
