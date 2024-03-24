1. **Basic Scan**:
   - Perform a basic scan on a WordPress website. Replace `http://example.com` with the URL of the WordPress site:

    ```bash
    wpscan --url http://example.com
    ```

2. **Verbose Mode**:
   - Run the scan in verbose mode to display detailed information:

    ```bash
    wpscan --url http://example.com -v
    ```

3. **Output to File**:
   - Save the scan results to a file. Replace `output.txt` with the desired filename:

    ```bash
    wpscan --url http://example.com -o output.txt
    ```

4. **Enumeration Process**:
   - Enumerate vulnerable plugins and themes:

    ```bash
    wpscan --url http://example.com -e vp,vt
    ```

5. **Password Attack**:
   - Perform a password attack against WordPress login:

    ```bash
    wpscan --url http://example.com -U admin -P passwords.txt
    ```

6. **Custom User-Agent**:
   - Use a custom User-Agent for the scan:

    ```bash
    wpscan --url http://example.com --user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.182 Safari/537.36"
    ```

7. **Ignoring SSL/TLS Checks**:
   - Disable SSL/TLS certificate verification:

    ```bash
    wpscan --url https://example.com --disable-tls-checks
    ```

8. **Using Proxy**:
   - Use a proxy to connect to the target URL:

    ```bash
    wpscan --url http://example.com --proxy http://127.0.0.1:8080
    ```

9. **Updating Database**:
   - Update the WPScan database:

    ```bash
    wpscan --update
    ```

10. **Full Help Information**:
    - Display full help information:

    ```bash
    wpscan --hh
    ```
11. **Specifying Detection Mode**:
   - Set the detection mode for scanning. For example, set it to aggressive:

    ```bash
    wpscan --url http://example.com --detection-mode aggressive
    ```

12. **Setting Maximum Threads**:
   - Specify the maximum number of threads to use for scanning:

    ```bash
    wpscan --url http://example.com -t 10
    ```

13. **Setting Throttle Time**:
   - Set the throttle time in milliseconds before making another web request. This is useful for reducing the load on the target server:

    ```bash
    wpscan --url http://example.com --throttle 2000
    ```

14. **Setting Request Timeout**:
   - Specify the request timeout in seconds:

    ```bash
    wpscan --url http://example.com --request-timeout 90
    ```

15. **Setting Connect Timeout**:
   - Specify the connection timeout in seconds:

    ```bash
    wpscan --url http://example.com --connect-timeout 45
    ```

16. **Using API Token**:
   - Use the WPScan API Token to display vulnerability data. Replace `YOUR_API_TOKEN` with your actual API token:

    ```bash
    wpscan --url http://example.com --api-token YOUR_API_TOKEN
    ```

17. **Specifying wp-content Directory**:
   - Set the wp-content directory if custom or not detected:

    ```bash
    wpscan --url http://example.com --wp-content-dir custom-wp-content
    ```

18. **Specifying wp-plugins Directory**:
   - Set the plugins directory if custom or not detected:

    ```bash
    wpscan --url http://example.com --wp-plugins-dir custom-plugins
    ```

19. **Excluding Content-Based on Regex**:
   - Exclude all responses matching a regular expression during parts of the enumeration. For example, to exclude responses containing "admin":

    ```bash
    wpscan --url http://example.com --exclude-content-based admin
    ```

20. **Setting Multicall Maximum Passwords**:
    - Set the maximum number of passwords to send by request with XMLRPC multicall:

    ```bash
    wpscan --url http://example.com --multicall-max-passwords 1000
    ```
