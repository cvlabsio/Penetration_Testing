1. **Basic Usage**:
   ```
   dmitry [options] host
   ```

   This is the basic syntax of Dmitry. You specify the target host or domain after the options you want to use.

2. **Options**:

   - `-o`: Save output to a specified file.
   - `-i`: Perform a WHOIS lookup on the IP address of the host.
   - `-w`: Perform a WHOIS lookup on the domain name of the host.
   - `-n`: Retrieve Netcraft.com information on the host.
   - `-s`: Perform a search for possible subdomains.
   - `-e`: Perform a search for possible email addresses.
   - `-p`: Perform a TCP port scan on the host.
   - `-f`: Perform a TCP port scan on the host, showing output reporting filtered ports.
   - `-b`: Read in the banner received from the scanned port.
   - `-t 0-9`: Set the Time-to-Live (TTL) in seconds when scanning a TCP port (Default is 2).

   Note: Options marked with '*' require the `-p` flag to be passed.

3. **Examples**:

   - Perform a WHOIS lookup on a domain:
     ```
     dmitry -w example.com
     ```

   - Retrieve Netcraft.com information on a host:
     ```
     dmitry -n example.com
     ```

   - Search for possible subdomains:
     ```
     dmitry -s example.com
     ```

   - Search for possible email addresses:
     ```
     dmitry -e example.com
     ```

   - Perform a TCP port scan on a host:
     ```
     dmitry -p example.com
     ```

   - Perform a TCP port scan on a host, showing output reporting filtered ports:
     ```
     dmitry -pf example.com
     ```

   - Set the TTL to 5 seconds when scanning a TCP port:
     ```
     dmitry -p -t 5 example.com
     ```

4. **Saving Output**:
   You can save the output to a file using the `-o` option:
   ```
   dmitry -o output.txt example.com
   ```

   This will save the output to a file named `output.txt`.
   
#### More examples:

1. **Performing WHOIS Lookups**:
   - WHOIS lookup on an IP address:
     ```
     dmitry -i 192.0.2.1
     ```

2. **Retrieving Netcraft.com Information**:
   - Retrieve Netcraft.com information on a domain:
     ```
     dmitry -n example.com
     ```

3. **Searching for Subdomains**:
   - Search for possible subdomains of a domain:
     ```
     dmitry -s example.com
     ```

4. **Searching for Email Addresses**:
   - Search for possible email addresses associated with a domain:
     ```
     dmitry -e example.com
     ```

5. **Performing TCP Port Scans**:
   - TCP port scan on a host:
     ```
     dmitry -p example.com
     ```

   - TCP port scan on a host with output reporting filtered ports:
     ```
     dmitry -pf example.com
     ```

6. **Setting TTL for TCP Port Scans**:
   - Set the TTL to 5 seconds when scanning TCP ports:
     ```
     dmitry -p -t 5 example.com
     ```

7. **Saving Output to a File**:
   - Save output to a specific file:
     ```
     dmitry -o output.txt example.com
     ```

8. **Combining Multiple Options**:
   - Combine multiple options to gather comprehensive information:
     ```
     dmitry -iwnspe example.com
     ```

   This command performs WHOIS lookups, retrieves Netcraft.com information, searches for subdomains and email addresses, and performs a TCP port scan on the domain example.com, saving the output to default filenames.
