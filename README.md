# cephmetrics

Cephmetrics is a tool that allows a user to visually monitor various metrics in a running Ceph cluster. 

This fork is a *really* stripped down version of cephmetrics more suitable for deployment on non-Redhat installations. The required infrastructure (Prometheus, Grafana) is also deployed via docker-compose.

We assume that the deployment of node_exporter on all hosts and enabling the ceph-mgr prometheus plugin are taken care of by the user.

Mostly we just keep the excellent dashboards :)

## Configuration

To get going you only really need to modify `prometheus/prometheus.yml` to configure the Ceph manager to scrape and the node exporter addresses for each physical host in your Ceph cluster.

The example config file just uses *localhost* in the various `targets` sections.

To use email based alerting you can also put sensible values into `grafana/config.monitoring` for the `SMTP_HOST` and the `SMTP_FROM_ADDRESS`.
