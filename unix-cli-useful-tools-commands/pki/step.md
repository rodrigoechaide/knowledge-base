# step

```text
# Check certificate validity
step certificate inspect https://smallstep.com --format json | jq .validity

# Inspect a certificate
step certificate inspect https://smallstep.com --format json

# Generate a elliptic curve P-256 key pair
step crypto keypair --kty EC --curve P-256 k.pub k.prv
```

More Info:

* [design-document](https://smallstep.com/docs/design-document)
* [step-ca](https://smallstep.com/docs/step-ca)
* [everything-pki](https://smallstep.com/blog/everything-pki/)