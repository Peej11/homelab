# Grafana Dashboards

Source-controlled Grafana dashboards provisioned by the [kube-prometheus-stack
HelmRelease](../kube-prometheus-stack/app/hr.yaml). Each dashboard is committed here as
pinned JSON and referenced from `hr.yaml` (`grafana.dashboards.<provider>.<key>.url`) via a
raw GitHub URL, so Grafana downloads it at pod start. Grafana fetches from `main`, so new or
moved dashboards must be pushed before the Grafana pod rolls out.

Dashboards are normalized to the `${datasource}` template-variable convention (a
`datasource`-typed template variable with `query: prometheus`, and every panel referencing
`{ "type": "prometheus", "uid": "${datasource}" }`) so they bind to the default Prometheus
datasource without a hardcoded UID. The `rpi-monitoring` dashboards are remixed/sized to fit a small
[1280x720 display](https://a.co/d/hUkaYWZ) for at-a-glance monitoring on the rack.

## Layout

Each subdirectory maps to a dashboard provider (Grafana folder) in `hr.yaml`:

| Subdirectory     | Grafana folder | Provider                       |
| ---------------- | -------------- | ------------------------------ |
| `rpi-monitoring` | RPi Monitoring | `rpi-monitoring`               |
| `network`        | Network        | `grafana-dashboards-network`   |
| `certs`          | Certificates   | `grafana-dashboards-certs`     |
| `nodes`          | Nodes          | `grafana-dashboards-nodes`     |

The Kubernetes folder (`grafana-dashboards-kubernetes`) is provisioned directly from the
upstream [dotdc](https://github.com/dotdc/grafana-dashboards-kubernetes) repo and is not
mirrored here.
