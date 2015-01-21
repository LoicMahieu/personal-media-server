
## ubuntu desktop
```
docker run \
  -it \
  --rm \
  -p 5901:5901 \
  -e USER=root \
  dockerfile/ubuntu-desktop \
    bash \
     -c "vncserver :1 \
     -geometry 1280x800 \
     -depth 24 && tail -F /root/.vnc/*.log"

docker run \
  -it \
  --rm \
  -e "USER=root" \
  -p 5901:5901 \
  dockerfile/ubuntu-desktop \
  /bin/sh \
    -c "vncserver :1 \
    -geometry 1280x800 \
    -depth 24; tail -f ~/.vnc/*.log"
```
