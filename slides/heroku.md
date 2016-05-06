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
