## Domain validation

* Let’s Encrypt identifies server by public key
* *First time*
  * Generates a new key pair
  * Proves to the Let’s Encrypt CA that the server controls one or more domains
* Agent asks the Let’s Encrypt CA **challenge** to prove that it controls `gableroux.com`
* Let’s Encrypt CA looks at the domain name and issue one or more sets of **challenges**

<small>Source: https://letsencrypt.org/how-it-works/</small>
