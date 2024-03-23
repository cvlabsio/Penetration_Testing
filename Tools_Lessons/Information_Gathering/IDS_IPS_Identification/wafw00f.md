### Basic Usage:
To use wafw00f, simply specify the URL of the target website as the argument. For example:

```bash
wafw00f http://example.com
```

This command will analyze the provided URL and attempt to detect any WAFs protecting it.

### Examples with Options:

#### 1. Verbose Output:
You can use the `-v` or `--verbose` option to get more detailed output:

```bash
wafw00f -v http://example.com
```

#### 2. Specify Custom Headers:
Sometimes, specifying custom headers can help wafw00f in its detection process. You can use the `-H` or `--headers` option for this:

```bash
wafw00f -H "User-Agent: Mozilla/5.0" http://example.com
```

#### 3. Ignore SSL Certificate Errors:
If you're testing a website with SSL and want to ignore SSL certificate errors, you can use the `--ssl` option:

```bash
wafw00f --ssl http://example.com
```

#### 4. Disable WAF Identification:
If you only want to see the HTTP headers without attempting to identify the WAF, you can use the `-n` or `--no-identify` option:

```bash
wafw00f -n http://example.com
```

#### 5. Disable SSL Certificate Verification:
In some cases, you might want to disable SSL certificate verification. You can do this using the `--no-ssl-verify` option:

```bash
wafw00f --no-ssl-verify http://example.com
```

#### 6. JSON Output Format:
To get the output in JSON format, which can be useful for scripting or parsing, you can use the `-j` or `--json` option:

```bash
wafw00f -j http://example.com
```
