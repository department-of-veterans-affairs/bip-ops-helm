# Benefits Integrated Platform Operational Helm Charts

## Summary

The purpose of this repository is to house helm charts for operations tasks. This is to include temporary charts used for troubleshooting ongoing issue and also long running apps that help facilitate tenant workloads (eg: s3 proxies).

To use this repository, you must first add it to [helm](https://helm.sh):

```sh
helm repo add bip https://department-of-veterans-affairs.github.io/bip-ops-helm/
```

Refresh your local cache:

```sh
helm repo update
```

Install a chart from the repo:

```sh
helm install dump-headers bip/dump-headers --set ingress.host=dump-headers.bip.va.gov
```

## Charts

Some, but not all, charts are listed below for reference:

| Name | Purpose |
| --- | --- |
| dump-headers | A single pod that dumps http headers to stdout for debugging and testing. |
