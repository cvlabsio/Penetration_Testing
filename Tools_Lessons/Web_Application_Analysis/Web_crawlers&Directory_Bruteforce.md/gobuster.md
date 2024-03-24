1. Directory and file enumeration:
   ```bash
   gobuster dir -u http://example.com -w wordlist.txt
   ```

2. DNS subdomain enumeration:
   ```bash
   gobuster dns -d example.com -w subdomains.txt
   ```

3. Fuzzing mode:
   ```bash
   gobuster fuzz -u http://example.com/FUZZ -w wordlist.txt
   ```

4. Google Cloud Storage bucket enumeration:
   ```bash
   gobuster gcs -u gs://example-bucket -w wordlist.txt
   ```

5. AWS S3 bucket enumeration:
   ```bash
   gobuster s3 -u s3://example-bucket -w wordlist.txt
   ```

6. TFTP enumeration:
   ```bash
   gobuster tftp -u tftp://example.com -w wordlist.txt
   ```

7. VHOST enumeration:
   ```bash
   gobuster vhost -u http://example.com -w vhosts.txt
   ```

8. Using a custom wordlist with directory enumeration:
   ```bash
   gobuster dir -u http://example.com -w custom_wordlist.txt
   ```

9. Performing DNS subdomain enumeration with a higher number of threads:
   ```bash
   gobuster dns -d example.com -w subdomains.txt -t 20
   ```

10. Fuzzing mode with verbose output and a custom pattern file:
    ```bash
    gobuster fuzz -u http://example.com/FUZZ -w wordlist.txt -v -p patterns.txt
    ```

11. Enumerating Google Cloud Storage buckets with a specified delay between requests:
    ```bash
    gobuster gcs -u gs://example-bucket -w wordlist.txt --delay 100ms
    ```

12. AWS S3 bucket enumeration with quiet mode enabled and output to a file:
    ```bash
    gobuster s3 -u s3://example-bucket -w wordlist.txt -q -o results.txt
    ```

13. TFTP enumeration with debugging enabled:
    ```bash
    gobuster tftp -u tftp://example.com -w wordlist.txt --debug
    ```

14. VHOST enumeration with verbose output and ignoring errors:
    ```bash
    gobuster vhost -u http://example.com -w vhosts.txt -v --no-error
    ```

15. Directory enumeration with a specified wordlist offset to resume from a certain position:
    ```bash
    gobuster dir -u http://example.com -w wordlist.txt --wordlist-offset 500
    ```
