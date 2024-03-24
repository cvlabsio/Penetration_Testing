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
