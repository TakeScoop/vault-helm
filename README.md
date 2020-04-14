# Vault Helm Chart [![CircleCI](https://circleci.com/gh/TakeScoop/vault-helm/tree/master.svg?style=svg)](https://circleci.com/gh/TakeScoop/vault-helm/tree/master)

**Maintainer:** Platform Team (Slack: [#dev-platform](https://takescoop.slack.com/app_redirect?channel=dev-platform))

This repository contains the official HashiCorp Helm chart for installing
and configuring Vault on Kubernetes. This chart supports multiple use
cases of Vault on Kubernetes depending on the values provided.

For full documentation on this Helm chart along with all the ways you can
use Vault with Kubernetes, please see the
[Vault and Kubernetes documentation](https://www.vaultproject.io/docs/platform/k8s/).

## Why the fork?

The vault-helm repository is fairly new. When started integrating it into our clusters, there were three distinct pieces that were missing:
- Published to a repository
    - While we could download a tagged release as [noted in the docs](https://github.com/hashicorp/vault-helm/tree/d696408fae1524979c82e9b9ae98a63d4f00fad7#usage), this is a bit too messy for us to include in our cluster base installation.

When these three things are completed, we can celebrate and move off of the fork, onto the upstream chart.

## Prerequisites

To use the charts here, [Helm](https://helm.sh/) must be installed in your
Kubernetes cluster. Setting up Kubernetes and Helm and is outside the scope
of this README. Please refer to the Kubernetes and Helm documentation.

The versions required are:

  * **Helm 3.0+** - This is the earliest version of Helm tested. It is possible
    it works with earlier versions but this chart is untested for those versions.
  * **Kubernetes 1.9+** - This is the earliest version of Kubernetes tested.
    It is possible that this chart works with earlier versions but it is
    untested. Other versions verified are Kubernetes 1.10, 1.11.

## Usage

For now, we do not host a chart repository. To use the charts, you must
download this repository and unpack it into a directory. Either
[download a tagged release](https://github.com/hashicorp/vault-helm/releases) or
use `git checkout` to a tagged release.
Assuming this repository was unpacked into the directory `vault-helm`, the chart can
then be installed directly:

    helm install ./vault-helm

Please see the many options supported in the `values.yaml`
file. These are also fully documented directly on the
[Vault website](https://www.vaultproject.io/docs/platform/k8s/helm).
