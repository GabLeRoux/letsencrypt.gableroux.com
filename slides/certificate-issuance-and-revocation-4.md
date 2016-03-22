## Requesting and Renewing

* Let’s Encrypt CA receives the request
* Verifies both signatures.
* If everything looks good, issues a certificate with the public key from the `CSR` and returns it to the agent.

![Requesting and renewing][/resources/howitworks_certificate.png]

<small>Source: https://letsencrypt.org/how-it-works/</small>
