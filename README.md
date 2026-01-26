<div align="center">

### <img src="./res/k8s-logo.png" align="center" width="30px" height="30px"/> Homelab <img src="./res/talos-logo.png" align="center" width="30px" height="30px"/>

_... managed with Flux, Renovate, and Github Actions_ 🤖

![Dynamic YAML Badge](https://img.shields.io/badge/dynamic/yaml?url=https%3A%2F%2Fraw.githubusercontent.com%2FPeej11%2Fhomelab%2Frefs%2Fheads%2Fmain%2Fkubernetes%2Fapps%2Ftuppr-config%2Fapp%2Ftalosupgrade.yaml&query=%24.spec.talos.version&style=for-the-badge&logo=talos&logoColor=white&label=Talos) ![Dynamic YAML Badge](https://img.shields.io/badge/dynamic/yaml?url=https%3A%2F%2Fraw.githubusercontent.com%2FPeej11%2Fhomelab%2Frefs%2Fheads%2Fmain%2Fkubernetes%2Fapps%2Ftuppr-config%2Fapp%2Fkubernetesupgrade.yaml&query=%24.spec.kubernetes.version&style=for-the-badge&logo=kubernetes&logoColor=white&label=Kubernetes
)

</div>

## 🛠️ Tools

| Tool                                     | Purpose                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------|
| [Flux](https://fluxcd.io/flux/)          | Operator to manage your K8S cluster based any number of sources including GitHub |
| [Renovate](https://docs.renovatebot.com) | Tool to automate dependency updates                                              |
| [SOPS](https://github.com/getsops/sops)  | K8S secrets and configmap manager to encrypt secrets with GnuPG for storage      |


## 🖥️ Nodes

| System             | RAM  | Storage        | Role   | OS    |
|--------------------|------|----------------|--------|-------|
| Radxa Rock 5B      | 32GB | None           | Master | Talos |
| Lenovo ThinkCentre | 32GB | 256GB NVMe SSD | Master | Talos |
| Lenovo ThinkCentre | 16GB | 256GB NVMe SSD | Master | Talos |
| Lenovo ThinkCentre | 16GB | 256GB NVMe SSD | Worker | Talos |
| Lenovo ThinkCentre | 16GB | 1TB NVMe SSD   | Worker | Talos |
| Lenovo ThinkCentre | 16GB | 2TB NVMe SSD   | Worker | Talos |


## 📦 Storage

| System  | RAM   | Storage             | OS            |
|---------|-------|---------------------|---------------|
| TrueNAS | 128GB | 12 x 8TB HDD RAIDZ3 | TrueNAS Scale |


## 🛜 Network 

| Vendor   | Model             | Function                                        |
|----------|-------------------|-------------------------------------------------|
| Ubiquiti | Dream Machine Pro | Primary Router, Camera Storage, Network Manager |
| Ubiquiti | US-48-500W        | Rack switch with PoE and 10G SFP+               |
| Ubiquiti | U7-Pro            | Wireless Access Point                           |
| Ubiquiti | U7-Pro Wall       | Wireless Access Point                           |
| Ubiquiti | U7-Pro Wall       | Wireless Access Point                           |


## ☁️ Cloud Services

| Service                                              | Use                                        | Cost            |
|------------------------------------------------------|--------------------------------------------|-----------------|
| [Backblaze](https://www.backblaze.com/cloud-storage) | Offsite S3 storage for important files     | ~$100/yr        |
| [Bitwarden](https://bitwarden.com)                   | Password management                        | Free            |
| [Cloudflare](https://www.cloudflare.com/)            | Domains and DNS management                 | ~$70/yr         |
| [GitHub](https://github.com/)                        | Hosting this repo and CI/CD                | Free            |
| [Let's Encrypt](https://letsencrypt.org/)            | Issuing SSL Certificates with Cert Manager | Free            |
| [UniFi Site Manager](https://unifi.ui.com)           | UniFi External Access Management           | Free            |
|                                                      |                                            | Total: ~$170/yr |
