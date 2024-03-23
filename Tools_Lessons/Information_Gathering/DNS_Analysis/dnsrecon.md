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
