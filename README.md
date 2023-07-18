# Spatial Focus helm charts

Helm charts for GeoNetwork and GeoServer used on our microk8s.

# GeoNetwork

A Helm chart for running GeoNetwork, Elastic Seach and Kibana, connecting to an existing PostGIS database.

Create a yaml-file to override the helm values: `geonetwork-helm-values.override.yml`. Here we define the image source, database connection, and host information.

Then install the helm chart using the following command:

```bash
helm install -f geonetwork-helm-values.override.yml geonetwork-example ./charts/geonetwork/v0.1.0
```

# GeoServer

Source: [kartoza/geoserver](https://github.com/kartoza/charts/blob/develop/charts/geoserver/)

Unfortunately the helm repo at `https://kartoza.github.io/charts` is outdated, so we need to host v0.3.3 ourselves.

## Usage

Create a yaml-file to override the geoserver helm values: `geoserver-helm-values.override.yml`.

Then install the helm chart using the following command:

```bash
helm install -f geoserver-helm-values.override.yml geoserver-example ./charts/geoserver/v0.3.3
```

----

Made with :heart: by [Spatial Focus](https://www.spatial-focus.net/)