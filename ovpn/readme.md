
https://registry.hub.docker.com/u/kylemanna/openvpn/


```
OVPN_DATA="ovpn-data"
OVPN_SERVER="ovpn-server"
OVPN_DOMAIN="loic-home.igloo.be"
```

# Create openvpn-data
```
docker run --name $OVPN_DATA -v /etc/openvpn busybox
docker run --volumes-from $OVPN_DATA --rm kylemanna/openvpn ovpn_genconfig -u udp://$OVPN_DOMAIN
docker run --volumes-from $OVPN_DATA --rm -it kylemanna/openvpn ovpn_initpki
```

# Run server
```
docker run \
  --name $OVPN_SERVER \
  --volumes-from $OVPN_DATA \
  -d \
  -p 1194:1194/udp \
  --cap-add=NET_ADMIN \
  --restart="always" \
  kylemanna/openvpn
```

# create client without password
```
docker run --volumes-from $OVPN_DATA --rm -it kylemanna/openvpn easyrsa build-client-full loic nopass
docker run --volumes-from $OVPN_DATA --rm kylemanna/openvpn ovpn_getclient loic > loic.ovpn
```
