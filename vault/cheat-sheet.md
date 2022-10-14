# vault cli cheat sheet

## vault cli commands

```text
# Check the status of the vault server
vault status

# List secret engines
vault secrets list

# Read a secret from a kv secret engine
vault kv get --format=<yaml/json/table> <secret_engine_name/secret_path>
vault kv get --format=<yaml/json/table> -mount=<secret_engine_name> <secret_path>
vault read --format=<yaml/json/table> <secret_engine_name>/data/<secret_path>
```

## References

* [vault cli overview](https://www.vaultproject.io/docs/commands)
