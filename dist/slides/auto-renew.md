### What I prefer using:

```bash
letsencrypt-auto certonly -a webroot --renew-by-default \
--config /usr/local/etc/le-renew-webroot.ini
```

`le-renew-webroot.ini`
```
rsa-key-size = 4096
email = lebreton.gabriel@gmail.com
domains = gableroux.com, www.gableroux.com
webroot-path = /var/www/
```
<small>_Rendred by jinja template in salt btw_</small>
