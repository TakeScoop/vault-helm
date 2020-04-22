# Vault Helm Chart

**Maintainer:** Platform Team (Slack: [#dev-platform](https://takescoop.slack.com/app_redirect?channel=dev-platform))

This repository publishes the official HashiCorp Helm chart to Scoop's Artifactory Helm repository. Hashicorp does [not offer a hosted chart](https://github.com/hashicorp/vault-helm#usage), however it is much more convenient for our infrastructure to deploy hosted charts than to download a chart manually and deploy from a file directory. 

## Publish a new version

- Ensure that your desired chart version has been released on [hashicorps/vault-helm](https://github.com/hashicorp/vault-helm/releases).
- In a new branch named the version youre releaseing (ex `0.6.0`), update the `version` file in the project root

```diff
- 0.5.0
+ 0.6.0
```

- Push your branch and merge it to master. CircleCI will download the chart version from `hashicorps/vault-helm` and push the chart to our Artifactory Helm repository.
