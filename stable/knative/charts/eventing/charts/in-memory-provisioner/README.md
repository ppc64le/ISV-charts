# In Memory Provisioner for Knative Eventing

This chart installs In Memory Provisioner components for Knative Eventing.
[Knative](https://github.com/knative/) extends Kubernetes to provide a set of middleware components that are essential to build modern, source-centric, and container-based applications that can run anywhere: on premises, in the cloud, or even in a third-party data center.

## Introduction

This chart is a subchart of Knative Eventing. It installs In Memory Provisioner. Visit [Eventing](https://github.com/knative/eventing/blob/master/README.md) to find out more about Knative Eventing.

## Chart Details

- Internal Services:
    - in-memory-channel-controller, in-memory-channel-dispatcher, in-memory-channel

- Knative In Memory provisioner Pods:
    - Deployments: in-memory-channel-controller, in-memory-channel-dispatcher
    - ClusterChannelProvisioner: in-memory-channel

## Prerequisites

- Requires kubectl v1.10+.
- Knative requires a Kubernetes cluster v1.10 or newer with the
[MutatingAdmissionWebhook admission controller](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/#how-do-i-turn-on-an-admission-controller)
enabled.
- Requires Knative Eventing to be installed with this chart or previously be installed.
- Istio - You should have Istio installed on your Kubernetes cluster. If you do not have it installed already you can do so by following the steps mentioned here https://github.com/IBM/charts/tree/master/stable/ibm-istio

## Installing the Chart

Please ensure that you have reviewed the [prerequisites](#prerequisites).
To install the chart using helm cli:

Install In Memory provisioner for eventing
```
$ helm install ./knative/charts/eventing/charts/in-memory-provisioner [--tls]
```

### Configuration

[Values.yaml](./values.yaml) outlines the configuration options that are supported by this chart.

### Verifying the Chart

To verify all Pods are running, try:
```bash
$ helm status <my-release> [--tls]
```

## Uninstalling the Chart

To uninstall/delete the deployment:

```bash
$ helm delete <my-release> --purge [--tls]
```

To uninstall/delete the crds:
```bash
$ kubectl delete --filename knative/all-crds.yaml
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Limitations

You must use `knative-eventing` namespace to install Knative Eventing.

## Documentation

To learn more about Knative in general, see the [Overview](https://github.com/knative/docs/blob/master/README.md).

# Support

If you're a developer, operator, or contributor trying to use Knative, the
following resources are available for you:

- [Knative Users](https://groups.google.com/forum/#!forum/knative-users)
- [Knative Developers](https://groups.google.com/forum/#!forum/knative-dev)

For contributors to Knative, we also have [Knative Slack](https://slack.knative.dev).
