### HTTP Options:
1. **Header (-H):** Specify custom HTTP headers.
   ```bash
   ffuf -w wordlist.txt -u https://example.com/FUZZ -H "Authorization: Bearer TOKEN"
   ```

2. **HTTP Method (-X):** Specify the HTTP method to use.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -X POST
   ```

3. **Cookie Data (-b):** Send custom cookie data with the request.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -b "session=SESSION_ID"
   ```

4. **POST Data (-d):** Send POST data with the request.
   ```bash
   ffuf -w wordlist.txt -u https://example.com/login -X POST -d "username=admin&password=FUZZ"
   ```

5. **Follow Redirects (-r):** Follow HTTP redirects.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -r
   ```

6. **Timeout (-timeout):** Set the HTTP request timeout in seconds.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -timeout 15
   ```

### General Options:
7. **Colorize Output (-c):** Colorize output for better readability.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -c
   ```

8. **Verbose Output (-v):** Print full URLs and redirect locations.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -v
   ```

9. **Maximum Running Time (-maxtime):** Set the maximum running time in seconds.
   ```bash
   ffuf -w wordlist.txt -u https://example.com -maxtime 3600
   ```

10. **Number of Threads (-t):** Set the number of concurrent threads.
    ```bash
    ffuf -w wordlist.txt -u https://example.com -t 50
    ```

### Matcher Options:
11. **Match HTTP Status Codes (-mc):** Match specific HTTP status codes.
    ```bash
    ffuf -w wordlist.txt -u https://example.com/FUZZ -mc 200,204,301
    ```

12. **Match Regexp (-mr):** Match responses based on regular expressions.
    ```bash
    ffuf -w wordlist.txt -u https://example.com/FUZZ -mr 'Error: \d+'
    ```

13. **Match HTTP Response Size (-ms):** Match responses based on their size.
    ```bash
    ffuf -w wordlist.txt -u https://example.com/FUZZ -ms '!=1024'
    ```

### Filter Options:
14. **Filter HTTP Status Codes (-fc):** Filter out specific HTTP status codes.
    ```bash
    ffuf -w wordlist.txt -u https://example.com/FUZZ -fc 403,404
    ```

15. **Filter by Response Size (-fs):** Filter responses based on their size.
    ```bash
    ffuf -w wordlist.txt -u https://example.com/FUZZ -fs '>=1024'
    ```

16. **Filter by Regexp (-fr):** Exclude responses matching a regular expression.
    ```bash
    ffuf -w wordlist.txt -u https://example.com/FUZZ -fr 'Access Denied'
    ```
