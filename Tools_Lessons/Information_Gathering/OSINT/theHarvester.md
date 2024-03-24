1. **Enumerate Email Addresses**:
```
theharvester -d example.com -l 500 -b google
```
This command searches for email addresses associated with the domain `example.com` using Google as the data source (`-b google`) and limits the search to 500 results (`-l 500`).

2. **Enumerate Subdomains**:
```
theharvester -d example.com -b all
```
This command enumerates subdomains of the domain `example.com` using all available data sources (`-b all`), including search engines, DNS servers, and more.

3. **Enumerate Email Addresses and Save Results to a File**:
```
theharvester -d example.com -l 100 -b all -f results.txt
```
This command searches for email addresses associated with the domain `example.com` and saves the results to a file named `results.txt`. It limits the search to 100 results (`-l 100`) and uses all available data sources (`-b all`).

4. **Enumerate Email Addresses and Virtual Hosts with Detailed Output**:
```
theharvester -d example.com -l 200 -b all -v -f detailed_results.xml
```
This command searches for email addresses and virtual hosts associated with the domain `example.com`, limits the search to 200 results (`-l 200`), and saves the detailed results to an XML file named `detailed_results.xml`.

5. **Use Specific Data Sources**:
```
theharvester -d example.com -b bing,linkedin
```
This command searches for email addresses associated with the domain `example.com` using specific data sources (`-b bing,linkedin`), such as Bing and LinkedIn.

6. **Enumerate Email Addresses and Show Only Unique Results**:
```
theharvester -d example.com -l 100 -b all -e gmail.com
```
This command searches for email addresses associated with the domain `example.com`, limits the search to 100 results (`-l 100`), uses all available data sources (`-b all`), and shows only unique results with the domain `gmail.com` (`-e gmail.com`).

7. **Enumerate Email Addresses and Specify Output Format**:
```
theharvester -d example.com -l 200 -b all -f output.json
```
This command searches for email addresses associated with the domain `example.com`, limits the search to 200 results (`-l 200`), uses all available data sources (`-b all`), and saves the results in JSON format to a file named `output.json`.
