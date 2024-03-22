**Usage**:
   - Basic usage: `fierce --domain example.com`
   - Specify DNS server: `fierce --domain example.com -dnsserver 8.8.8.8`
   - Output to a file: `fierce --domain example.com -file output.txt`

**Options**:
   - `--domain <domain>`: Specifies the target domain.
   - `-dnsserver <server>`: Allows specifying a custom DNS server.
   - `-file <filename>`: Specifies the output file.
   - `-threads <num>`: Sets the number of threads to use for DNS resolution.
   - `-traverse <num>`: Sets the number of iterations for subdomain discovery.
   - `-wordlist <filename>`: Specifies a custom wordlist for subdomain brute-forcing.
   - `-version`: Displays the tool's version.

**Examples**:
   - Enumerate DNS for example.com: `fierce --domain example.com`
   - Use a custom DNS server: `fierce --domain example.com -dnsserver 8.8.8.8`
   - Save output to a file: `fierce --domain example.com -file output.txt`
   - Increase threads for faster resolution: `fierce --domain example.com -threads 10`
   - Set the number of traversal iterations: `fierce --domain example.com -traverse 5`
   - Use a custom wordlist for subdomain discovery: `fierce --domain example.com -wordlist custom_wordlist.txt`
