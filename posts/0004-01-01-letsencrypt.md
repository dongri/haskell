---
title:  Let's Encrypt
author: D
---


```
./certbot-auto certonly --manual \
-d *.lgtm.lol \
-d lgtm.lol \
-m dongrify@gmail.com \
--agree-tos \
--manual-public-ip-logging-ok \
--preferred-challenges dns-01 \
--server https://acme-v02.api.letsencrypt.org/directory
```

```
dig _acme-challenge.lgtm.lol any @8.8.8.8
```
