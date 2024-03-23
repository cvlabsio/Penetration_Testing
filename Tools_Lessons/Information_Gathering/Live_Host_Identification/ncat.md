### Ncat Usage Guide:

#### 1. Basic Connection:

- **Hostname**: Specify the hostname or IP address of the target host.
- **Port**: Specify the port number to connect to.

Example:
```bash
ncat example.com 80
```

#### 2. Options for Connection:

- **IPv4/IPv6/Unix domain sockets/vsock sockets**: Specify the address family to use.

Example:
```bash
ncat -4 example.com 80
```

- **CRLF for EOL sequence**: Use CRLF (Carriage Return Line Feed) for the end-of-line sequence.

Example:
```bash
ncat -C example.com 80
```

- **Execute Command**: Execute a command on the remote host.

Example:
```bash
ncat -e /bin/bash example.com 1234
```

- **Maximum Simultaneous Connections**: Set the maximum number of simultaneous connections.

Example:
```bash
ncat -m 10 example.com 80
```

- **Source Port/Address**: Specify the source port or address.

Example:
```bash
ncat -p 12345 -s 192.168.1.100 example.com 80
```

#### 3. Listening Mode:

- **Bind and Listen**: Start Ncat in listening mode.

Example:
```bash
ncat -l -p 1234
```

- **Keep Open**: Accept multiple connections in listen mode.

Example:
```bash
ncat -l -k -p 1234
```

#### 4. Protocol and Connection Options:

- **Use UDP/SCTP**: Use UDP or SCTP instead of the default TCP.

Example:
```bash
ncat -u example.com 1234
```

- **Telnet Negotiations**: Answer Telnet negotiations.

Example:
```bash
ncat -t example.com 23
```

- **Verbose Output**: Set verbosity level.

Example:
```bash
ncat -v -v -v example.com 80
```

#### 5. Miscellaneous Options:

- **Connect Timeout**: Set connection timeout.

Example:
```bash
ncat -w 10 example.com 80
```

- **Zero-I/O Mode**: Report connection status only.

Example:
```bash
ncat -z example.com 80
```

- **SSL**: Connect or listen with SSL.

Example:
```bash
ncat --ssl example.com 443
```

- **Version Information**: Display Ncat's version information.

Example:
```bash
ncat --version
```
