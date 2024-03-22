**dnsmap** is a subdomain enumeration tool that helps penetration testers and security researchers discover potential subdomains of a target domain. It works by brute-forcing subdomains using a built-in wordlist or a custom one you provide.

**Usage:**

```bash
dnsmap [options] <target domain>
```

**Options:**

- `-w <wordlist>`: Specify the path to a custom wordlist containing potential subdomains. (default: uses Kali's built-in wordlist)
- `-r <file>`: Save results to a file in human-readable format.
- `-c`: Save results to a file in CSV format (comma-separated values).
- `-d <delay>`: Introduce a delay (in seconds) between DNS lookups to avoid overwhelming the DNS server.
- `-v`: Enable verbose output for more details about the enumeration process.

**Examples:**

1. **Basic Subdomain Enumeration:**

   ```bash
   dnsmap example.com
   ```

   This enumerates subdomains of `example.com` using the default wordlist.

2. **Using a Custom Wordlist:**

   ```bash
   dnsmap -w my_subdomains.txt google.com
   ```

   This enumerates subdomains of `google.com` using the wordlist in the file `my_subdomains.txt`.

3. **Saving Results to a File:**

   ```bash
   dnsmap -r subdomains.txt target.com
   ```

   This enumerates subdomains of `target.com` and saves the results to the file `subdomains.txt`.

4. **Saving in CSV Format with Delay:**

   ```bash
   dnsmap -c -d 2 facebook.com > subdomains.csv
   ```

   This enumerates subdomains of `facebook.com`, saves the results in CSV format to the file `subdomains.csv`, and introduces a 2-second delay between DNS lookups.
