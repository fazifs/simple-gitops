
# ArgoCD ApplicationSets
You can read more about argocd application sets [here](https://cloud.redhat.com/blog/getting-started-with-applicationsets).


## What does this repo do
The argocd applicationset in this repo deploys the bgd and pacman apps from the [following repository](https://github.com/RedHat-EMEA-SSA-Team/ns-apps), the **appsets** branch.

## How to deply 
To deploy the applicationset, you can run the appproject and applicatioset objects, by running the yaml files in application-sets and app-projects directories seperately or run the kustomization file in the deploy folder to include both at the same time.

```
oc apply -k deploy/
```

## How to delete
To delete the applications, you can delete the created argo applicationset and the appproject. 

1) To view the exising appsets and appprojetcs:

```
oc get applicationset -n openshift-gitops
```
```
oc get appproject -n openshift-gitops
```
The appset is called demo-app-set and the appproject is called demo-app-project.

2) To delete:
```
oc delete applicationset demp-app-set -n openshift-gitops
```
```
oc delete appproject demo-app-project -n openshift-gitops
```