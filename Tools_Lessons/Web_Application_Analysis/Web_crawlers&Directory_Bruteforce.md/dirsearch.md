
1. Recursive scan with custom wordlists:
```bash
python3 dirsearch.py -u http://example.com -w wordlist1.txt,wordlist2.txt --recursive
```

2. Scan with specific extensions and follow redirects:
```bash
python3 dirsearch.py -u http://example.com -e php,html -F
```

3. Scan with custom headers and maximum recursion depth:
```bash
python3 dirsearch.py -u http://example.com -H "Authorization: Bearer token123" -R 5
```

4. Scan with proxy and authentication:
```bash
python3 dirsearch.py -u http://example.com -t 5 --proxy http://proxy.example.com:8080 --proxy-auth username:password
```

5. Scan with specified response status codes:
```bash
python3 dirsearch.py -u http://example.com -i 200,301,302,403
```

6. Scan with specified exclusion criteria:
```bash
python3 dirsearch.py -u http://example.com --exclude-status 404 --exclude-text "Not Found"
```

7. Scan with custom output format and log file:
```bash
python3 dirsearch.py -u http://example.com -o result.txt --format json --log scan.log
```

8. Scan multiple URLs from a file:
```bash
python3 dirsearch.py -l urls.txt --threads 10
```

9. Scan with custom wordlists and extensions, excluding specific subdirectories:
```bash
python3 dirsearch.py -u http://example.com -w custom_wordlist.txt -e php,html --exclude-subdirs admin,images
```

10. Recursive scan with specified response sizes and maximum runtime:
```bash
python3 dirsearch.py -u http://example.com --recursive --min-response-size 1KB --max-response-size 1MB --max-time 3600
```

11. Scan with custom request headers and delays between requests:
```bash
python3 dirsearch.py -u http://example.com -H "X-Custom-Header: Value" -H "Authorization: Bearer token" --delay 500
```

12. Scan with proxy and Tor network:
```bash
python3 dirsearch.py -u http://example.com --proxy http://proxy.example.com:8080 --tor
```

13. Scan with authentication using basic authentication:
```bash
python3 dirsearch.py -u http://example.com --auth username:password --auth-type basic
```

14. Scan using a raw HTTP request stored in a file:
```bash
python3 dirsearch.py --raw raw_request.txt
```

15. Scan with custom prefixes and suffixes added to all wordlist entries:
```bash
python3 dirsearch.py -u http://example.com --prefixes /admin,/test --suffixes .bak,.old
```

16. Scan with specified crawl depth and follow redirects history:
```bash
python3 dirsearch.py -u http://example.com --deep-recursive --recursion-status 200-399 --redirects-history
```

17. Scan with quiet mode and full URLs in the output:
```bash
python3 dirsearch.py -u http://example.com -q --full-url
```
