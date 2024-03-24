### Usage:
```plaintext
CutyCapt --url=<url> --out=<path> [options]
```

### Options:
- `--help`: Print the help page and exit.
- `--url=<url>`: Specifies the URL to capture (supports `http://`, `https://`, `file://`, etc.).
- `--out=<path>`: Specifies the target file to save the screenshot.
- `--out-format=<f>`: Overrides the output format specified in `--out`.
- `--min-width=<int>`: Specifies the minimal width for the image (default: 800).
- `--min-height=<int>`: Specifies the minimal height for the image (default: 600).
- `--max-wait=<ms>`: Specifies the maximum wait time in milliseconds (default: 90000, inf: 0).
- `--delay=<ms>`: Specifies the delay in milliseconds after successful load (default: 0).
- `--user-style-path=<path>`: Specifies the location of the user style sheet file.
- `--user-style-string=<css>`: Specifies user style rules as text.
- `--header=<name>:<value>`: Specifies request headers (repeatable).
- `--method=<get|post|put>`: Specifies the request method (default: get).
- `--body-string=<string>`: Specifies the unencoded request body (default: none).
- `--body-base64=<base64>`: Specifies the Base64-encoded request body (default: none).
- `--app-name=<name>`: Specifies the appName used in User-Agent (default: none).
- `--app-version=<version>`: Specifies the appVers used in User-Agent (default: none).
- `--user-agent=<string>`: Overrides the User-Agent header set by Qt.
- `--javascript=<on|off>`: Specifies JavaScript execution (default: on).
- `--java=<on|off>`: Specifies Java execution (default: unknown).
- `--plugins=<on|off>`: Specifies plugin execution (default: unknown).
- `--private-browsing=<on|off>`: Specifies private browsing (default: unknown).
- `--auto-load-images=<on|off>`: Specifies automatic image loading (default: on).
- `--js-can-open-windows=<on|off>`: Specifies whether script can open windows (default: unknown).
- `--js-can-access-clipboard=<on|off>`: Specifies script clipboard privileges (default: unknown).
- `--print-backgrounds=<on|off>`: Specifies backgrounds in PDF/PS output (default: off).
- `--zoom-factor=<float>`: Specifies the page zoom factor (default: no zooming).
- `--zoom-text-only=<on|off>`: Specifies whether to zoom only the text (default: off).
- `--http-proxy=<url>`: Specifies the address for HTTP proxy server (default: none).
- `--smooth`: Attempt to enable Qt's high-quality settings.
- `--insecure`: Ignore SSL/TLS certificate errors.

### Examples:
1. **Basic Usage**:
   - Capture a screenshot of a web page and save it as `example.png`:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png
    ```

2. **Specifying Output Format**:
   - Capture a screenshot and save it as a PDF file:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.pdf --out-format=pdf
    ```

3. **Setting Minimal Width and Height**:
   - Specify the minimal width and height for the image:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --min-width=1024 --min-height=768
    ```

4. **Delay After Successful Load**:
   - Wait for 5 seconds after successful page load before capturing the screenshot:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --delay=5000
    ```

5. **Setting User Agent**:
   - Override the User-Agent header:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --user-agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.182 Safari/537.36"
    ```

6. **Ignoring SSL/TLS Certificate Errors**:
   - Capture a screenshot ignoring SSL/TLS certificate errors:

    ```bash
    CutyCapt --url=https://www.example.org/ --out=example.png --insecure
    ```
7. **Using User Style Sheet File**:
   - Capture a screenshot using a user style sheet file:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --user-style-path=/path/to/user_style.css
    ```

8. **Specifying Request Method**:
   - Specify the request method (e.g., POST) for capturing the screenshot:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --method=post
    ```

9. **Setting Request Headers**:
   - Set custom request headers (e.g., User-Agent, Referer):

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --header="User-Agent: Mozilla/5.0" --header="Referer: http://www.example.org"
    ```

10. **Setting Request Body**:
    - Set the request body for POST requests:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --method=post --body-string="param1=value1&param2=value2"
    ```

11. **Specifying Application Name and Version**:
    - Set the application name and version used in the User-Agent header:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --app-name="MyApp" --app-version="1.0"
    ```

12. **Disabling JavaScript Execution**:
    - Capture a screenshot with JavaScript execution disabled:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --javascript=off
    ```

13. **Enabling Java Execution**:
    - Capture a screenshot with Java execution enabled:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --java=on
    ```

14. **Enabling Plugin Execution**:
    - Capture a screenshot with plugin execution enabled:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --plugins=on
    ```

15. **Enabling Private Browsing**:
    - Capture a screenshot with private browsing enabled:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --private-browsing=on
    ```

16. **Disabling Automatic Image Loading**:
    - Capture a screenshot with automatic image loading disabled:

    ```bash
    CutyCapt --url=http://www.example.org/ --out=example.png --auto-load-images=off
    ```
