# Workflow

## Step 1: Node Exporter

Use to collects server metrics like CPU, Memory, Disk.

## Step 2: Prometheus

Is use to collects the metrics form NodeExporter.

We define alert rules in Prometheus, such as memory usage above 80% or a server being down. Prometheus continuously collects metrics from Node Exporter and compares them with these rules. If any rule is matched, Prometheus goes into the Firing state.

## Step 3: Alertmanager

Prometheus forwards all firing alerts to Alertmanager.

When Alertmanager receives an alert, it sends email to the configured mail address.

## Step 4: Grafana

Grafana connects to Prometheus as a data source. Grafana is mainly used for visualization.
