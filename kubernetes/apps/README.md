# Applications

### [Actual](https://github.com/actualbudget/actual)
Actual is a local-first personal finance tool. It is 100% free and open-source, written in NodeJS, it has a synchronization element so that all your changes can move between devices without any heavy lifting.

### [Alert Manager](https://github.com/prometheus/alertmanager)
The Alertmanager handles alerts sent by client applications such as the Prometheus server. It takes care of deduplicating, grouping, and routing them to the correct receiver integrations such as email, PagerDuty, OpsGenie, or many other mechanisms thanks to the webhook receiver. It also takes care of silencing and inhibition of alerts. Installed as part of kube-prometheus-stack.

### [Cert-Manager](https://github.com/cert-manager/cert-manager)
Cert-manager is a X.509 certificate manager for Kubernetes. It adds multiple certificate and issuer resources to your cluster can help you automate obtaininig, renewing, and using your certificates.

### [Cloudflare DNS (External DNS)](https://github.com/kubernetes-sigs/external-dns)
ExternalDNS synchronizes exposed Kubernetes Services and Ingresses with DNS providers.

### [Cloudflare Tunnel](https://github.com/cloudflare/cloudflared)
A tunneling daemon that proxies traffic from the Cloudflare network to your origins. This daemon sits between Cloudflare network and your origin (e.g. a webserver). Cloudflare attracts client requests and sends them to you via this daemon, without requiring you to poke holes on your firewall --- your origin can remain as closed as possible. Extensive documentation can be found in the Cloudflare Tunnel section of the Cloudflare Docs.

### [Cilium](https://github.com/cilium/cilium)
Cilium is an open source, cloud native solution for providing, securing, and observing network connectivity between workloads, fueled by the revolutionary Kernel technology eBPF

### [CoreDNS](https://github.com/coredns/coredns)
CoreDNS is a fast and flexible DNS server. The key word here is flexible: with CoreDNS you are able to do what you want with your DNS data by utilizing plugins. If some functionality is not provided out of the box you can add it by writing a plugin. CoreDNS is a Cloud Native Computing Foundation graduated project.

