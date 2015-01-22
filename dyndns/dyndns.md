
# Update IP via crontab
```
  */5 *  *   *   *     curl http://larzhome.hopper.pw:aaaa@ipv4.www.hopper.pw/nic/update > /dev/null 2>&1
  */5 *  *   *   *     echo url="https://www.duckdns.org/update?domains=larzhome&token=aaaa&ip=" | curl -k -K - > /dev/null 2>&1
```
