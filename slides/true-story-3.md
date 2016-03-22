##  Investigate

* Mobiles (ios and Android) have missing chains
* Discover stunnel
* Read config
* Fun begins:  
  https://certs.godaddy.com/repository
* Find out you need  
  *all_intermediate_ca_certificates.p7b*

Oh great, `p7b`, not the right format, we need `pem`

    openssl pkcs7 -inform der -in a.p7b -print_certs -out a.pem

<small>ref: [serverfault: How do I ensure that stunnel sends all intermediate ca certs](http://serverfault.com/questions/254795/how-do-i-ensure-that-stunnel-sends-all-intermediate-ca-certs)</small>
