##  [Dokku](http://dokku.viewdocs.io/dokku/)

Debian OS (Preferably Ubuntu 14.04)

```sh
# On Local
# instance --image "/ubuntu-os-cloud/ubuntu-1404-trusty-v20160406"
# ssh


# On Host
wget https://raw.githubusercontent.com/dokku/dokku/v0.5.6/bootstrap.sh
sudo DOKKU_TAG=v0.5.6 bash bootstrap.sh
dokku apps:create apknox-app
dokku plugin:install https://github.com/dokku/dokku-postgres.git
dokku postgres:create appknox-db
dokku postgres:link appknox-db appknox-app
dokku ps:scale web=2

# On Local
git remote add dokku dokku@dokku.me:appknox-app
git push dokku master # App will be deployed to http://appknox-app.example.com
```


### Services

Through Plugins - https://github.com/dokku
