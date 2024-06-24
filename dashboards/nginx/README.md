Nginx Dashboards
================

fetched from the [ingress-nginx git repo](https://github.com/kubernetes/ingress-nginx/tree/main/deploy/grafana/dashboards)

To fix, we must change all `datasource` configurations in the `templating` and `panels` blocks as follows:

    -          "datasource": {
    -            "type": "prometheus",
    -            "uid": "${DS_PROMETHEUS}"
    -          },
    +          "datasource": "${DS_PROMETHEUS}",