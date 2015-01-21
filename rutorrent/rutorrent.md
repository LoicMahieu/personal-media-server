```
docker run \
  -d \
  -t \
  --name rtorrent-rutorrent \
  -p 8080:80 \
  -p 49160:49160/udp \
  -p 49161:19161 \
  -v /media/larzdata/downloads:/downloads \
  diameter/rtorrent-rutorrent:64
```

# https://github.com/Micka33/docker-rtorrent-rutorrent
```
docker build -t rutorrent_image ./docker_files
docker run \
  --name rutorrent \
  -d \
  -p 8082:80 \
  -p 0.0.0.0:63256:63256 \
  -v /media/larzdata/downloads:/root/mounted \
  rutorrent_image
```
