
# ArgoCD Application Sets
You can read more about application sets here: 
https://cloud.redhat.com/blog/getting-started-with-applicationsets

## To deploy the application, you can run the application set yaml in the 

```
oc apply -k deploy/
```

## To delete the application, you can delete the application set and the app project 

Just delete the application set and the ArgoCD ApplicationSet contoller will do the magic!

```
oc delete applicationset --all -n openshift-gitops
```

## Links of interest

* [Getting Started with Application Sets](https://cloud.redhat.com/blog/getting-started-with-applicationsets)
* [GitOps Guide to the Galaxy (Ep 15): Introducing the App of Apps and ApplicationSets](https://www.youtube.com/watch?v=HqzUIJMYnfY&ab_channel=OpenShift)
=======
# simple-gitops
>>>>>>> 4f554bf12a5c469948aa898f5b33fc86664c203f
