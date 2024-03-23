### hping3 Usage Guide:

#### 1. General Options:

- **-h, --help**: Show help.

Example:
```bash
hping3 --help
```

- **-v, --version**: Show version.

Example:
```bash
hping3 --version
```

- **-c, --count**: Packet count.

Example:
```bash
hping3 -c 5 example.com
```

- **-i, --interval**: Wait time between packets.

Example:
```bash
hping3 -i u1000 example.com
```

- **--fast**: Alias for `-i u10000` (10 packets per second).

Example:
```bash
hping3 --fast example.com
```

- **--faster**: Alias for `-i u1000` (100 packets per second).

Example:
```bash
hping3 --faster example.com
```

- **--flood**: Send packets as fast as possible. Don't show replies.

Example:
```bash
hping3 --flood example.com
```

- **-n, --numeric**: Numeric output.

Example:
```bash
hping3 -n example.com
```

- **-q, --quiet**: Quiet mode.

Example:
```bash
hping3 -q example.com
```

- **-I, --interface**: Interface name.

Example:
```bash
hping3 -I eth0 example.com
```

- **-V, --verbose**: Verbose mode.

Example:
```bash
hping3 -V example.com
```

- **-D, --debug**: Debugging info.

Example:
```bash
hping3 -D example.com
```

- **-z, --bind**: Bind ctrl+z to TTL.

Example:
```bash
hping3 -z example.com
```

- **-Z, --unbind**: Unbind ctrl+z.

Example:
```bash
hping3 -Z example.com
```

- **--beep**: Beep for every matching packet received.

Example:
```bash
hping3 --beep example.com
```

#### 2. Mode:

- **Default Mode**: TCP.

Example:
```bash
hping3 example.com
```

- **-0, --rawip**: RAW IP mode.

Example:
```bash
hping3 -0 192.168.1.1
```

- **-1, --icmp**: ICMP mode.

Example:
```bash
hping3 -1 example.com
```

- **-2, --udp**: UDP mode.

Example:
```bash
hping3 -2 example.com
```

- **-8, --scan**: SCAN mode.

Example:
```bash
hping3 -8 1-30,70-90 -S www.target.host
```

- **-9, --listen**: Listen mode.

Example:
```bash
hping3 -9 example.com
```

#### 3. IP:

- **-a, --spoof**: Spoof source address.

Example:
```bash
hping3 -a 192.168.1.2 example.com
```

- **--rand-dest**: Random destination address mode.

Example:
```bash
hping3 --rand-dest example.com
```

- **--rand-source**: Random source address mode.

Example:
```bash
hping3 --rand-source example.com
```

- **-t, --ttl**: TTL (default 64).

Example:
```bash
hping3 -t 64 example.com
```

- **-N, --id**: ID (default random).

Example:
```bash
hping3 -N 12345 example.com
```

- **-W, --winid**: Use win* id byte ordering.

Example:
```bash
hping3 -W example.com
```

- **-r, --rel**: Relativize ID field.

Example:
```bash
hping3 -r example.com
```

- **-f, --frag**: Split packets in more fragments.

Example:
```bash
hping3 -f example.com
```

- **-x, --morefrag**: Set more fragments flag.

Example:
```bash
hping3 -x example.com
```

- **-y, --dontfrag**: Set don't fragment flag.

Example:
```bash
hping3 -y example.com
```

- **-g, --fragoff**: Set the fragment offset.

Example:
```bash
hping3 -g 12345 example.com
```

- **-m, --mtu**: Set virtual MTU.

Example:
```bash
hping3 -m 1500 example.com
```

- **-o, --tos**: Type of service (default 0x00).

Example:
```bash
hping3 -o 0x0A example.com
```

- **-G, --rroute**: Includes RECORD_ROUTE option and display the route buffer.

Example:
```bash
hping3 -G example.com
```

- **--lsrr**: Loose source routing and record route.

Example:
```bash
hping3 --lsrr example.com
```

- **--ssrr**: Strict source routing and record route.

Example:
```bash
hping3 --ssrr example.com
```

- **-H, --ipproto**: Set the IP protocol field (only in RAW IP mode).

Example:
```bash
hping3 -H 6 example.com
```
#### You can combine multiple options and commands for `hping3`:

Example 1: Flood ICMP packets with a count of 1000 and verbose output.
```bash
hping3 --flood -1 -c 1000 -V example.com
```

Example 2: Spoof source address, flood UDP packets, and set TTL to 128.
```bash
hping3 -a 192.168.1.2 --flood -2 -t 128 example.com
```

Example 3: Scan ports 1-1000 on a target host using SYN mode with verbose output.
```bash
hping3 -8 1-1000 -S -V example.com
```

Example 4: Listen for incoming ICMP packets and display verbose output.
```bash
hping3 -9 -1 -V
```

Example 5: Send TCP packets with SYN and FIN flags set.
```bash
hping3 -S -F example.com
```
