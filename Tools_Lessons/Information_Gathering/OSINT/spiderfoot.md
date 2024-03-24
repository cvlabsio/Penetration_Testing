1. Basic scan with default settings:
```
spiderfoot -s example.com
```
This command will perform a basic scan on the target domain `example.com`, using default settings for module selection and output format.

2. Enable specific modules for the scan:
```
spiderfoot -s example.com -m passive,totalhash
```
This command will perform a scan on the target domain `example.com` and enable only the `passive` and `totalhash` modules for data collection.

3. List available modules:
```
spiderfoot -M
```
This command will list all available modules that can be enabled for data collection.

4. List available event types:
```
spiderfoot -T
```
This command will list all available event types that can be collected by the enabled modules.

5. Specify output format:
```
spiderfoot -s example.com -o json
```
This command will perform a scan on the target domain `example.com` and output the results in JSON format.

6. Enable strict mode:
```
spiderfoot -s example.com -x
```
This command will perform a scan on the target domain `example.com` in strict mode, where only modules that can directly consume the target will be enabled.

7. Specify maximum number of threads:
```
spiderfoot -s example.com -max-threads 10
```
This command will perform a scan on the target domain `example.com` with a maximum of 10 threads running concurrently.
