# Package: Metrics Server

Deploy the [Core Metrics Server](https://github.com/defenseunicorns/uds-core) package configured to your environment.

- powers `kubectl top node/pod` commands
- metrics-server does not probe containers directly, and it does not contact the container runtime. It only talks to the Kubelet on each node.
- Each Kubelet exposes the Summary API (/stats/summary).
- metrics-server registers an aggregated APIService with the apiserver
  - exposes an apiservice: `v1beta1.metrics.k8s.io`
