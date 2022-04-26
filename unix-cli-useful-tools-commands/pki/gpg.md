# gpg

```text
# search a gpg public key
gpg --search-keys <email/id/etc>

# download a public key
gpg --recv-keys <id>

# specify key server
gpg --keyserver <server> --recv-keys <id>
gpg --keyserver hkps://keys.openpgp.org --recv-keys 288DD1632F6E8951
```

More Info:

* [gpg2](https://linux.die.net/man/1/gpg2)
* [gpg documentation](https://gnupg.org/documentation/manuals/gnupg/)