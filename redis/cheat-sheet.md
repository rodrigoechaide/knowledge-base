# redis-cli cheat sheet

## redis-cli no interactive commands

```text
# Get general information
redis-cli info

# Continuous stats mode
redis-cli --stat

# Scanning for big keys
redis-cli --bigkeys

# Check redis latency
redis-cli --latency
```

## redis-cli interactive commands

```text
# Select an specific Database
select <db number from 0 to 15>
select 15

# Get all keys
keys *

```

## References

[redis-cli manual](https://redis.io/docs/manual/cli/)
[data-types-tutorial](https://redis.io/docs/data-types/tutorial/)
[How To Manage Redis Databases and Keys](https://www.digitalocean.com/community/cheatsheets/how-to-manage-redis-databases-and-keys)
