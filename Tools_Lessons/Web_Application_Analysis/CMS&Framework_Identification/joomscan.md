1. **Basic Usage**:
   - To perform a basic scan on a Joomla website, you need to specify the URL using the `--url` or `-u` option:

    ```bash
    joomscan --url http://example.com
    ```

2. **Enumerating Components**:
   - You can instruct joomscan to enumerate components using the `--enumerate-components` or `-ec` option:

    ```bash
    joomscan --url http://example.com --enumerate-components
    ```

3. **Setting Cookies**:
   - If the website requires a specific cookie, you can set it using the `--cookie` option:

    ```bash
    joomscan --url http://example.com --cookie "name=value"
    ```

4. **Setting User-Agent**:
   - You can specify a custom User-Agent using the `--user-agent` or `-a` option:

    ```bash
    joomscan --url http://example.com --user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.182 Safari/537.36"
    ```

5. **Using Random User-Agent**:
   - If you want to use a random User-Agent for anonymity, you can use the `--random-agent` or `-r` option:

    ```bash
    joomscan --url http://example.com --random-agent
    ```

6. **Setting Timeout**:
   - You can specify a timeout for requests using the `--timeout` option:

    ```bash
    joomscan --url http://example.com --timeout 30
    ```

7. **Using Proxy**:
   - If you want to use a proxy to connect to the target URL, you can use the `--proxy` option:

    ```bash
    joomscan --url http://example.com --proxy http://127.0.0.1:8080
    ```

8. **About Author**:
   - If you want to know more about the author, you can use the `--about` option:

    ```bash
    joomscan --about
    ```

9. **Help**:
   - You can display the help screen using the `--help` or `-h` option:

    ```bash
    joomscan --help
    ```

10. **Version**:
    - To output the current version of joomscan, use the `--version` option:

    ```bash
    joomscan --version
    ```
    
11. **Scanning with Custom Headers**:
   - You can include custom headers in your requests using the `-H` option. For example, to include a custom header `X-My-Header: Value`:

    ```bash
    joomscan --url http://example.com -H "X-My-Header: Value"
    ```

12. **Enumerating Plugins**:
   - To enumerate plugins installed on the Joomla website, you can use the `--enumerate-plugins` or `-ep` option:

    ```bash
    joomscan --url http://example.com --enumerate-plugins
    ```

13. **Setting Request Timeout**:
   - You can specify the request timeout in seconds using the `--timeout` option. For example, to set the timeout to 60 seconds:

    ```bash
    joomscan --url http://example.com --timeout 60
    ```

14. **Using SOCKS Proxy**:
   - If you want to use a SOCKS proxy to connect to the target URL, you can specify it using the `--proxy` option with the `socks://` prefix:

    ```bash
    joomscan --url http://example.com --proxy socks://127.0.0.1:414
    ```

15. **Displaying Version Information Only**:
   - You can output only the version information of joomscan using the `--version` option:

    ```bash
    joomscan --version
    ```

16. **Scanning HTTPS Site with Custom Port**:
   - If the Joomla website is hosted on HTTPS and uses a custom port (e.g., 8443), you can specify the URL with the port using the `--url` option:

    ```bash
    joomscan --url https://example.com:8443
    ```

17. **Scanning Multiple URLs**:
   - You can scan multiple Joomla URLs by providing them in a file and using the `-L` option:

    ```bash
    joomscan -L urls.txt
    ```

    - The `urls.txt` file should contain one URL per line.

18. **Displaying Help Information Verbosely**:
   - You can display detailed help information using the `--help` option:

    ```bash
    joomscan --help
    ```
