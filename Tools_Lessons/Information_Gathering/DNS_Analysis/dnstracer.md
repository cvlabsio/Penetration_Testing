**Understanding the Options:**

Here's a breakdown of the options available with dnstracer:

- `-c`: Disables the local DNS cache on your machine, forcing dnstracer to query nameservers for fresh records. (Default: enabled)
- `-C`: Enables negative caching, where dnstracer remembers negative responses (e.g., "Domain not found") to avoid redundant requests for the same query. (Default: disabled)
- `-o`: Provides an overview of all received answers at the end of the trace, showing the complete chain and responses from each nameserver. (Default: disabled)
- `-q <querytype>`: Specifies the query type to use. Defaults to "A" for address records, but you can also use other types like "MX" (mail exchange), "CNAME" (canonical name), etc.
- `-r <retries>`: Sets the number of retries for failed DNS requests. Defaults to 3 attempts.
- `-s <server>`: Defines the initial nameserver to use for the query. Defaults to your local DNS server (often localhost). You can also use a specific IP address or ".'' (dot) to use a root nameserver (A.ROOT-SERVERS.NET).
- `-t <maximum timeout>`: Sets the maximum time to wait for a response from each nameserver in milliseconds.
- `-v`: Enables verbose output for more details about the tracing process.
- `-S <ip address>`: Allows you to specify the source IP address for your DNS queries.
- `-4`: Forces dnstracer to only query IPv4 nameservers, excluding IPv6 servers from the trace.

**Example Usage:**

1. **Standard Tracing (Default Options):**

   ```bash
   dnstracer google.com
   ```

   This will trace the path taken to resolve the A record for "google.com" using your local DNS cache settings and default query type (A).

2. **Tracing with Verbose Output:**

   ```bash
   dnstracer -v youtube.com
   ```

   This enables verbose output, providing more detailed information about each step of the tracing process for "youtube.com".

3. **Tracing with Negative Caching:**

   ```bash
   dnstracer -C non-existent-domain.com
   ```

   This attempts to resolve "non-existent-domain.com". With negative caching enabled, if the domain truly doesn't exist, dnstracer might avoid unnecessary queries to subsequent nameservers after receiving a negative response from the initial server.

4. **Tracing a Specific Query Type (MX Records):**

   ```bash
   dnstracer -q MX mail.yahoo.com
   ```

   This specifically traces the path for MX records associated with "mail.yahoo.com". 

5. **Tracing with Alternative Initial Nameserver:**

   ```bash
   dnstracer -s 8.8.8.8 google.com  # Using Google's Public DNS server (8.8.8.8)
   ```

   This initiates the trace for "google.com" using Google's public DNS server (8.8.8.8) as the starting point instead of your local server.

6. **Tracing with Maximum Timeout:**

   ```bash
   dnstracer -t 2000 stackoverflow.com  # Maximum wait time of 2 seconds per attempt
   ```

   This sets a maximum timeout of 2 seconds per retry for resolving "stackoverflow.com".

7. **Force IPv4 Server Query:**

   ```bash
   dnstracer -4 wikipedia.org  # Excludes IPv6 servers from the trace
   ```

   This ensures the trace only uses IPv4 nameservers to resolve "wikipedia.org", excluding any potential IPv6 servers from the path.
