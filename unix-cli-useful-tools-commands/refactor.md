# Unix Cli Useful Tools and Commands

## Load/Performance Tests Tools

### Apache Benchmark

```bash
# Perform http load test with 10 request of concurrency and with a total of 1000 requests to https://test-site.com/api/ site
ab -c 10 -n 1000 https://test-site.com/api/
```

### Apache Jmeter

```bash
TBC
```

### stress

It is recommended to run this tool with root privileges.

```bash
# Stress using CPU-bound task
stress --cpu 4 --timeout 10 --verbose

# Stress using IO-bound task
stress --io 2 --timeout 20 --quiet

# Stress system memory
stress-ng --vm 1 --vm-bytes 5G
```

More Info:
* https://linux.die.net/man/1/stress
* https://www.tecmint.com/linux-cpu-load-stress-test-with-stress-ng-tool/

## stress-ng (stress next-generation)

It is recommended to run this tool with root privileges.

```bash
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
* https://manpages.ubuntu.com/manpages/artful/man1/stress-ng.1.html
* https://www.tecmint.com/linux-cpu-load-stress-test-with-stress-ng-tool/2/

## HTTP Tools

### curl

```bash
# Make an HTTP request passing a user
curl -u user http://localhost:8080

# Make an HTTP request passing a user and a password
curl -u user:password http://localhost:8080

# Make a HTTP request passing custom headers
curl https://reqbin.com/echo/get/json -H "X-Custom-Header: value" -H "Content-Type: application/json"

# Make a HTTP request without certificate checking
curl -k [options] [url]
curl --insecure [options] [url]

# Make a HTTP request sending a client certificate to perform mutual authentication (mutual TLS)
curl https://test.host.com --cert [certificate.crt/pem] --key [privatekey.key/pem]
curl https://test.host.com --cert [certificate.crt/pem]:[passphrase] --key [privatekey.key/pem]
curl https://test.host.com --cert [certificate.crt/pem]:[passphrase] --key [privatekey.key/pem] --cacert [cacer.crt/pem]

```

Notes:

* `--cacert` flag will be used so curl can trust in the certificate presented by the server. This verification can be skipped using `-k` or `--insecure` flags

More Info:

* https://reqbin.com/curl
* https://reqbin.com/
* https://smallstep.com/hello-mtls/doc/client/curl

### wget

```bash
TBC
```

## Change User/Privilege Escalation

### gosu

```bash
TBC
```

### su

```bash
TBC
```

### sudo

```bash
TBC
```

## Process and Resources Analysis 

### General Tools

#### htop

```bash
TBC
```

More Info:

* https://peteris.rocks/blog/htop/

#### kill

```bash
# List available signals
kill -l

# Send SIGHUP Signal to a process
kill -1 <process_id>
```

More Info:

* [sending signal to procesess](https://bash.cyberciti.biz/guide/Sending_signal_to_Processes)

#### lsof

```bash
TBC
```

#### ps

```bash
# Get a hierarchical way inter-processes dependency, a snapshot of all running processes and information related to threads corresponding to a particular process 
ps -ef --forest
```

#### systemd

```bash
TBC
```

#### supervisord

```bash
TBC
```

#### top

```bash
TBC
```

### Memory Related Tools

#### free

```bash
# Check Free Memory
free -m
```

#### vmstat

```bash
# Check Free Memory
vmstat
```

## Log Analysis

### journald

```bash
# Check logs of nginx service unit
journalctl -u nginx.service [--since today]

# Check logs of kubelet service unit retrieving the latest log entries first
journalctl -u kubelet.service -r
```

More Info:

* https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs

## Network Tools

### dig

```bash
TBC
```

### nmap

```bash
TBC
```

### netcat

```bash
# Open TCP Port
nc -l 8080
```

### netstat

```bash
TBC
```

### nslookup

```bash
# Resolve a host name
nslookup [dns-hosname] [dns-server]
nslookup www.google.com 8.8.8.8
```

### ping

```bash
TBC
```

### ssh

```bash
# Connecting to a server specifying a user and a private key bypassing the fingerprint checking of the host
ssh -l [username] -i [path_to_private_key_file] -o "StrictHostKeyChecking no"
```

### tcpdump

```bash
# Filter ICMP Packages
tcpdump -i [interface_name] icmp

# Filter udp packages
tcpdump -i [interface_name] udp

# Filter tcp packages
tcpdump -i [interface_name] tcp

# Show IP Addresess instead of DNS names
tcpdump -n -i [interface_name]
```

More Info:

* https://www.tcpdump.org/manpages/tcpdump.1.html
* https://danielmiessler.com/study/tcpdump/

### telnet

```bash
TBC
```

## Shell tools/commands

### awk

```bash
TBC
```

More Info:

* https://linux.die.net/man/1/awk
* https://likegeeks.com/awk-command/

### echo

```bash
TBC
```

More Info:

* https://linuxize.com/post/echo-command-in-linux-with-examples/

### cut

```bash
# Split by spaces and get the second splitted field
echo "Lorem ipsum dolor sit amet" | cut -d ' ' -f 2
```

More info:

* https://www.geeksforgeeks.org/cut-command-linux-examples/

### grep

```bash
# Show previous and next lines when grepping
grep -B 3 -A 3 foo README.txt

# Use OR function to search several expressions
grep 'expresion1\|expresion2\|expresion3' filename
```

More Info:

* https://www.digitalocean.com/community/tutorials/using-grep-regular-expressions-to-search-for-text-patterns-in-linux
* https://www.thegeekstuff.com/2011/10/grep-or-and-not-operators/

### head

```bash
# Print the beginning n=10 lines of a file
head -n 10 file.txt
```

More Info:

* https://man7.org/linux/man-pages/man1/head.1.html

### set

```bash
# Exit immediately if a command exits with a non-zero status
set -e
```

More Info:

* https://www.gnu.org/software/bash/manual/html_node/The-Set-Builtin.html
* https://www.javatpoint.com/linux-set-command

### sed

```bash
TBC
```

More Info:

* https://www.digitalocean.com/community/tutorials/the-basics-of-using-the-sed-stream-editor-to-manipulate-text-in-linux
* https://www.gnu.org/software/sed/manual/sed.html

### xargs

```bash
# Delete all the kubernetes pods that have error state
kubectl get pods | grep Error | awk '{print $1}' | xargs kubectl delete pod
```

More Info:

* https://man7.org/linux/man-pages/man1/xargs.1.html
* https://www.cyberciti.biz/faq/linux-unix-bsd-xargs-construct-argument-lists-utility/