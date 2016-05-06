##  Heroku

* Buildpacks
* Procfile

```shell
heroku login
heroku create appknox
heroku addons:create heroku-postgresql:appknox-db
git push heroku master
heroku ps:scale web=2
```



| Name | Deis | Flynn | Dokku |
| --- | --- | --- | --- |
| Cluster | Yes | Yes | No |
| Buildpacks | Yes | No | Yes |
| Services | Kubernetes | Docker | Plugins |
| Host OS | Kuberbetes | AWS / Google / ubuntu SSH | Docker |
| GUI Setup | No | Yes | No |
