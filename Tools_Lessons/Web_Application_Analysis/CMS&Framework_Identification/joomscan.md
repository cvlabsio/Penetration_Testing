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
