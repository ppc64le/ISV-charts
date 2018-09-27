# RethinkDB

[RethinkDB](https://github.com/rethinkdb/rethinkdb) Open-source database for building realtime web applications.

## TL;DR;

```console
$ helm install stable/ibm-rethinkdb
```

## Prerequisites

- Kubernetes 1.7+ with Beta APIs enabled
- Tiller 2.6.0 or later

## Resources Required
The chart deploys pods consuming minimum resources as specified in the values.yaml file (default: Memory: 200Mi, CPU: 100m)

## Introduction

[RethinkDB](https://github.com/rethinkdb/rethinkdb) Open-source database for building realtime web applications.

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm intall --name my-release stable/ibm-rethinkdb
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Chart Details
This chart bootstraps a [RethinkDB](https://github.com/rethinkdb/rethinkdb) deployment on a [Kubernetes](http://kubernetes.io) cluster


## Configuration

The following table lists the configurable parameters of the rethinkdb chart and their default values.

|      Parameter            |          Description            |                         Default                         |
|---------------------------|---------------------------------|---------------------------------------------------------|
| `image`                   | The image to pull and run       | A recent official rethinkdb tag                         |
| `imagePullPolicy`         | Image pull policy               | `Always` if `imageTag` is `latest`, else `IfNotPresent` |
| `node`                    | Specify what architecture Node  | `amd64` or `ppc64le`                                    |


The above parameters map to `ibm-rethinkdb` params.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. 

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

```bash
$ helm install --name my-release -f values.yaml stable/ibm-rethinkdb
```

> **Tip**: You can use the default [values.yaml](values.yaml)

## Limitations
