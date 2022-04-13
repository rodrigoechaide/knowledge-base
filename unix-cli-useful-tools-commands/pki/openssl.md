# openssl

## Certificates Format Conversions

```text
# Export a certificate plus the private key into a p12 file
openssl pkcs12 -export -clcerts -inkey [private.key] -in [certificate.crt] -out [mypkcs.p12] -name "Some Name"
```

## Key Pairs Generation

```text
# Generate a elliptic curve P-256 key pair
openssl ecparam -name prime256v1 -genkey -out k.prv
openssl ec -in k.prv -pubout -out k.pub
```

## CA and client/server certificates generation

```text
# Generate the CA Key and Certificate
openssl req -x509 -sha256 -newkey rsa:4096 -keyout ca.key -out ca.crt -days 3560 -nodes -subj '/CN=Fern Cert Authority'

# Generate the Server Key, and Certificate and Sign with the CA Certificate
openssl req -new -newkey rsa:4096 -keyout server.key -out server.csr -nodes -subj '/CN=meow.com'
openssl x509 -req -sha256 -days 3650 -in server.csr -CA ca.crt -CAkey ca.key -set_serial 01 -out server.crt

# Generate the Client Key, and Certificate and Sign with the CA Certificate
openssl req -new -newkey rsa:4096 -keyout client.key -out client.csr -nodes -subj '/CN=Fern'
openssl x509 -req -sha256 -days 3650 -in client.csr -CA ca.crt -CAkey ca.key -set_serial 02 -out client.crt

# Sign a client/server certificate using a CA certificate and specify Subject Alternate Names
openssl x509 -req -extfile <(printf "subjectAltName=DNS:alternative.dns.name.one,DNS:alternative.dns.name.two") -days 3650 -in server.csr -CA ca.crt -CAkey ca.key -CAcreateserial -out server.crt

# Check the created certificate
openssl x509 -in server.crt -text -noout
```

More Info:

* [Creating a trusted CA and SAN certificate using OpenSSL](https://fabianlee.org/2018/02/17/ubuntu-creating-a-trusted-ca-and-san-certificate-using-openssl-on-ubuntu/)
* [OpenSSL Essentials](https://www.digitalocean.com/community/tutorials/openssl-essentials-working-with-ssl-certificates-private-keys-and-csrs)