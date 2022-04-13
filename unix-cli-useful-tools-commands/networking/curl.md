# curl cheat sheet

```text
# Make an HTTP request passing a user
curl -u user http://localhost:8080

# Make an HTTP request passing a user and a password
curl -u user:password http://localhost:8080

# Make a HTTP request passing custom headers
curl https://reqbin.com/echo/get/json -H "X-Custom-Header: value" -H "Content-Type: application/json"

# Make a HTTP request without certificate checking
curl -k [options] [url]
curl --insecure [options] [url]

# Follow HTTP redirects
curl -L [url]

# Make a HTTP request sending a client certificate to perform mutual authentication (mutual TLS)
curl https://test.host.com --cert [certificate.crt/pem] --key [privatekey.key/pem]
curl https://test.host.com --cert [certificate.crt/pem]:[passphrase] --key [privatekey.key/pem]
curl https://test.host.com --cert [certificate.crt/pem]:[passphrase] --key [privatekey.key/pem] --cacert [cacer.crt/pem]

# Full curl request example
curl --header "Content-Type: application/json" --request POST --data '{ "inputs": {"key1":"value1", "key2":"value2", "key3":"value3"} }' https://test.endpoint.com/test -u <username> -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:90.0) Gecko/20100101 Firefox/90.0'
```

Notes:

* `--cacert` flag will be used so curl can trust in the certificate presented by the server. This verification can be skipped using `-k` or `--insecure` flags

More Info:

* [https://reqbin.com/curl](https://reqbin.com/curl)
* [https://smallstep.com/hello-mtls/doc/client/curl](https://smallstep.com/hello-mtls/doc/client/curl)