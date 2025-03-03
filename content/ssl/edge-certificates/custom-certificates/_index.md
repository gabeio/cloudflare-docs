---
pcx_content_type: concept
title: Custom certificates
weight: 3
layout: single
---

# Custom certificates

{{<render file="_custom-certificates-definition.md">}}
<br/>

Custom certificates require that you [upload the certificate](uploading/), [manually renew these certificates](/ssl/edge-certificates/custom-certificates/renewing/), and upload these certificates in advance of expiration (otherwise your visitors will be unable to browse your site).

If you have first-level hostnames not covered by your custom SSL certificate, they will be covered by your [Universal SSL certificate](/ssl/edge-certificates/universal-ssl/), if enabled.

## Certificate Signing Requests (CSRs)

As part of this custom certificate process, you may also want to [generate a Certificate Signing Request (CSR)](/ssl/edge-certificates/additional-options/certificate-signing-requests/) so you can maintain control of your private key on Cloudflare.

## Keyless SSL

Typically, customers will upload both the SSL certificate and the private key. Those that wish to retain their private keys on their own infrastructure may wish to use [Keyless SSL](/ssl/keyless-ssl/).

## Geo Key Manager (private key restriction)

By default, private keys will be encrypted and securely distributed to each data center, where they can be utilized for local SSL/TLS termination. To restrict where these keys may be used, use [Geo Key Manager](/ssl/edge-certificates/geokey-manager/).

## Certificate packs

{{<render file="_custom-cert-ciphers.md">}}

Each pack only counts as one SSL certificate against your custom certificate quota.

{{<Aside type="note">}}

You cannot delete the primary certificate if secondary certificates are present in the pack.

{{</Aside>}}

## Availability

{{<feature-table id="ssl.custom_certificates">}}