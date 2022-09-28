
# Run Kong Gateway on EKS

## Prerequisites
* AWS account with access to EKS
* `aws` cli installed and logged into account
* [`eksctl`](https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html)
* [`helm`](https://helm.sh/docs/intro/install/)
* A domain name that's available for use with permissions to add DNS records

## Usage

* Modify `cluster.yaml` if desired
   * Verify region is as desired
* `eksctl create cluster -f cluster.yaml`
   * wait a long time...
* Follow the Kubernetes in the Cloud steps in the [helm quickstart](https://docs.konghq.com/gateway/latest/install/kubernetes/helm-quickstart/)
   * Update your DNS entry, use a CNAME

## Cleanup

* eksctl delete cluster -f cluster.yaml
* Cleanup any DNS records if desired
