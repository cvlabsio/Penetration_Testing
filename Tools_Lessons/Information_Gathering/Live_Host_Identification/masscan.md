### MASSCAN Usage Guide:

#### 1. Primary Input Parameters:

- **IP Addresses/Range**: Specify the IP addresses or ranges you want to scan.

Example:
```bash
masscan 10.0.0.0/8
```

- **Port Numbers**: Specify the port numbers you want to scan.

Example:
```bash
masscan 10.0.0.0/8 -p80
```

#### 2. Auto-Detection and Manual Network Interface Settings:

- **Auto-Detection**: The program auto-detects network interface/adapter settings.

- **Manual Configuration**: If auto-detection fails, you can set these parameters manually.

Example:
```bash
masscan --adapter-ip 192.168.10.123 --adapter-mac 00-11-22-33-44-55 --router-mac 66-55-44-33-22-11
```

#### 3. Setting Parameters via Command-Line or Config-File:

- **Command-Line**: Parameters can be set directly via the command-line.

- **Config-File**: Alternatively, you can specify parameters in a configuration file.

Example of setting parameters via command-line:
```bash
masscan -p80
```

Example of setting parameters via config-file:
```bash
masscan -c config_file.conf
```

#### 4. Equivalent Parameters:

- **Single-Dash Parameters**: All single-dash parameters have a spelled out double-dash equivalent.

Example:
```bash
masscan -p80
```
is equivalent to:
```bash
masscan --ports 80
```

#### 5. Generating Config-File:

- **Generating Config-File**: To generate a config-file from the current settings, use the `--echo` option.

Example:
```bash
masscan -p1234 --echo
```

Feel free to experiment with these options and examples to perform port scanning tasks efficiently with `masscan`! If you have any further questions or need additional assistance, feel free to ask!
