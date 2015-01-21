
# owncloud server

https://registry.hub.docker.com/u/jchaney/owncloud/


# without db (sqllite)

```
docker run \
  -p 443:443 \
  --name owncloud-server \
  -v /media/larzdata/var/owncloud/data:/var/www/owncloud/data \
  -v /media/larzdata/var/owncloud/ssl:/root/ssl \
  -e "SSL_KEY=/root/ssl/owncloud.key" \
  -e "SSL_CERT=/root/ssl/owncloud.crt" \
  jchaney/owncloud
```