### [CloudNative Postgres Operator](https://github.com/cloudnative-pg/cloudnative-pg)
CloudNativePG is a comprehensive open source platform designed to seamlessly manage PostgreSQL databases within Kubernetes environments, covering the entire operational lifecycle from initial deployment to ongoing maintenance. The main component is the CloudNativePG operator. Deploy a Postgres `Cluster` to [define your deployment](https://cloudnative-pg.io/documentation/1.25/cloudnative-pg.v1/#Cluster).
```
apiVersion: postgresql.cnpg.io/v1
kind: Cluster
metadata:
  name: cluster-example
  namespace: default
spec:
  instances: 3
  storage:
    size: 1Gi
```

### [CSI Driver NFS](https://github.com/kubernetes-csi/csi-driver-nfs)
This driver allows Kubernetes to access NFS servers on both Linux and Windows nodes, plugin name: `nfs.csi.k8s.io`.

### [CSI Driver SMB](https://github.com/kubernetes-csi/csi-driver-smb)
This driver allows Kubernetes to access SMB servers on both Linux and Windows nodes, plugin name: `smb.csi.k8s.io`.

### [Descheduler](https://github.com/kubernetes-sigs/descheduler)
The descheduler can be used to rebalance clusters by evicting pods that can potentially be scheduled on better nodes. In its default configuration, it runs as a CronJob to periodically check and optimize pod placement based on configurable strategies.

### [Device Plugin](https://github.com/squat/generic-device-plugin)
The generic-device-plugin enables allocating generic Linux devices, such as serial devices, the FUSE device, or video cameras, to Kubernetes Pods. This allows devices that don't require special drivers to be advertised to the cluster and scheduled, enabling various use-cases.

### [Endurain](https://github.com/endurain-project/endurain)
Endurain is a self-hosted fitness tracking service designed to give users full control over their data and hosting environment. It's similar to Strava but focused on privacy and customization.

### [Envoy Gateway](https://github.com/envoyproxy/gateway)
Envoy Gateway is an open source project for managing Envoy Proxy as a standalone or Kubernetes-based application gateway. Gateway API resources are used to dynamically provision and configure the managed Envoy Proxies.

### [Flux Extensions](https://github.com/fluxcd/flux2/)
- [Monitoring Alerts](https://fluxcd.io/flux/monitoring/alerts/) - This guide will help you setup alerts that use the notification controller. Many Flux `kind`s can be monitored and send alerts based on state changes or errors. Cross-namespace references are difficult (by design) so I've done a single secret in `flux-system` as well as the provider which references it. The alert can point to objects in other namespaces so this removes the need for replicating resources across namespaces.
- [Webhook Receivers](https://fluxcd.io/flux/guides/webhook-receivers/) - With cert-manager installed and the ability to create certificates for custom domains, we can turn Flux into a push-based pipeline that will trigger a sync any time there's a commit.

### [Gatus](https://github.com/TwiN/gatus)
Gatus is a developer-oriented health dashboard that gives you the ability to monitor your services using HTTP, ICMP, TCP, and even DNS queries as well as evaluate the result of said queries by using a list of conditions on values like the status code, the response time, the certificate expiration, the body and many others. The icing on top is that each of these health checks can be paired with alerting via Slack, Teams, PagerDuty, Discord, Twilio and many more.

### [Gatus Sidecar](https://github.com/home-operations/gatus-sidecar)
A powerful Kubernetes sidecar that automatically generates Gatus monitoring configuration from Kubernetes resources including Ingress, Gateway API HTTPRoute, and Service resources.

### [Glance](https://github.com/glanceapp/glance)
A lightweight, highly customizable dashboard that displays your feeds in a beautiful, streamlined interface.

### [Grafana](https://github.com/grafana/grafana)
Grafana lets you query, visualize, alert on, and explore your metrics, logs, and traces wherever they're stored. This install is a part of the [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack) which is helpful for monitoring a K8S cluster. It comes with many helpful default dashboards. The default credentials for this install is `admin`/`prom-operator`.

### [Grocy](https://github.com/grocy/grocy)
Grocy is a web-based self-hosted groceries & household management solution for your home. Uses the LinuxServer [Docker image](https://hub.docker.com/r/linuxserver/grocy).

### [Home Assistant](https://github.com/home-assistant/core)
Home Assistant is a home automation toolkit that lets you automate and control your home. Changes to `configuration.yaml` are required if you want to place Home Assistant behind a proxy. When doing the first-time install, disable the mount that maps the configmap to the pod. Let the deployment create the directory and necessary files first, then reconfigure the deployment to use your configmap which can be updated as needed. Reloader will take care of restarting it if you do any further configuration changes. Use `ws://localhost:3000` for the web-socket address in the z-wave integration instead of the detected IP address since the pod IP can change with restarts.

### [Homepage](https://github.com/gethomepage/homepage)
A modern, fully static, fast, secure fully proxied, highly customizable application dashboard with integrations for over 100 services and translations into multiple languages. Easily configured via YAML files or through docker label discovery.

### [Jellyfin](https://github.com/jellyfin/jellyfin/)
Jellyfin is a Free Software Media System that puts you in control of managing and streaming your media. It is an alternative to the proprietary Emby and Plex, to provide media from a dedicated server to end-user devices via multiple apps.

### [K8S Gateway](https://github.com/k8s-gateway/k8s_gateway)
A CoreDNS plugin that is very similar to k8s_external but supporting all types of Kubernetes external resources - Ingress, Service of type LoadBalancer, HTTPRoutes, TLSRoutes, GRPCRoutes from the Gateway API project.

### [Kavita](https://github.com/Kareadita/Kavita)
Kavita is a fast, feature rich, cross-platform reading server. Built with a focus for being a full solution for all your reading needs. Set up your own server and share your reading collection with your friends and family!

### [Linkding](https://github.com/sissbruecker/linkding)
Linkding is a bookmark manager that you can host yourself. It's designed be to be minimal, fast, and easy to set up using Docker.

### [LocalAI](https://github.com/mudler/LocalAI)
LocalAI is the open-source AI engine. Run any model - LLMs, vision, voice, image, video - on any hardware. No GPU required.

### [Mealie](https://github.com/mealie-recipes/mealie/)
Mealie is a self-hosted recipe manager, meal planner, and shopping list application.

### [Metrics Server](https://github.com/kubernetes-sigs/metrics-server)
Metrics Server is a scalable, efficient source of container resource metrics for Kubernetes built-in autoscaling pipelines. Publishes resource usage to enable `HorizontalPodAutoscaler` and `VerticalPodAutoscaler`.

### [MySpeed](https://github.com/gnmyt/myspeed/)
Test analysis software that records your internet speed for up to 30 days.

### [Node Feature Discovery](https://github.com/kubernetes-sigs/node-feature-discovery)
Node Feature Discovery is an addon to detect node capabilities for Kubernetes. It detects hardware features available on each node in a Kubernetes cluster, and advertises those features using node labels and optionally node extended resources, annotations and node taints. Node Feature Discovery is compatible with any recent version of Kubernetes (v1.24+).

### [Nvidia Device Plugin](https://github.com/NVIDIA/k8s-device-plugin)
The NVIDIA device plugin for Kubernetes is a Daemonset that allows you to automatically expose the number of GPUs on each nodes of your cluster, keep track of the health of your GPUs, and run GPU enabled containers in your Kubernetes cluster.

### [Open WebUI](https://github.com/open-webui/open-webui)
Open WebUI is an extensible, feature-rich, and user-friendly self-hosted AI platform designed to operate entirely offline. It supports various LLM runners like Ollama and OpenAI-compatible APIs, with built-in inference engine for RAG, making it a powerful AI deployment solution.

### [Prometheus](https://github.com/prometheus/prometheus)
Prometheus is a great systems monitoring and alerting toolkit. It's the datasource that is used by Grafana to display your cluster statistics and information. This install is a part of the [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack) which is helpful for monitoring a K8S cluster.

### [Reflector](https://github.com/emberstack/kubernetes-reflector)
Reflector is a Kubernetes addon designed to monitor changes to resources (`secret` and `configmap`) and reflect changes to mirror resources in the same or other namespaces.

### [Reloader](https://github.com/stakater/reloader)
Reloader will watch many resources for `ConfigMap` or `Secret` changes and automatically rollout an update for those changes. Simply add the annotation `reloader.stakater.com/auto: "true"` to your Deployment `.metadata`. See the [documentation](https://github.com/stakater/reloader#how-to-use-reloader) for more examples.

### [Renovate Operator](https://github.com/mogenius/renovate-operator)
[Renovate](https://github.com/renovatebot/renovate) is an automated dependency update tool. It helps to update dependencies in your code without needing to do it manually. When Renovate runs on your repo, it looks for references to dependencies (both public and private) and, if there are newer versions available, Renovate can create pull requests to update your versions automatically.

### [Rook/Ceph](https://github.com/rook/rook)
Rook is an open source cloud-native storage orchestrator for Kubernetes, providing the platform, framework, and support for Ceph storage to natively integrate with Kubernetes.

### [Snapshot Controller](https://github.com/kubernetes-csi/external-snapshotter)
The CSI snapshotter is part of Kubernetes implementation of Container Storage Interface (CSI) and implements both the volume snapshot and the volume group snapshot feature.

### [SparkyFitness](https://github.com/CodeWithCJ/SparkyFitness)
A self-hosted, privacy-first alternative to MyFitnessPal. Track nutrition, exercise, body metrics, and health data while keeping full control of your data.

### [Spegel](https://github.com/spegel-org/spegel)
Spegel enables each node in a Kubernetes cluster to act as a local registry mirror, allowing nodes to share images between themselves. Any image already pulled by a node will be available for any other node in the cluster to pull. This has the benefit of reducing workload startup times and egress traffic as images will be stored locally within the cluster. On top of that it allows the scheduling of new workloads even when external registries are down.

### [Tuppr](https://github.com/home-operations/tuppr)
A Kubernetes controller for managing automated upgrades of Talos Linux and Kubernetes.

### [Valheim Game Server](https://github.com/lloesche/valheim-server-docker)
Valheim Server in a Docker Container (with BepInEx and ValheimPlus support)

### [vLLM](https://github.com/vllm-project/vllm)
vLLM is a fast and easy-to-use library for LLM inference and serving.

### [VolSync](https://github.com/backube/volsync)
VolSync asynchronously replicates Kubernetes persistent volumes between clusters using either rsync or rclone. It also supports creating backups of persistent volumes via restic.

### [Wiki.js](https://github.com/Requarks/wiki)
A modern, lightweight, and powerful wiki app built on NodeJS

### [Z-Wave JS UI](https://github.com/zwave-js/zwave-js-ui)
Z-Wave control panel and MQTT gateway. Either can be enabled separately or both together. I've paired this with Home Assistant so I can control z-wave switches and outlets around the home via [this dongle](https://a.co/d/9HZfxjH). By running this in the same pod as Home Assistant, it's still accessible from HA via localhost and keeps the services and ingresses simple.
