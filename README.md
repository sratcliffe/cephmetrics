# cephmetrics

Cephmetrics is a tool that allows a user to visually monitor various metrics in a running Ceph cluster. 

This fork is a stripped down version of cephmetrics more suitable for deployment on non-Redhat installations. The required infrastructure (Prometheus, Grafana) is also deployed via docker-compose.

We assume that the deployment of node_exporter on all hosts and enabling the ceph-mgr prometheus plugin are taken care of by the user.

Mostly we just keep the excellent dashboards :)
