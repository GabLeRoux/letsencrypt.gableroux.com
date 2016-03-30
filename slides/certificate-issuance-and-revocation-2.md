## Requesting and Renewing

* Agent constructs a [Certificate Signing Request](http://tools.ietf.org/html/rfc2986) (`CSR`) for domain
  * Asks the Let’s Encrypt CA to issue a certificate for `gableroux.com` with a specified public key
* `CSR` includes a signature by the private key corresponding to the public key in the `CSR`.
* Agent also signs the whole `CSR` with the authorized key
* Let’s Encrypt CA knows it’s authorized

<small>Source: https://letsencrypt.org/how-it-works/</small>
