# TLS Certificate and HTTPS

Setting up request encryption with HTTPS

## Expected features

- Automate certificate issuing
- Working with local development

## Difficulties

- Use of local domain name
- Trust self signed certificate

<!--
TLS: Transport Layer Security

Why do we want https ?

Encrypte request between server and client to prevent Man In The Middle attack.  
And since we wanted to use local domain name some navigator enforce https for specifique domain

Automate certificate issuing:
  - Provide low cost best pratices to developper
  - Fully automated every thing
  - Certificate have expiration date so need to reissue them.

Use of local domain prevent TLS certificate issuing since challenge can't be completed.  
Since using public Certificate Authority can't be done, make our own in local.  
Then just trust root certificate of Certificate Authority and all child certificate will be trusted.  
Example: Like DNA, parent certificate can be found with child certificate.  
-->