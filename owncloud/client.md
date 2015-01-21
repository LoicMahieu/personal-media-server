
# owncloudcmd

API: http://doc.owncloud.org/desktop/1.7/advancedusage.html
https://github.com/owncloud/client/blob/master/doc/owncloudcmd.1.rst

http://www.ossramblings.com/headless-owncloud-linux-sync


# docker-owncloudcmd

https://github.com/LoicMahieu/docker-owncloudcmd
https://registry.hub.docker.com/u/loicmahieu/owncloudcmd

```
docker pull loicmahieu/owncloudcmd
```

```
docker run \
  --rm \
  -t owncloudcmd \
  [OPTION] \
  <source_dir> \
  <server_url>
```


```
docker run \
  --rm \
  -v /home/loic/Owncloud/config:/owncloud/config \
  -v /home/loic/Owncloud/data:/owncloud/config \
  -t owncloudcmd \
  --config /owncloud/config/owncloud.cfg \
  <source_dir> \
  ownclouds://loic:password123@my.cloud.url.com/remote.php/webdav
```

# webdav

http://doc.owncloud.org/server/7.0/user_manual/files/files.html
