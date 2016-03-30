### 2. Run setup commands
```bash
# Using apache plugin
letsencrypt --apache

# Using Webroot plugin
letsencrypt certonly --webroot \
-w /var/www/gableroux.com -d gableroux.com -d www.gableroux.com \
-w /var/www/example.com -d example.com -d www.example.com \
-w /var/www/$DOMAIN -d $DOMAIN -d www.$DOMAIN

# ok you get it ;)
```
