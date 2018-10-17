# Alert Manager

[Alert Manager](https://prometheus.io/docs/alerting/alertmanager)The Alertmanager handles alerts sent by client applications such as the Prometheus server.

```console
$ helm install ibm-alertmanager
```

## Prerequisites

- Kubernetes 1.7+ with Beta APIs enabled
- Tiller 2.6.0 or later

## Resources Required
The chart deploys pods consuming minimum resources as specified in the resources configuration parameter (default: Memory: 200Mi, CPU: 100m)

## Introduction

This chart bootstraps a [Alert Manager](https://github.com/prometheus/alertmanager) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.


## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm intall --name my-release ibm-alertmanager
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Chart Details
This chart bootstraps a [Alert Manager]( https://hub.docker.com/r/ibmcom/alertmanager-ppc64le/) deployment on a [Kubernetes](http://kubernetes.io) cluster


## Configuration

The following table lists the configurable parameters of the Alert Manager chart and their default values.

|      Parameter            |          Description            |                         Default                         |
|---------------------------|---------------------------------|---------------------------------------------------------|
| `image`                   | The image to pull and run       | A recent official alertmanager tag                      |
| `imagePullPolicy`         | Image pull policy               | `Always` if `imageTag` is `latest`, else `IfNotPresent` |
| `nodeSelector`            | Specify what architecture Node  | `amd64` or `ppc64le`                                    |


The above parameters map to `ibm-alertmanager` params.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. 

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

```bash
$ helm install --name my-release -f values.yaml ibm-alertmanager
```

> **Tip**: You can use the default [values.yaml](values.yaml)

## Limitations
