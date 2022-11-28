# Mastodon chart

A Helm chart for [Mastodon](https://github.com/tootsuite/mastodon).
Mastodon is a free, open-source social network server.

This Helm chart was designed/tested with:

| Package | Version |
| ------- | ------- |
| Mastodon | `tootsuite/mastodon:v4.0.2` |
| Kubernetes | v1.24 |
| Cilium | v1.12.4 |
| K3s worker nodes | Arm64 arch  |

## How to Install?
Copy and edit `secrets.yaml.sample` and `values.yaml.sample` to provide your
own `secrets.yaml` and `values.yaml` files, and then deploy the Helm chart
with: 

```
cd mastodon-chart
helm upgrade --install --create-namespace --namespace=mastodon -f secrets.yaml mastodon .
```

### Maintainer & License
Maintained by David Tham <davidthamwf@gmail.com>

Based on the original chart developed by Ladicle - https://github.com/Ladicle/mastodon-chart, and credit to upstream source Tim Walls <tim.walls@snowgoons.com> - for more information see here: https://snowgoons.ro/posts/2020-08-29-mastodon-on-kubernetes/
