# crontab

### PPPoE daily redial at every morning 6 AM

    0 6 * * * /usr/sbin/wicked ifdown ppp0; /usr/sbin/wicked ifup ppp0

### DDNS service by he.net (update every 5 mins, IPv4 only)

    */5 * * * * /usr/bin/curl -4 -s "http://host.example.com:token@dyn.dns.he.net/nic/update?hostname=host.example.com" >/dev/null 2>&1
