### 3. Renew commands
```bash
# Check what would be the result
letsencrypt renew --dry-run

# DO IT!
letsencrypt renew
```

```
Requesting root privileges to run letsencrypt...
   /root/.local/share/letsencrypt/bin/letsencrypt renew
Processing /etc/letsencrypt/renewal/www.gableroux.com.conf
Processing /etc/letsencrypt/renewal/gableroux.com.conf

The following certs are not due for renewal yet:
  /etc/letsencrypt/live/www.gableroux.com/fullchain.pem (skipped)
  /etc/letsencrypt/live/gableroux.com/fullchain.pem (skipped)
No renewals were attempted.
```

Run this in a daily random cron job and you're done
