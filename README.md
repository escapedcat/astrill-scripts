# astrill-scripts
a bunch of scripts to do split routing with astrill

you still need:

- astrill account + configs
- an internet connection
- dnsmasq or something similar to also do split DNS

if you're running DD-WRT, you may want to use this:

	https://www.astrill.com/dd-wrt.php

but, of course, these routers are shit anyways.

## usage for dummies

### add cronjob for `check` script
`crontab -e`
```
* * * * * /usr/local/Astrill/check
```


### add script to pppoe up
`/etc/ppp/ip-up.local`
```
/usr/local/Astrill/restart &
```

#### tips & hints
- remove TCP astrill connections from available connections, because...
- logs go to `Astrill/logs/`