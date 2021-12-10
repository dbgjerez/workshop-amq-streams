# 

# Prerequisites
* ArgoCD or Openshift GitOps operator installed

# Start up
Initialize the ArgoCD server
```bash
oc apply -f argocd/argocd-server.yaml
```

Bootstrap the cluster and ArgoCD configuration
```bash
oc apply -f argocd/argocd-app-bootstrap.yaml
```

The argocd application bootstrap uses the GitOps power to install and configure all the pieces that the cluster needs to run the repository use case.