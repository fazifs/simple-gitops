
# ArgoCD Application Sets
You can read more about application sets here: 
https://cloud.redhat.com/blog/getting-started-with-applicationsets

## What does this do
The argocd application set in this repo deploys the bgd and pacman apps from the following repository https://github.com/RedHat-EMEA-SSA-Team/ns-apps, the appsets branch.

## How to deply 
To deploy the application, you can run the appproject and applicatioset objects, by running the yaml files in application-sets and app-projects directories seperately or run the kustomization file in the deploy folder to include both at the same time.

```
oc apply -k deploy/
```

## How to delete
To delete the application, you can delete the application set and the app project 

Just delete the application set and the ArgoCD ApplicationSet contoller will do the magic!

```
oc delete applicationset --all -n openshift-gitops
```