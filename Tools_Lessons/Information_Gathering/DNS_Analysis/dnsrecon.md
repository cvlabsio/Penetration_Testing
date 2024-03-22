**dnsrecon** is a powerful DNS reconnaissance tool that aids security professionals in gathering detailed information about a target domain's DNS records. It offers a wide range of functionalities, including:

- **Standard Record Enumeration:** Enumerates common DNS records like A (address), MX (mail exchange), NS (nameserver), SOA (Start of Authority), AAAA (IPv6 address), SPF (Sender Policy Framework), and TXT (text) records.
- **Zone Transfer:** Attempts zone transfers to retrieve the entire DNS zone file (if permitted by the server configuration). **Be cautious** as zone transfers can be intrusive and might violate some DNS server policies.
- **Wildcard Resolution:** Checks if the target domain has wildcard DNS records that can resolve any subdomain.
- **SRV Record Enumeration:** Discovers Service Location records (SRV) used by specific services like SIP.
- **Top-Level Domain (TLD) Expansion:** Attempts to find subdomains using various TLDs (e.g., .com, .net, .org).
- **Brute-Force Subdomain Enumeration:** Uses a wordlist to brute-force potential subdomains of the target domain.
- **PTR Record Lookup:** Performs reverse DNS lookups to map IP addresses to hostnames (given an IP range or CIDR notation).
- **DNS Cache Snooping:** Queries nameservers for cached records of the target domain (experimental feature).

**Usage:**

```bash
dnsrecon [options] -d <target domain>
```

**Options:**

- `-a`: Performs standard record enumeration (default behavior).
- `-s`: Enables zone transfer attempt (use with caution).
- `-z`: Checks for wildcard resolution.
- `-D <file>`: Specifies a custom wordlist for brute-force subdomain enumeration.
- `-r <IP range/CIDR>`: Performs reverse DNS lookup for an IP range or CIDR.
- `-n <nameserver>`: Uses a custom nameserver for the DNS queries.
- `-c`: Saves results in CSV format.
- `-j`: Saves results in JSON format.
- `-x`: Saves results in XML format.
- `-d`: Saves results in a database (SQLite format by default).
- `-v`: Enables verbose output for more details.

**Examples:**

1. **Standard Record Enumeration:**

   ```bash
   dnsrecon -d example.com
   ```

   This enumerates common DNS records for `example.com`.

2. **Brute-Force Subdomain Enumeration (Using Default Wordlist):**

   ```bash
   dnsrecon -D -d example.com
   ```

   This attempts to brute-force subdomains of `example.com` using the built-in wordlist.

3. **Reverse DNS Lookup:**

   ```bash
   dnsrecon -r 192.168.1.0/24
   ```

   This performs reverse DNS lookups for all IP addresses in the subnet 192.168.1.0/24.

4. **Saving Results in JSON Format:**

   ```bash
   dnsrecon -j -d target.com > results.json
   ```

   This enumerates DNS records for `target.com` and saves the results in JSON format to the file `results.json`.

5. **Zone Transfer Attempt (Use with Caution):**

   ```bash
   dnsrecon -s -d vulnerabledomain.com
   ```

   This attempts a zone transfer for `vulnerabledomain.com`. **Remember, zone transfers can be intrusive.**
