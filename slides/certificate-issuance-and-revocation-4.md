## Revocation

* Agent signs a `revocation request` with the key pair authorized for `gableroux.com`
* Let’s Encrypt CA verifies that the request is authorized
* Publishes revocation information into the normal revocation channels
  * [Certificate revocation list (CRLs)](https://en.wikipedia.org/wiki/Revocation_list)
  * [Online Certificate Status Protocol (OCSP)](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol)

<small>Source: https://letsencrypt.org/how-it-works/</small>
