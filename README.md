# 🏠 HomeLab

Personal home lab environment running on self-hosted infrastructure. This repository contains Docker Compose stacks, configurations, and documentation for my home lab setup.

## 🖥️ Hardware

| Device | Role | Specs |
|--------|------|-------|
| Lenovo V520s SFF | Main server | Intel i5 7th gen, 16GB DDR4, Debian |
| ThinkPad L390 | Workstation | Intel i5 8th gen, 8GB RAM, Windows 11 |
| iPad Air M3 | Management terminal | — |
| ZTE U50 | LTE Router | T-Mobile 5G |

## 🌐 Network

- **Local network:** `192.168.0.0/24`
- **VPN:** Tailscale (all devices connected)
- **DNS/DHCP:** Pi-hole
- **Local domains:** `.lab` (resolved via Pi-hole)
- **Reverse proxy:** Nginx Proxy Manager with SSL

## 📦 Stacks

| Service | URL | Description |
|---------|-----|-------------|
| Portainer | `portainer.lab` | Docker management UI |
| Pi-hole | `pihole.lab` | DNS sinkhole + DHCP server |
| Nginx Proxy Manager | `npm.lab` | Reverse proxy + SSL termination |
| Grafana | `grafana.lab` | Metrics dashboards |
| Prometheus | `prometheus.lab` | Metrics collection |
| Homepage | `home.lab` | Lab dashboard |
| Code Server | `code.lab` | VS Code in the browser |
| Firefly III | — | Personal finance manager |
| RustDesk | — | Self-hosted remote desktop |

## 🔒 Security

- Tailscale VPN for secure remote access (no open ports on router)
- SSL certificates via Tailscale for all services
- Pi-hole for network-level ad and tracker blocking
- Secrets and certificates excluded from this repository

## 🛠️ Tech Stack

`Debian` `Docker` `Tailscale` `Nginx` `Prometheus` `Grafana` `Pi-hole`

---

> This lab is a personal learning environment. Configurations are shared for reference — always review before use in your own setup.
