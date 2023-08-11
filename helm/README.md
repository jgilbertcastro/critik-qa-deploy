# Deploy to cluster

1.	review and update is needed the value file and the appversion on chart.yaml

2.	create the namespace for the new deploy
```
kubectl create ns feature1-gis
```
3.	create the secret for the new deploy

4.	position your promt in the helm dir in this repo

```
cd helm
```

5.	Install the chart in the namespace previous created.

```
helm install feature1-gis-auth -n feature1-gis -f values.yaml .
```

# Upgrade a previous Deploy

1.	review and update is needed the value file and the appversion on chart.yaml

2.	position your promt in the helm dir in this repo

```
cd helm
```

3.	upgrade the installed helm deploy with the following command.

```
helm upgrade feature1-gis-auth -n feature1-gis -f values.yaml .
```


# Important note

You need to have knowledge and access to the following resources to deploy for the first time

* DNS
* kubernetes secret
* helm commands
* kubernetes namespace
