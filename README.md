# igou-node-bootstrap

Nodes in my cluster are bootstrapped using cloud-init using these manifests. One day I will migrate to netbooting - but the support for Pis is too limited right now for me to feel it's worth dealing with the issues.

External Ingress k3os nodes in AWS are not configured using code in this repository. That is done via the terraform in igou-io/igou-infrastructure after the cluster is installed.
