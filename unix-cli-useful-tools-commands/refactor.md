# Unix Cli Useful Tools and Commands

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