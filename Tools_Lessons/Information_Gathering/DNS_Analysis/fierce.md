**Usage**:
   - Basic usage: `fierce -dns example.com`
   - Specify DNS server: `fierce -dns example.com -dnsserver 8.8.8.8`
   - Output to a file: `fierce -dns example.com -file output.txt`

**Options**:
   - `-dns <domain>`: Specifies the target domain.
   - `-dnsserver <server>`: Allows specifying a custom DNS server.
   - `-file <filename>`: Specifies the output file.
   - `-threads <num>`: Sets the number of threads to use for DNS resolution.
   - `-traverse <num>`: Sets the number of iterations for subdomain discovery.
   - `-wordlist <filename>`: Specifies a custom wordlist for subdomain brute-forcing.
   - `-version`: Displays the tool's version.

**Examples**:
   - Enumerate DNS for example.com: `fierce -dns example.com`
   - Use a custom DNS server: `fierce -dns example.com -dnsserver 8.8.8.8`
   - Save output to a file: `fierce -dns example.com -file output.txt`
   - Increase threads for faster resolution: `fierce -dns example.com -threads 10`
   - Set the number of traversal iterations: `fierce -dns example.com -traverse 5`
   - Use a custom wordlist for subdomain discovery: `fierce -dns example.com -wordlist custom_wordlist.txt`
