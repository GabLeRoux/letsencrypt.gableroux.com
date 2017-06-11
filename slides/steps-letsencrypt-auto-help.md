### `./letsencrypt-auto --help`

```text
Checking for new version...
Requesting root privileges to run letsencrypt...
   /root/.local/share/letsencrypt/bin/letsencrypt --help

  letsencrypt-auto [SUBCOMMAND] [options] [-d domain] [-d domain] ...

The Let's Encrypt agent can obtain and install HTTPS/TLS/SSL certificates.  By
default, it will attempt to use a webserver both for obtaining and installing
the cert. Major SUBCOMMANDS are:

  (default) run        Obtain & install a cert in your current webserver
  certonly             Obtain cert, but do not install it (aka "auth")
  install              Install a previously obtained cert in a server
  renew                Renew previously obtained certs that are near expiry
  revoke               Revoke a previously obtained certificate
  rollback             Rollback server configuration changes made during install
  config_changes       Show changes made to server config during installation
  plugins              Display information about installed plugins

Choice of server plugins for obtaining and installing cert:

  --apache          Use the Apache plugin for authentication & installation
  --standalone      Run a standalone webserver for authentication
  (nginx support is experimental, buggy, and not installed by default)
  --webroot         Place files in a server's webroot folder for authentication

OR use different plugins to obtain (authenticate) the cert and then install it:

  --authenticator standalone --installer apache

More detailed help:

  -h, --help [topic]    print this message, or detailed help on a topic;
                        the available topics are:

   all, automation, paths, security, testing, or any of the subcommands or
   plugins (certonly, install, nginx, apache, standalone, webroot, etc)
```
