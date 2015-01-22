
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
  -t loicmahieu/owncloudcmd \
  [OPTION] \
  <source_dir> \
  <server_url>
```

```
docker run \
  --rm \
  -v /home/loic/owncloud:/owncloud \
  -t loicmahieu/owncloudcmd \
  --trust \
  /owncloud \
  ownclouds://loic:password@192.168.1.102/owncloud/remote.php/webdav
```

### Mac
```
# not work
docker run \
  --rm \
  -v /Volumes/Data\ HD/owncloud:/owncloud \
  -t loicmahieu/owncloudcmd \
  --trust \
  /owncloud \
  ownclouds://loic:password@loic-home.igloo.be:14723/owncloud/remote.php/webdav

# bug
docker run \
  --rm \
  -v /Users/loicmahieu/ownCloudPersonal:/owncloud \
  -t loicmahieu/owncloudcmd \
  --trust \
  /owncloud \
  ownclouds://loic:password@192.168.1.102/owncloud/remote.php/webdav
```
```
# works on `boot2docker ssh`
docker run \
  --rm \
  -v /home/docker/owncloud:/owncloud \
  -t loicmahieu/owncloudcmd \
  --trust \
  /owncloud \
  ownclouds://loic:password@192.168.1.102/owncloud/remote.php/webdav
```

# webdav

http://doc.owncloud.org/server/7.0/user_manual/files/files.html
