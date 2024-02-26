# simple-nginx-forward-proxy
Sample docker configuration to build a nginx forward proxy on docker, based on https://github.com/theohbrothers/docker-nginx-forward-proxy.
This sample compose builds a nginx container that acts as forward proxy towards a SCIM server based on Tirasa [docker image](https://hub.docker.com/r/tirasa/scimple-server) of [SCIMple](https://github.com/apache/directory-scimple).

To run:

`docker compose up -d`

According to your requirements you may want to change configuration files:

* `./conf/nginx.conf`: nginx configuration file containing forward rules for path `/v2`
* `./conf/htpasswd`: to (optionally) add basic auth to the nginx server. Default user is `sample-user` with password `password`.
