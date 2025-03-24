# my-monitoring

My monitoring lab repo

## System
### Exporter
https://github.com/prometheus/node_exporter

### Dashboard
https://grafana.com/grafana/dashboards/1860-node-exporter-full

## Docker
### Exporter
https://github.com/google/cadvisor

### Dashboard
https://grafana.com/grafana/dashboards/14282-cadvisor-exporter/

Had to add the following snippet to the dashboard json file to automatically find the datasource for grafana provisioning (defining the variable 'DS_PROMETHEUS' with the 'prometheus' value).
```json
  "templating": {
    "list": [
      {
        "current": {
          "selected": false,
          "text": "default",
          "value": "default"
        },
        "hide": 0,
        "includeAll": false,
        "label": "Datasource",
        "multi": false,
        "name": "DS_PROMETHEUS",
        "options": [],
        "query": "prometheus",
        "queryValue": "",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "type": "datasource"
      },
 ```

## Oracle
### Exporter
https://github.com/oracle/oracle-db-appdev-monitoring

### Dashboard
Based on https://github.com/oracle/oracle-db-appdev-monitoring/blob/main/docker-compose/grafana/dashboards/oracle_rev2.json and modified to add new visualizations

