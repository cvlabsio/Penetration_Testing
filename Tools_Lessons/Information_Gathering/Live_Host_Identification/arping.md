### arping Usage Guide:

#### 1. Basic Usage:
To use arping, you typically provide the target host, IP address, or MAC address as an argument. For example:

```bash
arping 192.168.1.1
```

#### 2. Options:

- **-0**: Use this option to ping with source IP address 0.0.0.0. This can be useful when you haven't configured your interface yet.

Example:
```bash
arping -0 192.168.1.1
```

- **-a**: Audible ping. This option produces an audible sound when receiving a reply.

Example:
```bash
arping -a 192.168.1.1
```

- **-A**: Only count addresses matching the requested address. This option is mainly used for specific scanning purposes.

Example:
```bash
arping -A 192.168.1.0/24
```

- **-b**: Like `-0`, but with a broadcast source address (255.255.255.255). Note that this may not receive responses from some hosts due to unusual behavior.

Example:
```bash
arping -b 192.168.1.1
```

- **-B**: Use instead of the host if you want to address 255.255.255.255.

Example:
```bash
arping -B
```

- **-c count**: Only send the specified number of requests.

Example:
```bash
arping -c 5 192.168.1.1
```

- **-C count**: Only wait for this many replies, regardless of the `-c` and `-w` options.

Example:
```bash
arping -C 3 192.168.1.1
```

- **-d**: Find duplicate replies. Exit with 1 if there are answers from two different MAC addresses.

Example:
```bash
arping -d 192.168.1.1
```

- **-D**: Display answers as exclamation points and missing packets as dots.

Example:
```bash
arping -D 192.168.1.1
```

- **-e**: Like `-a`, but beep when there is no reply.

Example:
```bash
arping -e 192.168.1.1
```

- **-F**: Don't try to be smart about the interface name.

Example:
```bash
arping -F 192.168.1.1
```

- **-g group**: Set the group ID to this instead of the default nobody group.

Example:
```bash
arping -g 1000 192.168.1.1
```

- **-h**: Displays a help message and exits.

Example:
```bash
arping -h
```

- **-i interface**: Use the specified network interface.

Example:
```bash
arping -i eth0 192.168.1.1
```

- **-m type**: Type of timestamp to use for incoming packets.

Example:
```bash
arping -m timestamp 192.168.1.1
```

- **-q**: Does not display messages, except error messages.

Example:
```bash
arping -q 192.168.1.1
```

- **-Q pri**: 802.1p priority to set. Should be used with 802.1Q (-V). Defaults to 0.

Example:
```bash
arping -Q 5 192.168.1.1
```

- **-r**: Raw output: only the MAC/IP address is displayed for each reply.

Example:
```bash
arping -r 192.168.1.1
```

- **-R**: Raw output: Like `-r` but shows "the other one", can be combined with `-r`.

Example:
```bash
arping -R 192.168.1.1
```

- **-s MAC**: Set source MAC address.

Example:
```bash
arping -s 00:11:22:33:44:55 192.168.1.1
```

- **-S IP**: Like `-b` and `-0` but with a set source address.

Example:
```bash
arping -S 192.168.1.2 192.168.1.1
```

- **-t MAC**: Set target MAC address to use when pinging IP address.

Example:
```bash
arping -t 00:11:22:33:44:55 192.168.1.1
```

- **-T IP**: Use -T as target address when pinging MACs that won't respond to a broadcast ping but perhaps to a directed broadcast.

Example:
```bash
arping -T 192.168.1.1 00:11:22:33:44:55
```

- **-p**: Turn on promiscuous mode on the interface.

Example:
```bash
arping -p 192.168.1.1
```

- **-P**: Send ARP replies instead of requests. Useful with -U.

Example:
```bash
arping -P 192.168.1.1
```

- **-u**: Show index=received/sent instead of just index=received when pinging MACs.

Example:
```bash
arping -u 192.168.1.1
```

- **-U**: Send unsolicited ARP.

Example:
```bash
arping -U 192.168.1.1
```

- **-v**: Verbose output. Use twice for more messages.

Example:
```bash
arping -v 192.168.1.1
```

- **-V num**: 802.1Q tag to add. Defaults to no VLAN tag.

Example:
```bash
arping -V 100 192.168.1.1
```

- **-w sec**: Specify a timeout before ping exits regardless of how many packets have been sent or received.

Example:
```bash
arping -w 5 192.168.1.1
```

- **-W sec**: Time to wait between pings.

Example:
```bash
arping -W 1 192.168.1.1
```

- **-z**: Enable seccomp.

Example:
```bash
arping -z 192.168.1.1
```

- **-Z**: Disable seccomp (default).

Example:
```bash
arping -Z 192.168.1.1
```
#### combine multiple `arping` commands with different options to perform various tasks. Here are a few examples:

1. **Combining `-c` and `-W` Options**: Send a specified number of ARP requests to a host with a timeout between each request.

```bash
arping -c 5 -W 1 192.168.1.1
```

2. **Using `-i` and `-s` Options**: Send ARP requests using a specific network interface and set a custom source MAC address.

```bash
arping -i eth0 -s 00:11:22:33:44:55 192.168.1.1
```

3. **Using `-A` and `-q` Options**: Perform ARP scanning for hosts in a subnet and suppress output messages.

```bash
arping -A -q 192.168.1.0/24
```

4. **Combining `-r` and `-R` Options**: Display raw output with MAC/IP addresses and show "the other one" for each reply.

```bash
arping -r -R 192.168.1.1
```

5. **Using `-v` and `-VV` Options**: Display verbose output with more detailed messages.

```bash
arping -v -VV 192.168.1.1
```

6. **Combining `-p` and `-u` Options**: Enable promiscuous mode on the interface and show index=received/sent instead of just index=received when pinging MACs.

```bash
arping -p -u 192.168.1.1
```
