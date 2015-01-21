
```
rsync \
  -n \
  -avP \
  -e ssh \
  --bwlimit=1000 \
  --exclude='.DS_Store' \
  /Volumes/Data\ HD/Videos/Films/ \
  loic@192.168.1.102:/media/larzdata/Videos/Movies/

rsync \
  -n \
  -avP \
  -e ssh \
  --exclude='.DS_Store' \
  "/Volumes/Data HD/Videos/Séries/" \
  loic@192.168.1.102:/media/larzdata/Videos/TVShows/
```
