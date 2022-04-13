# stress cheat sheet

It is recommended to run this tool with root privileges.

```text
# Stress using CPU-bound task
stress --cpu 4 --timeout 10 --verbose

# Stress using IO-bound task
stress --io 2 --timeout 20 --quiet

# Stress system memory
stress-ng --vm 1 --vm-bytes 5G
```

More Info:

* [https://linux.die.net/man/1/stress](https://linux.die.net/man/1/stress)
* [https://www.tecmint.com/linux-cpu-load-stress-test-with-stress-ng-tool/](https://www.tecmint.com/linux-cpu-load-stress-test-with-stress-ng-tool/)
