# stress-ng (stress next-generation) cheat sheet

It is recommended to run this tool with root privileges.

```text
# Run 8 CPU stressors with a timeout of 60 seconds and a summary at the end of operations
stress-ng --cpu 8 --timeout 60 --metrics-brief

# Run 5 hdd stressors and stop after 100000 bogo operations.
stress-ng --hdd 5 --hdd-ops 100000

# Run 8 CPU stressors, 4 I/O stressors and 1 virtual memory stressor using 1GB of virtual memory for one minute
stress-ng --cpu 4 --io 4 --vm 1 --vm-bytes 1G --timeout 60s --metrics-brief

# Run 1 virtual memory stressor using 5GB of virtual memory
stress-ng --vm 1 --vm-bytes 5G
```

More Info:

* [https://manpages.ubuntu.com/manpages/artful/man1/stress-ng.1.html](https://manpages.ubuntu.com/manpages/artful/man1/stress-ng.1.html)
* [https://www.tecmint.com/linux-cpu-load-stress-test-with-stress-ng-tool/2/](https://www.tecmint.com/linux-cpu-load-stress-test-with-stress-ng-tool/2/)