##  nginx

```
## https redirect
server {
  listen 80;
  listen [::]:80;
  server_name gableroux.com;

  location ~ '/.well-known/acme-challenge' {
    default_type "text/plain";
    root /var/www;
  }

  location / {
    return 301 https://$server_name$request_uri;
  }
}

## www removal
server {
  listen 80;
  listen [::]:80;
  server_name www.gableroux.com;

  location ~ '/.well-known/acme-challenge' {
    default_type "text/plain";
    root /var/www;
  }

  location / {
    return 301 https://gableroux.com$request_uri;
  }
}

## Main server config
server {
  listen 443 ssl;
  server_name gableroux.com;
  root /var/www/gableroux.com/_site;

  index  index.html;

  ### SSL Config (using letsencrypt)
  ssl_certificate /etc/letsencrypt/live/gableroux.com/fullchain.pem;
  ssl_certificate_key /etc/letsencrypt/live/gableroux.com/privkey.pem;
  ssl_session_timeout 5m;
  ssl_session_cache shared:SSL:5m;

  # Generate ssl_dhparam using `openssl dhparam -out dhparams.pem 4096`
  ssl_dhparam /etc/nginx/dhparams.pem;
  ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
  ssl_prefer_server_ciphers on;
  ssl_ciphers 'EECDH+AESGCM:EDH+AESGCM:AES256+EECDH:AES256+EDH';

  ### Logs
  access_log  /var/log/nginx/gableroux.com.access.log;
  error_log   /var/log/nginx/gableroux.com.error.log;

  ### Serve root
  location / {
    root  /var/www/gableroux.com/_site;

    #### Todo: better 404
  }
}
```

