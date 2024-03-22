**Why use dnswalk?**

Dnswalk helps troubleshoot DNS issues. If you're having trouble resolving domain names or suspect inconsistencies in your DNS settings, dnswalk can pinpoint potential problems.

**Using dnswalk:**

Dnswalk is a command-line tool. Here's the basic usage:

```
dnswalk <domain_name>
```

Replace `<domain_name>` with the domain you want to check (e.g., dnswalk example.com).

**Common Options:**

* `-r`: Enables recursive mode. Dnswalk will also check subdomains of the specified domain.
* `-a`: Warns about duplicate A records (used for mapping domain names to IP addresses).
* `-d`: Prints debugging information during the process. 
* `-F`: Performs "fascist" checking, enforcing stricter consistency rules.
* `-i`: Ignores checks for invalid characters in the domain name. (Use with caution)
* `-l`: Checks for "lame delegation," where a nameserver doesn't have a valid record for a subdomain it's supposed to handle.

**Example Usage:**

1. **Basic Check:**

```
dnswalk example.com
```

This performs a basic check of the example.com zone.

2. **Recursive Check with Debugging:**

```
dnswalk -r -d google.com
```

This checks google.com and its subdomains while printing debugging information.

3. **Strict Checking for lame delegation:**

```
dnswalk -F -l mydomain.com
```

This performs a stricter check of mydomain.com, looking for consistency issues and potential lame delegation problems.
