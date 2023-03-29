This README.md shows how to install the workshop using the GitOps philosophy.

# Installation

Exists a few ways to install ArgoCD, in this case, we'll use the "OpenShift GitOps operator". 

```bash
oc apply -f argocd/argocd-operator.yaml
```

Like we're going to work with special objects which provide the Kafka Operator, we must grant privileges to ArgoCD service account. I've granted ClusterRole admin, but you can create your own more restricted role and grant it. 

```bash
oc apply -f argocd/cluster-role.yaml
```

And finally, apply the bootstrap application:

```bash
oc apply -f argocd/argocd-app-bootstrap.yaml
```