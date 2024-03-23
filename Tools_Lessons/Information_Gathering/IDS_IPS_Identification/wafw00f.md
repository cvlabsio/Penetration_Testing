### wafw00f Usage Guide:

#### 1. Basic Usage:
To use wafw00f, simply provide the URL(s) of the target website(s) as arguments. For example:

```bash
wafw00f http://www.example.com
```

#### 2. Options:

- **-h, --help**: Displays the help message with usage instructions and exits.
  
- **-v, --verbose**: Enables verbosity, providing more detailed output. You can use multiple `-v` options to increase verbosity levels.

Example:
```bash
wafw00f -v http://www.example.com
```

- **-a, --findall**: Finds all WAFs that match the signatures, rather than stopping testing after detecting the first one.

Example:
```bash
wafw00f -a http://www.example.com
```

- **-r, --noredirect**: Prevents following redirections given by 3xx responses.

Example:
```bash
wafw00f -r http://www.example.com
```

- **-t TEST, --test=TEST**: Tests for one specific WAF. You can specify the WAF to test against.

Example:
```bash
wafw00f -t Cloudflare http://www.example.com
```

- **-o OUTPUT, --output=OUTPUT**: Writes output to a CSV, JSON, or text file, depending on the file extension. Use `-` as the filename for stdout.

Example:
```bash
wafw00f -o output.json http://www.example.com
```

- **-f FORMAT, --format=FORMAT**: Forces the output format to CSV, JSON, or text.

Example:
```bash
wafw00f -f csv http://www.example.com
```

- **-i INPUT, --input-file=INPUT**: Reads targets from a file. The input format can be CSV, JSON, or text. For CSV and JSON, a `url` column name or element is required.

Example:
```bash
wafw00f -i targets.txt
```

- **-l, --list**: Lists all WAFs that wafw00f is able to detect.

Example:
```bash
wafw00f -l
```

- **-p PROXY, --proxy=PROXY**: Uses an HTTP proxy to perform requests.

Example:
```bash
wafw00f -p http://localhost:8080 http://www.example.com
```

- **-V, --version**: Prints out the current version of wafw00f and exits.

Example:
```bash
wafw00f -V
```

- **-H HEADERS, --headers=HEADERS**: Passes custom headers via a text file to overwrite the default header set.

Example:
```bash
wafw00f -H custom_headers.txt http://www.example.com
```
