With this [Piku](https://github.com/rcarmo/piku) application you can deploy a [Bittorrent tracker](https://www.npmjs.com/package/bittorrent-tracker) with one `git push`.

Note: this requires `nodeenv` on the Piku server. You can install it with `piku-bootstrap root@YOURSERVER nodeenv.yml`.

```
git remote add piku piku@yourserver.net:bittorrent-tracker
git push piku master
piku config:set NGINX_SERVER_NAME=tracker.somedomain.net
```

 * `NGINX_SERVER_NAME` (optional) is the external domain name you want for the Bittorrent tracker server. The domain must point at the machine already.

Once it's up you can browse to `tracker.somedomain.net/stats` to see it in operation.
