1. **Basic Directory Enumeration**:
```bash
wfuzz -c -z file,wordlist.txt --hc 404 http://example.com/FUZZ
```
This command fuzzes the FUZZ keyword in the URL with values from the wordlist file `wordlist.txt` and hides responses with status code 404.

2. **Brute-Forcing Parameters**:
```bash
wfuzz -c -z list,username.txt -z list,password.txt --basic auth -u http://example.com/login.php
```
This command bruteforces usernames and passwords using HTTP Basic Authentication against the login endpoint.

3. **Fuzzing Headers**:
```bash
wfuzz -c -z list,useragents.txt -H "User-Agent: FUZZ" -u http://example.com
```
This command fuzzes the User-Agent header with values from the `useragents.txt` file.

4. **Fuzzing POST Data**:
```bash
wfuzz -c -z file,postdata.txt -d "username=admin&password=FUZZ" -u http://example.com/login.php
```
This command fuzzes the password field in the POST data with values from the `postdata.txt` file.

5. **Recursive Path Discovery**:
```bash
wfuzz -c -z file,directory_list.txt -R 5 http://example.com/FUZZ
```
This command recursively discovers paths on the target website using a list of directories from `directory_list.txt` up to a depth of 5.

6. **Custom Header Fuzzing**:
```bash
wfuzz -c -z file,custom_headers.txt -H "X-Custom-Header: FUZZ" -u http://example.com
```
This command fuzzes a custom header named X-Custom-Header with values from the `custom_headers.txt` file.
