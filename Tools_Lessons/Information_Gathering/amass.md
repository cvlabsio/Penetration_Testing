### Amass Intel Examples:

1. **Discover Subdomains for a Single Domain:**
```bash
amass intel -d example.com
```
This command initiates the Amass `intel` subcommand to gather intelligence about the domain `example.com` and discover its subdomains.

2. **Discover Subdomains for Multiple Domains:**
```bash
amass intel -d example.com,example.org,example.net
```
You can specify multiple domains separated by commas to gather intelligence about all of them.

3. **Specify a Custom Output File:**
```bash
amass intel -d example.com -o output.txt
```
This command saves the gathered intelligence to a custom output file named `output.txt`.

### Amass Enum Examples:

4. **Perform Enumerations for a Single Domain:**
```bash
amass enum -d example.com
```
This command initiates the Amass `enum` subcommand to perform enumerations and network mapping based on the gathered intelligence for the domain `example.com`.

5. **Perform Enumerations for Multiple Domains:**
```bash
amass enum -d example.com,example.org,example.net
```
Similar to the `intel` subcommand, you can specify multiple domains separated by commas to perform enumerations for all of them.

6. **Specify a Custom Output File:**
```bash
amass enum -d example.com -o output.txt
```
This command saves the results of the enumerations to a custom output file named `output.txt`.

7. **Use a Custom Configuration File:**
```bash
amass enum -d example.com -config config.yaml
```
Replace `config.yaml` with the path to your custom configuration file to specify advanced options and settings for Amass.

### General Examples:

8. **Show Version Information:**
```bash
amass -version
```
This command prints the version number of the Amass binary.

9. **Show Help Message:**
```bash
amass -h
```
This command displays the program usage message, providing a quick reference for available options.
