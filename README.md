# http-cache-proxy
A versatile caching http proxy

## Features
This project should include the following features

1. HTTP(S) proxy to upstream servers
2. Configurable Cache control settings per upstream server
3. Configurable HTTP/TLS settings per upstream server

## Config Example
```
proxy:
- name: gravatar
  description: A public service which provides a user's avatar image
  incoming:
    host: gravatar.svc.cluster.local
  upstream:
    host: gravatar.com
    tls: default
  cache:
    enabled: true
    ttl: 1month

tls_configs:
- name: default
  cert_file: /etc/pki/ssl/client.crt
  key_file: /etc/pki/ssl/client.key
  ca_file: /etc/pki/ssl/ca.pem
```
