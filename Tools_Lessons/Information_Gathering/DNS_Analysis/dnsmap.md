**dnamap** is a network reconnaissance tool designed to help you efficiently gather information about network devices and their connections. It employs a combination of techniques, including:

- **ARP Scanning:** Discovers devices on a network by sending ARP (Address Resolution Protocol) requests.
- **ICMP Scanning (Ping Sweep):** Pings devices to determine their reachability.
- **TCP SYN Scanning:** Attempts to establish TCP connections with specific ports on devices to identify open services.
- **UDP Scanning:** Sends UDP packets to devices to check for open UDP ports.
- **DNS Resolution:** Resolves hostnames to IP addresses, providing more context to the discovered devices.

**Usage:**

```bash
dnamap [options] <target>
```

**Options:**

- `-i <interface>`: Specify the network interface to use (default: your system's default interface).
- `-p <port range>`: Comma-separated list of ports to scan (e.g., `-p 22,80,443`).
- `-t <scan type>`: Choose the scan type (ARP, ping, SYN, UDP, or all).
- `-sS`: Enables TCP SYN scan.
- `-sU`: Enables UDP scan.
- `-sn`: Suppresses name resolution (faster but less informative).
- `-r <file>`: Reads targets from a file (one per line).
- `-o <file>`: Saves output to a file (default: standard output).
- `-v`: Enables verbose output for more details.

**Examples:**

1. **Basic ARP Scan:**

   ```bash
   dnamap 192.168.1.0/24
   ```

   This scans all devices on the subnet 192.168.1.0/24 using ARP scanning.

2. **Ping Sweep and Port Scan (Default Ports):**

   ```bash
   dnamap -t ping,syn 10.0.0.1-10
   ```

   This performs a ping sweep and TCP SYN scan of devices with IP addresses from 10.0.0.1 to 10.0.0.10, targeting the default ports used by common services.

3. **Custom Port Scan with Verbose Output:**

   ```bash
   dnamap -t syn -p 22,80,443,139 172.16.0.50 -v
   ```

   This scans device 172.16.0.50 using a TCP SYN scan, focusing on ports 22 (SSH), 80 (HTTP), 443 (HTTPS), and 139 (Netware). Verbose output provides more detailed information about the scan process.

4. **Scan with Output to File:**

   ```bash
   dnamap -t all 192.168.1.200 > scan_results.txt
   ```

   This performs a comprehensive scan (ARP, ping, SYN, UDP) of device 192.168.1.200 and saves the results to the file "scan_results.txt".
