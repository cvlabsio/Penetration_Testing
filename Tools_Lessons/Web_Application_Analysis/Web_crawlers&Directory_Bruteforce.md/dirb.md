1. **Simple Test**:
   - Scan a directory on a web server:

    ```bash
    dirb http://url/directory/
    ```

2. **Testing Files with Specific Extension**:
   - Test files with the '.html' extension:

    ```bash
    dirb http://url/ -X .html
    ```

3. **Using Custom Wordlist**:
   - Test with the 'apache.txt' wordlist:

    ```bash
    dirb http://url/ /usr/share/dirb/wordlists/vulns/apache.txt
    ```

4. **Simple Test with SSL**:
   - Scan a secure URL using SSL:

    ```bash
    dirb https://secure_url/
    ```
5. **Specifying User-Agent**:
   - Specify a custom User-Agent string for the HTTP request:

    ```bash
    dirb http://url/ -a "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.182 Safari/537.36"
    ```

6. **Using Proxy**:
   - Use a proxy server for the scan:

    ```bash
    dirb http://url/ -p http://proxy_server:port
    ```

7. **Using HTTP Authentication**:
   - Perform the scan with HTTP authentication:

    ```bash
    dirb http://url/ -u username:password
    ```

8. **Ignoring Specific HTTP Responses**:
   - Ignore responses with a specific HTTP code (e.g., 403):

    ```bash
    dirb http://url/ -N 403
    ```

9. **Saving Output to a File**:
   - Save the output to a file:

    ```bash
    dirb http://url/ -o output.txt
    ```

10. **Fine-Tuning 404 Detection**:
    - Fine-tune the detection of NOT_FOUND (404) responses:

    ```bash
    dirb http://url/ -f
    ```

11. **Using Case-Insensitive Search**:
    - Perform a case-insensitive search:

    ```bash
    dirb http://url/ -i
    ```

12. **Printing Location Header**:
    - Print the "Location" header when found:

    ```bash
    dirb http://url/ -l
    ```

13. **Silent Mode**:
    - Run in silent mode, don't show tested words:

    ```bash
    dirb http://url/ -S
    ```

14. **Ignoring Redirects**:
    - Ignore redirects and don't follow them:

    ```bash
    dirb http://url/ -t
    ```
