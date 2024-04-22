## Helm Install
Clone down the repo and do the install
`git clone git@github.com:argoproj/argo-helm.git`
`cd argo-helm/charts/argo-cd/`
`helm install argocd -n argocd . --debug`


## OCP Install of ArgoCD

1. Make sure to delete the `namespaces` value in the cluster secret:
The secret name is: `argocd-default-cluster-config`

delete the following:
```
namespaces: YXJnb2Nk
```

2. To enable the ability for argocd to create cluster level resources in OCP add the following
`clusterResources: dHJ1ZQ==` to the secret `argocd-default-cluster-config`
