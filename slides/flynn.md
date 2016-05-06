##  Flynn

```sh
# On local Machine
L=/usr/local/bin/flynn && curl -sSL -A "`uname -sp`" https://dl.flynn.io/cli | zcat >$L && chmod +x $L

git clone https://github.com/flynn/nodejs-flynn-example.git
cd nodejs-flynn-example
flynn create example
git push flynn master

# Procfile

# Scale
flynn scale web=3

```
