# Overview

This directory contains the Helm charts to deploy the kgateway project via [Helm](https://helm.sh/docs/helm/helm_install/).

## Directory Structure

- `kgateway-dashboards/`: Contains Grafana dashboards which can be used for monitoring.
  - Dashboards install as ConfigMaps, which can be detected automatically, when using kube-prometheus-stack.
  - They are optional and are not required to use kgateway.
  - The dashboards are intended only as a reference implementation for working with control-plane and data-plane metrics.
  - Users are encouraged to extend or expand upon these dashboards based on their particular monitoring needs.

## Installation Order

1. Install the monitoring dashboards:
   ```bash
   helm install kgateway-dashboards ./kgateway-dashboards
   ```

For detailed configuration options, please refer to the `values.yaml` file in each chart directory.
