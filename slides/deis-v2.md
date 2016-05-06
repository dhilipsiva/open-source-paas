##  Deis V2

Currently Beta3

Buildpacks / Dockerfiles

Expected stable version to release on June 8, 2016: https://github.com/deis/workflow/milestones

```sh
# On Local
gcloud container clusters create deis-paas
helm target
helm repo add deis https://github.com/deis/charts
helm fetch deis/workflow-beta3
helm generate -f -x manifests workflow-beta3
helm install workflow-beta3
kubectl get pods --namespace=deis
kubectl --kubeconfig=kubeconfig proxy &

# Client
deis register http://deis.example.com
deis login http://deis.example.com
deis create appknoxp-app --buildpack heroku/python
git push heroku master
deis apps:scale web=2
```
