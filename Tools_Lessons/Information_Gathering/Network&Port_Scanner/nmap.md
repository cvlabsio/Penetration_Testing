 **Basic Usage**:
   - The basic syntax for using Nmap is:
     ```
     nmap [Scan Type(s)] [Options] {target specification}
     ```
   - For example, to perform a basic TCP SYN scan:
     ```
     nmap -sS <target>
     ```

**Scan Types**:
   - Nmap supports various scan types, each with its own advantages and limitations. Common scan types include:
     - TCP SYN scan (`-sS`): Stealthy scan that does not complete TCP connections.
     - TCP Connect scan (`-sT`): Completes TCP connections to target ports.
     - UDP scan (`-sU`): Scans for open UDP ports.
     - Comprehensive scan (`-sC`): Enables default scripts for service enumeration, version detection, etc.
     - Ping scan (`-sP`): Determines online hosts without scanning ports.

**Output Formats**:
   - Nmap offers different output formats to suit your needs. Common formats include:
     - Normal output: Human-readable output displayed in the terminal.
     - XML output (`-oX`): Machine-readable output suitable for parsing by scripts and tools.
     - Grepable output (`-oG`): Output that can be easily parsed with grep and other Unix tools.

**Service and Version Detection**:
   - Nmap can detect the services running on open ports and attempt to determine their versions.
   - Enable service detection with `-sV` and version detection with `-sV`.

**Operating System Detection**:
   - Nmap can attempt to determine the operating system of the target hosts based on various characteristics.
   - Enable OS detection with `-O`.

**Timing and Performance**:
   - Nmap allows you to control the timing and performance of scans using options such as `-T<0-5>` for timing templates and `-p-` to scan all 65,535 ports.
   - Be cautious with aggressive timing settings, as they may increase the chance of detection or disrupt network services.

**Scripting Engine**:
   - Nmap includes a scripting engine (NSE) that allows users to write and run scripts for advanced tasks such as vulnerability scanning, exploitation, and network manipulation.
   - Run NSE scripts using the `--script` option, e.g., `--script vuln`.

**Firewall Evasion**:
   - Nmap offers techniques for evading firewalls and intrusion detection systems (IDS) to improve scan accuracy.
   - Techniques include fragmentation (`-f`), decoy scans (`-D`), and idle scan (`-sI`).
#### Examples:

1. **Scan a Single Host with TCP SYN Scan**:
   ```
   nmap -sS <target_ip>
   ```

2. **Scan Multiple Hosts in a Subnet**:
   ```
   nmap -sS <subnet>
   ```

3. **Scan Specific Ports**:
   ```
   nmap -p <port(s)> <target_ip>
   ```

4. **Scan All Ports**:
   ```
   nmap -p- <target_ip>
   ```

5. **Perform Version Detection**:
   ```
   nmap -sV <target_ip>
   ```

6. **Perform Operating System Detection**:
   ```
   nmap -O <target_ip>
   ```

7. **Scan with Aggressive Timing**:
   ```
   nmap -T4 <target_ip>
   ```

8. **Scan with Very Aggressive Timing**:
   ```
   nmap -T5 <target_ip>
   ```

9. **Scan Using a Specific Network Interface**:
   ```
   nmap -e <interface> <target_ip>
   ```

10. **Output Results to XML Format**:
    ```
    nmap -oX scan_results.xml <target_ip>
    ```

11. **Output Results to Grepable Format**:
    ```
    nmap -oG scan_results.gnmap <target_ip>
    ```

12. **Scan for UDP Ports**:
    ```
    nmap -sU <target_ip>
    ```

13. **Perform a Comprehensive Scan**:
    ```
    nmap -sC <target_ip>
    ```

14. **Scan for Vulnerabilities using NSE Scripts**:
    ```
    nmap --script vuln <target_ip>
    ```

15. **Scan with Decoy IP Addresses**:
    ```
    nmap -D RND:10 <target_ip>
    ```

16. **Perform a Ping Sweep**:
    ```
    nmap -sn <target_subnet>
    ```

17. **Scan Using Randomized Target Order**:
    ```
    nmap --randomize-hosts <target_ip>
    ```

18. **Scan Using IPv6**:
    ```
    nmap -6 <target_ipv6>
    ```

19. **Scan a Range of Hosts and Ports**:
    ```
    nmap -p 1-1000 192.168.1.1-10
    ```

20. **Scan for Common Web Ports**:
    ```
    nmap -p 80,443,8080 <target_ip>
    ```
#### More examples: 

1. **Scan for Common Vulnerabilities**:
   ```
   nmap --script vuln <target_ip>
   ```

2. **Scan for SMB Vulnerabilities**:
   ```
   nmap --script smb-vuln* <target_ip>
   ```

3. **Scan for HTTP Vulnerabilities**:
   ```
   nmap --script http-vuln* <target_ip>
   ```

4. **Scan for SSH Vulnerabilities**:
   ```
   nmap --script ssh* <target_ip>
   ```

5. **Scan for SSL/TLS Vulnerabilities**:
   ```
   nmap --script ssl* <target_ip>
   ```

6. **Scan for DNS Vulnerabilities**:
   ```
   nmap --script dns* <target_ip>
   ```

7. **Scan for FTP Vulnerabilities**:
   ```
   nmap --script ftp* <target_ip>
   ```

8. **Scan for SNMP Vulnerabilities**:
   ```
   nmap --script snmp* <target_ip>
   ```

9. **Scan for SMB Enumeration**:
   ```
   nmap --script smb-enum* <target_ip>
   ```

10. **Scan for HTTP Enumeration**:
    ```
    nmap --script http-enum* <target_ip>
    ```

11. **Scan for SNMP Enumeration**:
    ```
    nmap --script snmp-enum* <target_ip>
    ```

12. **Scan for SMB Authentication Bypass**:
    ```
    nmap --script smb-brute <target_ip>
    ```

13. **Scan for FTP Authentication Bypass**:
    ```
    nmap --script ftp-brute <target_ip>
    ```

14. **Scan for SSH Authentication Bypass**:
    ```
    nmap --script ssh-brute <target_ip>
    ```

15. **Scan for Telnet Authentication Bypass**:
    ```
    nmap --script telnet-brute <target_ip>
    ```

16. **Scan for Vulnerable Web Applications**:
    ```
    nmap --script http-vuln-cve2014-3704 <target_ip>
    ```

17. **Scan for Backdoors**:
    ```
    nmap --script backdoor <target_ip>
    ```

18. **Scan for Default Credentials**:
    ```
    nmap --script default* <target_ip>
    ```

19. **Scan for Known Vulnerable Software Versions**:
    ```
    nmap --script known* <target_ip>
    ```

20. **Scan for Heartbleed Vulnerability**:
    ```
    nmap --script ssl-heartbleed <target_ip>
    ```
#### More examples:

1. **Scan for SMB Shares**:
   ```
   nmap --script smb-enum-shares <target_ip>
   ```

2. **Scan for SNMP Information**:
   ```
   nmap --script snmp-info <target_ip>
   ```

3. **Scan for Web Servers and Their Technologies**:
   ```
   nmap --script http-headers <target_ip>
   ```

4. **Scan for Web Servers Vulnerabilities**:
   ```
   nmap --script http-vuln* <target_ip>
   ```

5. **Scan for FTP Servers and Their Banner**:
   ```
   nmap --script ftp-bounce <target_ip>
   ```

6. **Scan for DNS Zone Transfer**:
   ```
   nmap --script dns-zone-transfer <target_ip>
   ```

7. **Scan for Oracle Database Vulnerabilities**:
   ```
   nmap --script oracle-brute <target_ip>
   ```

8. **Scan for MySQL Database Vulnerabilities**:
   ```
   nmap --script mysql-vuln* <target_ip>
   ```

9. **Scan for MS-SQL Database Vulnerabilities**:
   ```
   nmap --script ms-sql-brute <target_ip>
   ```

10. **Scan for PostgreSQL Database Vulnerabilities**:
    ```
    nmap --script pgsql-brute <target_ip>
    ```

11. **Scan for VNC Servers and Authentication Bypass**:
    ```
    nmap --script vnc-brute <target_ip>
    ```

12. **Scan for SIP Servers**:
    ```
    nmap --script sip-enum-users <target_ip>
    ```

13. **Scan for Redis Servers**:
    ```
    nmap --script redis-info <target_ip>
    ```

14. **Scan for RDP Servers and Brute-Force Authentication**:
    ```
    nmap --script rdp-brute <target_ip>
    ```

15. **Scan for SMTP Servers and Enumerate Users**:
    ```
    nmap --script smtp-enum-users <target_ip>
    ```

16. **Scan for DNSSEC Vulnerabilities**:
    ```
    nmap --script dnssec-* <target_ip>
    ```

17. **Scan for Windows Registry Information**:
    ```
    nmap --script smb-registry* <target_ip>
    ```

18. **Scan for IPMI Service Information**:
    ```
    nmap --script ipmi-brute <target_ip>
    ```

19. **Scan for NFS Shares**:
    ```
    nmap --script nfs* <target_ip>
    ```

20. **Scan for IP Cameras and Their Vulnerabilities**:
    ```
    nmap --script ip-cam* <target_ip>
    ```
21. **Scan for SNMP Community Strings**:
    ```
    nmap --script snmp-brute <target_ip>
    ```

22. **Scan for SIP VoIP Devices**:
    ```
    nmap --script sip-enum-users, sip-methods <target_ip>
    ```

23. **Scan for IPMI Cipher 0 Vulnerability**:
    ```
    nmap --script ipmi-cipher-zero <target_ip>
    ```

24. **Scan for SMB2/SMB3 Vulnerabilities**:
    ```
    nmap --script smb2-capabilities, smb2-security-mode <target_ip>
    ```

25. **Scan for IP Forwarding and Spoofing**:
    ```
    nmap --script ip-spoofing, ip-forwarding <target_ip>
    ```

26. **Scan for Cisco Smart Install Vulnerability**:
    ```
    nmap --script cisco-smart-install <target_ip>
    ```

27. **Scan for Telnet Credentials**:
    ```
    nmap --script telnet-brute <target_ip>
    ```

28. **Scan for RealVNC Authentication Bypass**:
    ```
    nmap --script realvnc-auth-bypass <target_ip>
    ```

29. **Scan for MongoDB Databases**:
    ```
    nmap --script mongodb-databases <target_ip>
    ```

30. **Scan for Web Servers Vulnerable to Shellshock**:
    ```
    nmap --script http-shellshock <target_ip>
    ```

31. **Scan for Modbus Devices**:
    ```
    nmap --script modbus-discover <target_ip>
    ```

32. **Scan for SMB Signing Disabled**:
    ```
    nmap --script smb-security-mode <target_ip>
    ```

33. **Scan for Default SNMP Community Strings**:
    ```
    nmap --script snmp-brute, snmp-default-community <target_ip>
    ```

34. **Scan for Apache Struts Vulnerabilities**:
    ```
    nmap --script struts* <target_ip>
    ```

35. **Scan for UPnP Devices**:
    ```
    nmap --script upnp-info, upnp-discover <target_ip>
    ```

36. **Scan for SCADA Systems**:
    ```
    nmap --script scada* <target_ip>
    ```

37. **Scan for SSL Certificate Information**:
    ```
    nmap --script ssl-cert <target_ip>
    ```

38. **Scan for Heartbleed Vulnerability on Specific Port**:
    ```
    nmap --script ssl-heartbleed -p 443 <target_ip>
    ```

39. **Scan for SNMPv3 Credentials**:
    ```
    nmap --script snmp-enum, snmp-brute <target_ip>
    ```

40. **Scan for NTP Server Information**:
    ```
    nmap --script ntp-info <target_ip>
    ```

41. **Scan for Oracle Database Vulnerabilities**:
    ```
    nmap --script oracle* <target_ip>
    ```

42. **Scan for WordPress Vulnerabilities**:
    ```
    nmap --script http-wordpress* <target_ip>
    ```

43. **Scan for Joomla Vulnerabilities**:
    ```
    nmap --script http-joomla* <target_ip>
    ```

44. **Scan for Drupal Vulnerabilities**:
    ```
    nmap --script http-drupal* <target_ip>
    ```

45. **Scan for DNS Amplification**:
    ```
    nmap --script dns-recursion <target_ip>
    ```

46. **Scan for Heartbleed Vulnerability on SMTP Server**:
    ```
    nmap --script ssl-heartbleed -p 25 <target_ip>
    ```

47. **Scan for Heartbleed Vulnerability on FTP Server**:
    ```
    nmap --script ssl-heartbleed -p 21 <target_ip>
    ```

48. **Scan for Heartbleed Vulnerability on IMAP Server**:
    ```
    nmap --script ssl-heartbleed -p 143 <target_ip>
    ```

49. **Scan for Heartbleed Vulnerability on POP3 Server**:
    ```
    nmap --script ssl-heartbleed -p 110 <target_ip>
    ```

50. **Scan for Heartbleed Vulnerability on LDAP Server**:
    ```
    nmap --script ssl-heartbleed -p 389 <target_ip>
    ```

51. **Scan for SMB Shares and Enumerate Users**:
    ```
    nmap --script smb-enum* <target_ip>
    ```

52. **Scan for SNMP Services and Gather Information**:
    ```
    nmap --script snmp* <target_ip>
    ```

53. **Scan for IRC Servers and Channels**:
    ```
    nmap --script irc* <target_ip>
    ```

54. **Scan for IP Forwarding and Spoofing Detection**:
    ```
    nmap --script ip-spoofing <target_ip>
    ```

55. **Scan for Exploitable Routers**:
    ```
    nmap --script http-default-accounts, http-webcam <target_ip>
    ```

56. **Scan for NTP Server Amplification**:
    ```
    nmap --script ntp-monlist <target_ip>
    ```

57. **Scan for SNMP Community String Bruteforcing**:
    ```
    nmap --script snmp-brute <target_ip>
    ```

58. **Scan for FTP Anonymous Access**:
    ```
    nmap --script ftp-anon <target_ip>
    ```

59. **Scan for SMTP Open Relays**:
    ```
    nmap --script smtp-open-relay <target_ip>
    ```

60. **Scan for Common Windows Ports**:
    ```
    nmap --script smb-protocols, smb-os-discovery, smb-security-mode <target_ip>
    ```

61. **Scan for SNMP Weak Community Strings**:
    ```
    nmap --script snmp-brute,snmp-default-community,snmp-sysdescr <target_ip>
    ```

62. **Scan for MySQL Database Information**:
    ```
    nmap --script mysql-info,mysql-enum <target_ip>
    ```

63. **Scan for DNS Cache Snooping**:
    ```
    nmap --script dns-cache-snoop <target_ip>
    ```

64. **Scan for IPv6 Router Advertisement**:
    ```
    nmap --script ipv6-ra-flood <target_ip>
    ```

65. **Scan for Known Vulnerabilities in Network Protocols**:
    ```
    nmap --script broadcast,unusual-port <target_ip>
    ```

66. **Scan for OpenVPN Information**:
    ```
    nmap --script openvpn-auth-brute <target_ip>
    ```

67. **Scan for RDP Security Settings**:
    ```
    nmap --script rdp-enum-encryption,rdp-enum-fips <target_ip>
    ```

68. **Scan for IPMI Information**:
    ```
    nmap --script ipmi-version,ipmi-brute <target_ip>
    ```

69. **Scan for SMB Signing Status**:
    ```
    nmap --script smb-security-mode <target_ip>
    ```

70. **Scan for SNMP System Information**:
    ```
    nmap --script snmp-system <target_ip>
    ```

71. **Scan for SSL Ciphers Supported by a Server**:
    ```
    nmap --script ssl-enum-ciphers <target_ip>
    ```

72. **Scan for SSL Renegotiation Vulnerability**:
    ```
    nmap --script ssl-renegotiation <target_ip>
    ```

73. **Scan for SSL Weak Certificates**:
    ```
    nmap --script ssl-cert <target_ip>
    ```

74. **Scan for SSL Heartbleed Vulnerability**:
    ```
    nmap --script ssl-heartbleed <target_ip>
    ```

75. **Scan for SSL POODLE Vulnerability**:
    ```
    nmap --script ssl-poodle <target_ip>
    ```

76. **Scan for Web Application Vulnerabilities**:
    ```
    nmap --script http-vuln-* <target_ip>
    ```

77. **Scan for HTTP Proxy Servers**:
    ```
    nmap --script http-proxy-brute <target_ip>
    ```

78. **Scan for SNMP Community String Bruteforce**:
    ```
    nmap --script snmp-brute <target_ip>
    ```

79. **Scan for SMTP Open Relay**:
    ```
    nmap --script smtp-open-relay <target_ip>
    ```

80. **Scan for DNS Records**:
    ```
    nmap --script dns-nsec-enum <target_ip>
    ```

## Firewall:


1. **Firewall Evasion**:
   - Nmap offers several options to evade firewalls and improve scan accuracy:
     - Fragmentation (`-f`): Fragment packets to bypass packet filtering.
     - Decoy scans (`-D`): Send packets from spoofed IP addresses to confuse firewalls.
     - Timing options (`-T`): Adjust timing to avoid triggering firewall rate limits.
   - Example:
     ```
     nmap -f -T4 <target_ip>
     ```

2. **IDS/IPS Evasion**:
   - Nmap provides options to evade detection by IDS/IPS systems:
     - Randomize TCP sequence numbers (`--rand-ports`): Randomize TCP sequence numbers to bypass signature-based detection.
     - Timing options (`-T`): Adjust timing to avoid detection by behavior-based systems.
   - Example:
     ```
     nmap --rand-ports -T3 <target_ip>
     ```

3. **Load Balancer Detection**:
   - Nmap can help detect load balancers by analyzing responses from different hosts behind the balancer:
     - Service detection (`-sV`): Analyze responses to identify patterns that indicate load balancing.
     - Scripting Engine (`--script`): Use scripts like `http-title` to analyze HTTP responses for load balancer signatures.
   - Example:
     ```
     nmap -sV --script http-title <target_ip>
     ```

4. **Fragmented Packets Scan**:
   - Fragmented packets can sometimes bypass packet filtering rules in firewalls and IDS/IPS systems:
     - Fragmentation (`-f`): Split packets into smaller fragments to evade detection.
     - Maximum Transmission Unit (MTU) options (`--mtu`): Adjust packet size to fragment them appropriately.
   - Example:
     ```
     nmap -f --mtu 8 <target_ip>
     ```

5. **Decoy Scan**:
   - Decoy scan involves sending packets with spoofed source IP addresses to make it harder for firewalls and IDS/IPS systems to detect the real source:
     - Decoy options (`-D`): Specify decoy addresses to confuse the target and intermediaries.
   - Example:
     ```
     nmap -T3 -D RND:10 <target_ip>
     ```

6. **Idle Scan**:
   - Idle scan (also known as zombie scan) can help bypass firewall and IDS/IPS detection by using a third-party host as a proxy:
     - Idle scan (`-sI`): Use a zombie host to perform the scan, making it harder to trace back to the actual source.
   - Example:
     ```
     nmap -sI zombie_host <target_ip>
     ```

7. **Idle Zombie Scan**:
   - This technique uses a third-party host as a 'zombie' to perform scans, making it harder to trace back to the actual source.
   - Example:
     ```
     nmap -sI zombie_host <target_ip>
     ```

8. **FTP Bounce Scan**:
   - This technique leverages the FTP bounce attack to perform port scanning through an FTP server.
   - Example:
     ```
     nmap -b ftp_server_ip <target_ip>
     ```

9. **Custom TCP Initial Sequence Number (ISN)**:
   - This option allows you to set a custom TCP initial sequence number, which can help in evading IDS/IPS.
   - Example:
     ```
     nmap --data-length 24 --source-port 53 <target_ip>
     ```

10. **Spoof MAC Address**:
    - Spoofing MAC addresses can help in bypassing MAC-based access controls.
    - Example:
      ```
      nmap --spoof-mac random <target_ip>
      ```

11. **Use Different Scan Techniques**:
    - Sometimes using different scan techniques in combination can help in evading detection.
    - Example:
      ```
      nmap -sS -sU -sT -p 1-65535 <target_ip>
      ```

12. **Use Proxy Chains**:
    - If you're scanning from behind a proxy, you can use proxy chains to route Nmap traffic through multiple proxies.
    - Example:
      ```
      proxychains nmap -sS <target_ip>
      ```

13. **Customize Timing Parameters**:
    - Adjusting timing parameters can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap -T0 <target_ip>
      ```

14. **Use IP Fragmentation**:
    - IP fragmentation can help in evading firewall rules that block fragmented packets.
    - Example:
      ```
      nmap -f -Pn <target_ip>
      ```

15. **Use Different Source IPs**:
    - Changing the source IP address can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap -S source_ip <target_ip>
      ```

16. **Use Scripting Engine for Advanced Evasion**:
    - Nmap scripting engine (NSE) provides scripts that can be used for advanced evasion techniques.
    - Example:
      ```
      nmap --script <script_name> <target_ip>
      ```

17. **Use IP Protocol Scan**:
    - Scanning using different IP protocols can sometimes bypass firewall rules.
    - Example:
      ```
      nmap -sO <target_ip>
      ```

18. **Use Timing Template Paranoid**:
    - Timing template "Paranoid" can be used for extremely stealthy scans.
    - Example:
      ```
      nmap -T0 <target_ip>
      ```

19. **Use Source Port Randomization**:
    - Randomizing the source port can sometimes help in evading detection.
    - Example:
      ```
      nmap --source-port 0-65535 <target_ip>
      ```

20. **Use IP Options**:
    - Adding IP options to packets can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap --ip-options LSRR <target_ip>
      ```

21. **Use Source IP Spoofing**:
    - Spoofing the source IP address can help in bypassing firewall rules and disguising the true origin of the scan.
    - Example:
      ```
      nmap -S spoofed_ip <target_ip>
      ```

22. **Use Different IP Fragmentation Techniques**:
    - Experimenting with different IP fragmentation techniques can sometimes bypass firewall rules that block fragmented packets.
    - Example:
      ```
      nmap --mtu 8 <target_ip>
      ```

23. **Use IP Identification Field Manipulation**:
    - Manipulating the IP identification field can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --ip-id 42 <target_ip>
      ```

24. **Use TCP Window Size Manipulation**:
    - Manipulating the TCP window size can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --mtu 8 <target_ip>
      ```

25. **Use Different Scan Techniques Sequentially**:
    - Running different scan techniques sequentially can sometimes bypass firewall rules that are specific to certain scan types.
    - Example:
      ```
      nmap -sS; -sU; -sT <target_ip>
      ```

26. **Use Custom TCP Options**:
    - Adding custom TCP options to packets can sometimes bypass firewall rules.
    - Example:
      ```
      nmap --tcp-options 0x29 <target_ip>
      ```

27. **Use Source Routing**:
    - Source routing can help in bypassing firewall rules by specifying the route that packets should take.
    - Example:
      ```
      nmap --route-source <route> <target_ip>
      ```

28. **Use TCP SYN Cookies**:
    - Enabling TCP SYN cookies can sometimes help in bypassing firewall rules that block SYN packets.
    - Example:
      ```
      nmap --tcp-options 2 <target_ip>
      ```

29. **Use Custom Payloads**:
    - Sending custom payloads in packets can sometimes bypass firewall rules that are based on packet content.
    - Example:
      ```
      nmap --data <custom_payload> <target_ip>
      ```

30. **Use Different Timing Templates**:
    - Experimenting with different timing templates can sometimes bypass IDS/IPS that are configured to detect scan patterns.
    - Example:
      ```
      nmap -T paranoid <target_ip>
      ```

31. **Use TCP Timestamps**:
    - Enabling TCP timestamps can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap --tcp-options 1 <target_ip>
      ```

32. **Use TCP Initial Window Size Manipulation**:
    - Manipulating the TCP initial window size can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --initial-window 42 <target_ip>
      ```

33. **Use Different Scripting Engine Options**:
    - Experimenting with different scripting engine options can sometimes bypass IDS/IPS that are configured to detect specific Nmap scripts.
    - Example:
      ```
      nmap --script-args=<script_args> <target_ip>
      ```

34. **Use Different Scan Ports**:
    - Scanning different ports can sometimes bypass firewall rules that are specific to certain ports.
    - Example:
      ```
      nmap -p 80,443,8080 <target_ip>
      ```

35. **Use IP Options Padding**:
    - Adding padding to IP options field can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap --ip-options 0x1 <target_ip>
      ```
Certainly! Here are more examples of Nmap commands with techniques that can help in bypassing firewalls, IDS/IPS, and load balancers:

36. **Use Source IP Routing**:
    - Source IP routing can help in bypassing firewall rules by specifying the route that packets should take.
    - Example:
      ```
      nmap --source-ip-routing <target_ip>
      ```

37. **Use Source Port Randomization**:
    - Randomizing the source port can sometimes help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --source-port 0-65535 <target_ip>
      ```

38. **Use Fragmented TCP Packets**:
    - Sending fragmented TCP packets can help in bypassing firewall rules that are configured to block certain types of packets.
    - Example:
      ```
      nmap -f <target_ip>
      ```

39. **Use Source IP Address Spoofing with Decoys**:
    - Spoofing the source IP address with decoys can help in confusing IDS/IPS systems.
    - Example:
      ```
      nmap -S decoy_ip1,decoy_ip2 <target_ip>
      ```

40. **Use TCP ACK Flag Probe**:
    - Sending TCP ACK flag probes can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap -sA <target_ip>
      ```

41. **Use TCP FIN Flag Probe**:
    - Sending TCP FIN flag probes can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap -sF <target_ip>
      ```

42. **Use TCP XMAS Flag Probe**:
    - Sending TCP XMAS flag probes can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap -sX <target_ip>
      ```

43. **Use TCP NULL Flag Probe**:
    - Sending TCP NULL flag probes can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap -sN <target_ip>
      ```

44. **Use TCP Window Scaling Option**:
    - Using TCP window scaling option can help in bypassing firewall rules that limit the window size.
    - Example:
      ```
      nmap --window 1024 <target_ip>
      ```

45. **Use TCP Urgent Pointer Option**:
    - Using TCP urgent pointer option can help in bypassing firewall rules that inspect TCP urgent data.
    - Example:
      ```
      nmap --urgency 0xFF <target_ip>
      ```

46. **Use IP Source Routing Option**:
    - Using IP source routing option can help in bypassing firewall rules that block source-routed packets.
    - Example:
      ```
      nmap --ip-options <source_routing_options> <target_ip>
      ```

47. **Use Randomized TCP Initial Sequence Numbers (ISNs)**:
    - Using randomized TCP ISNs can help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --rand-source <target_ip>
      ```

48. **Use IP Packet Padding**:
    - Adding padding to IP packets can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap --ip-packet-padding <target_ip>
      ```

49. **Use TCP Timestamps Option**:
    - Using TCP timestamps option can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap --tcp-option 8 <target_ip>
      ```

50. **Use TCP Initial Window Scaling**:
    - Using TCP initial window scaling option can help in bypassing firewall rules that limit the initial window size.
    - Example:
      ```
      nmap --initial-window 512 <target_ip>
      ```

51. **Use TCP/IP Stack Fingerprinting**:
    - Nmap can use TCP/IP stack fingerprinting to mimic the behavior of known operating systems, making it harder for firewalls and IDS/IPS to detect the scan.
    - Example:
      ```
      nmap -O <target_ip>
      ```

52. **Use Source IP Spoofing with IPID Incrementation**:
    - Spoofing the source IP address with IPID incrementation can help in bypassing firewall rules that inspect IPID values.
    - Example:
      ```
      nmap --spoof-mac spoofed_mac --source-ip spoofed_ip --ip-id-response <target_ip>
      ```

53. **Use Different Protocol Scans**:
    - Scanning using different protocols such as UDP, TCP, and SCTP can sometimes bypass firewall rules that are specific to certain protocols.
    - Example:
      ```
      nmap -sU -sT -sS <target_ip>
      ```

54. **Use Packet Timing Manipulation**:
    - Manipulating packet timing parameters such as delay and interval can help in bypassing firewall and IDS/IPS rules.
    - Example:
      ```
      nmap --min-rtt-timeout 500ms --max-rtt-timeout 1000ms <target_ip>
      ```

55. **Use Source Port Randomization with Decoys**:
    - Randomizing the source port with decoys can help in confusing IDS/IPS systems and bypassing firewall rules.
    - Example:
      ```
      nmap -g 53 -D decoy1,decoy2 <target_ip>
      ```

56. **Use IP Fragmentation with Different Fragment Offset Values**:
    - Experimenting with different IP fragmentation offset values can sometimes bypass firewall rules that block fragmented packets.
    - Example:
      ```
      nmap --fragment-offset 7,14,21 <target_ip>
      ```

57. **Use IP Options with Different Values**:
    - Adding different IP options with varying values to packets can sometimes help in bypassing firewall rules.
    - Example:
      ```
      nmap --ip-options 0x2,0x4,0x6 <target_ip>
      ```

58. **Use Different Network Routes**:
    - Routing Nmap traffic through different network routes can sometimes help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --route <route1>,<route2>,<route3> <target_ip>
      ```

59. **Use Custom Payloads with Different Lengths**:
    - Sending packets with custom payloads of different lengths can sometimes bypass firewall rules that inspect packet content.
    - Example:
      ```
      nmap --data-length 100,200,300 <target_ip>
      ```

60. **Use TCP Flag Manipulation**:
    - Manipulating TCP flags such as SYN, ACK, FIN, RST, PSH, and URG can sometimes help in evading detection by IDS/IPS.
    - Example:
      ```
      nmap --tcp-flag SYN,ACK,FIN <target_ip>
      ```

61. **Use Different Scan Timing Options**:
    - Experimenting with different scan timing options can sometimes help in bypassing IDS/IPS and firewall rules that are configured to detect specific scan patterns.
    - Example:
      ```
      nmap -T0, -T2, -T4 <target_ip>
      ```

62. **Use TCP Sequence Number Prediction**:
    - Predicting TCP sequence numbers can sometimes help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap --predict-dest --badsum <target_ip>
      ```

63. **Use Source IP Spoofing with Random Source Ports**:
    - Spoofing the source IP address with random source ports can help in bypassing firewall rules and IDS/IPS systems.
    - Example:
      ```
      nmap --source-port 0-65535 --spoof-mac random <target_ip>
      ```

64. **Use Different TCP Window Sizes**:
    - Experimenting with different TCP window sizes can sometimes help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --window 1024, --window 2048, --window 4096 <target_ip>
      ```

65. **Use IP Option Record Route**:
    - Using IP option record route can help in bypassing firewall rules and IDS/IPS detection by specifying the route that packets should take.
    - Example:
      ```
      nmap --ip-options RR <target_ip>
      ```

66. **Use Fragmented UDP Packets**:
    - Sending fragmented UDP packets can sometimes help in bypassing firewall rules that are configured to block certain types of packets.
    - Example:
      ```
      nmap -f -sU <target_ip>
      ```

67. **Use Randomized Scan Order**:
    - Randomizing the order in which ports are scanned can sometimes help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --randomize-hosts <target_ip>
      ```

68. **Use TCP SYN Stealth Scan with Different Delay Values**:
    - Using TCP SYN stealth scan with different delay values can sometimes help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap -sS --max-rtt-timeout 100ms --min-rtt-timeout 50ms <target_ip>
      ```

69. **Use Different Scan Techniques for Different Ports**:
    - Using different scan techniques for different ports can sometimes help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap -sT -p 80 -sU -p 53 <target_ip>
      ```

70. **Use Source IP Spoofing with Randomized IPID Values**:
    - Spoofing the source IP address with randomized IPID values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --source-ip spoofed_ip --ip-id-response <target_ip>
      ```

Certainly! Here are more techniques that can be used in combination with Nmap to enhance evasion and bypass security mechanisms:

71. **Use TCP ACK Flag Probe with Randomized Sequence Numbers**:
    - Sending TCP ACK flag probes with randomized sequence numbers can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sA --source-port 0-65535 --rand-seed 12345 <target_ip>
      ```

72. **Use TCP SYN Scan with Randomized TTL Values**:
    - Using TCP SYN scan with randomized TTL (Time to Live) values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --ttl 1-255 <target_ip>
      ```

73. **Use TCP Window Scaling Option with Different Scale Factors**:
    - Using TCP window scaling option with different scale factors can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --window 64 --ws 3 <target_ip>
      ```

74. **Use IP Source Routing Option with Randomized Routes**:
    - Using IP source routing option with randomized routes can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options RTR <target_ip>
      ```

75. **Use TCP Timestamps Option with Different Timestamp Values**:
    - Using TCP timestamps option with different timestamp values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --tcp-option 8:12345678 <target_ip>
      ```

76. **Use TCP Initial Window Scaling with Randomized Values**:
    - Using TCP initial window scaling option with randomized values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --initial-window 1024-65535 <target_ip>
      ```

77. **Use TCP Initial Sequence Number Prediction with Randomized Sequence Numbers**:
    - Using TCP initial sequence number prediction with randomized sequence numbers can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap --badsum --randomize-hosts <target_ip>
      ```

78. **Use IP ID Field Manipulation with Randomized ID Values**:
    - Using IP ID field manipulation with randomized ID values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-id <source_ip> <target_ip>
      ```

79. **Use TCP Null Flag Probe with Randomized Options**:
    - Using TCP null flag probes with randomized options can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sN --tcp-option 7:1234 <target_ip>
      ```

80. **Use Source Port Randomization with TCP SYN Stealth Scan**:
    - Randomizing the source port with TCP SYN stealth scan can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --source-port 1024-65535 <target_ip>
      ```

81. **Use TCP ACK Flag Probe with Randomized TTL Values**:
    - Sending TCP ACK flag probes with randomized TTL (Time to Live) values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sA --ttl 1-255 <target_ip>
      ```

82. **Use IP Option Record Route with Randomized Route Length**:
    - Using IP option record route with randomized route length can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options RECORD_ROUTE:2 <target_ip>
      ```

83. **Use IP Fragmentation with Randomized Fragment Offset**:
    - Sending fragmented packets with randomized fragment offset values can help in bypassing firewall rules that block fragmented packets.
    - Example:
      ```
      nmap -f --mtu 32 <target_ip>
      ```

84. **Use Different Scan Intensity Levels**:
    - Experimenting with different scan intensity levels can sometimes help in bypassing IDS/IPS and firewall rules.
    - Example:
      ```
      nmap -T1, -T2, -T3 <target_ip>
      ```

85. **Use TCP SYN Scan with Randomized Source IP Addresses**:
    - Sending TCP SYN scan with randomized source IP addresses can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --spoof-mac random <target_ip>
      ```

86. **Use TCP ACK Flag Probe with Randomized Options**:
    - Sending TCP ACK flag probes with randomized options can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sA --tcp-option 6:1234 <target_ip>
      ```

87. **Use IP Source Routing Option with Randomized Pointer Length**:
    - Using IP source routing option with randomized pointer length can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options SSRR:4 <target_ip>
      ```

88. **Use IPID Incrementation with Randomized Increment Value**:
    - Using IPID incrementation with randomized increment value can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options RR --ip-id 0x1234 <target_ip>
      ```

89. **Use TCP Window Scaling Option with Randomized Shift Count**:
    - Using TCP window scaling option with randomized shift count can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --window 64 --ws 3 <target_ip>
      ```

90. **Use TCP SYN Stealth Scan with Randomized Delay Values**:
    - Using TCP SYN stealth scan with randomized delay values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --max-rtt-timeout 200ms --min-rtt-timeout 50ms <target_ip>
      ```
Certainly! Here are more techniques that can be used in conjunction with Nmap to enhance evasion and bypass security mechanisms:

91. **Use IP Source Routing Option with Randomized Route Length**:
    - Utilizing IP source routing option with randomized route length can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options SSRR:4 <target_ip>
      ```

92. **Use TCP FIN Flag Probe with Randomized TTL Values**:
    - Sending TCP FIN flag probes with randomized TTL (Time to Live) values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sF --ttl 1-255 <target_ip>
      ```

93. **Use IPID Incrementation with Randomized Initial ID Value**:
    - Using IPID incrementation with randomized initial ID value can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-id 1234-5678 <target_ip>
      ```

94. **Use TCP XMAS Flag Probe with Randomized Sequence Numbers**:
    - Sending TCP XMAS flag probes with randomized sequence numbers can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sX --source-port 0-65535 --rand-seed 12345 <target_ip>
      ```

95. **Use IPID Incrementation with Randomized Increment Value**:
    - Using IPID incrementation with randomized increment value can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options RR --ip-id 0x1234 <target_ip>
      ```

96. **Use TCP FIN Flag Probe with Randomized Initial Sequence Numbers**:
    - Sending TCP FIN flag probes with randomized initial sequence numbers can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sF --seq 12345678 <target_ip>
      ```

97. **Use TCP SYN Stealth Scan with Randomized Source Ports and Sequence Numbers**:
    - Using TCP SYN stealth scan with randomized source ports and sequence numbers can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --source-port 0-65535 --sequence 12345678 <target_ip>
      ```

98. **Use TCP Null Flag Probe with Randomized TTL Values**:
    - Sending TCP null flag probes with randomized TTL (Time to Live) values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sN --ttl 1-255 <target_ip>
      ```

99. **Use IPID Incrementation with Randomized Increment Value and Fragmented Packets**:
    - Using IPID incrementation with randomized increment value along with fragmented packets can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap -f --ip-id 0x1234 <target_ip>
      ```

100. **Use TCP SYN Stealth Scan with Randomized TTL Values**:
    - Using TCP SYN stealth scan with randomized TTL (Time to Live) values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --ttl 1-255 <target_ip>
      ```

101. **Use IP Source Routing Option with Randomized Route Entries**:
    - Utilizing IP source routing option with randomized route entries can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options SSRR:4 <target_ip>
      ```

102. **Use TCP ACK Flag Probe with Randomized Initial Sequence Numbers**:
    - Sending TCP ACK flag probes with randomized initial sequence numbers can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sA --seq 12345678 <target_ip>
      ```

103. **Use TCP SYN Stealth Scan with Randomized TCP Options**:
    - Using TCP SYN stealth scan with randomized TCP options can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --tcp-option 7:1234 <target_ip>
      ```

104. **Use IP Fragmentation with Randomized Fragment Identification Values**:
    - Sending fragmented packets with randomized fragment identification values can help in bypassing firewall rules that block fragmented packets.
    - Example:
      ```
      nmap -f --ip-id 1234-5678 <target_ip>
      ```

105. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and MAC Addresses**:
    - Using TCP SYN stealth scan with randomized source IP addresses and MAC addresses can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --spoof-mac random --source-ip random <target_ip>
      ```

106. **Use TCP Window Scaling Option with Randomized Scale Factors**:
    - Using TCP window scaling option with randomized scale factors can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --window 64 --ws 2-4 <target_ip>
      ```

107. **Use IP Source Routing Option with Randomized Pointer Values**:
    - Using IP source routing option with randomized pointer values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options SSRR:2-4 <target_ip>
      ```

108. **Use TCP SYN Stealth Scan with Randomized TCP Flags**:
    - Using TCP SYN stealth scan with randomized TCP flags can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --scanflags SYN,ACK <target_ip>
      ```

109. **Use IPID Incrementation with Randomized Increment Value and Fragmented Packets**:
    - Using IPID incrementation with randomized increment value along with fragmented packets can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap -f --ip-id 0x1234 <target_ip>
      ```

110. **Use TCP SYN Stealth Scan with Randomized Delay Values and Window Sizes**:
    - Using TCP SYN stealth scan with randomized delay values and window sizes can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --max-rtt-timeout 100ms --min-rtt-timeout 50ms --window 1024-65535 <target_ip>
      ```

111. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TTL Values**:
    - Using TCP SYN stealth scan with randomized source IP addresses and TTL (Time to Live) values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ttl 1-255 <target_ip>
      ```

112. **Use IPID Incrementation with Randomized Increment Value and TTL Values**:
    - Using IPID incrementation with randomized increment value and TTL (Time to Live) values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-id 0x1234 --ttl 1-255 <target_ip>
      ```

113. **Use TCP SYN Stealth Scan with Randomized IPID Values**:
    - Using TCP SYN stealth scan with randomized IPID values can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --ip-id 1234-5678 <target_ip>
      ```

114. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options**:
    - Using TCP SYN stealth scan with randomized source IP addresses and IP options can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 <target_ip>
      ```

115. **Use IP Fragmentation with Randomized Fragment Offset and TTL Values**:
    - Sending fragmented packets with randomized fragment offset and TTL (Time to Live) values can help in bypassing firewall rules that block fragmented packets.
    - Example:
      ```
      nmap -f --mtu 32 --ttl 1-255 <target_ip>
      ```

116. **Use TCP SYN Stealth Scan with Randomized TCP Options and Window Scaling Factors**:
    - Using TCP SYN stealth scan with randomized TCP options and window scaling factors can help in evading detection by IDS/IPS and bypassing firewall rules.
    - Example:
      ```
      nmap -sS --tcp-option 7:1234 --ws 2-4 <target_ip>
      ```

117. **Use IP Source Routing Option with Randomized Source IP Addresses and Pointer Values**:
    - Using IP source routing option with randomized source IP addresses and pointer values can help in bypassing firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options SSRR:2-4 --source-ip random <target_ip>
      ```


119. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TCP Window Sizes**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses and TCP window sizes to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --window 1024-65535 <target_ip>
      ```

120. **Use IP Fragmentation with Randomized Fragment Offset and TTL Values**:
    - Employ IP fragmentation with a randomized fragment offset and TTL values to bypass firewall rules blocking fragmented packets.
    - Example:
      ```
      nmap -f --mtu 32 --ttl 1-255 <target_ip>
      ```

121. **Use TCP SYN Stealth Scan with Randomized TCP Options and Window Scaling Factors**:
    - Utilize TCP SYN stealth scan with randomized TCP options and window scaling factors to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --tcp-option 7:1234 --ws 2-4 <target_ip>
      ```

122. **Use IP Source Routing Option with Randomized Source IP Addresses and Pointer Values**:
    - Implement IP source routing option with randomized source IP addresses and pointer values to bypass firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-options SSRR:2-4 --source-ip random <target_ip>
      ```

123. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TCP Flags**:
    - Use TCP SYN stealth scan with randomized source IP addresses and TCP flags to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --scanflags SYN,ACK <target_ip>
      ```

124. **Use IPID Incrementation with Randomized Increment Value and TTL Values**:
    - Apply IPID incrementation with randomized increment value and TTL values to bypass firewall rules and IDS/IPS detection.
    - Example:
      ```
      nmap --ip-id 0x1234 --ttl 1-255 <target_ip>
      ```

125. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses and IP options to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 <target_ip>
      ```

126. **Use TCP SYN Stealth Scan with Randomized IPID Values**:
    - Use TCP SYN stealth scan with randomized IPID values to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --ip-id 1234-5678 <target_ip>
      ```

127. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TCP Options**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses and TCP options to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --tcp-option 7:1234 <target_ip>
      ```

128. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TCP Flags and Options**:
    - Use TCP SYN stealth scan with randomized source IP addresses, TCP flags, and options to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --scanflags SYN,ACK --tcp-option 7:1234 <target_ip>
      ```

129. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options and TTL Values**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses, IP options, and TTL values to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 --ttl 1-255 <target_ip>
      ```

130. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TCP Flags and Window Sizes**:
    - Use TCP SYN stealth scan with randomized source IP addresses, TCP flags, and window sizes to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --scanflags SYN,ACK --window 1024-65535 <target_ip>
      ```

131. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options and TCP Flags**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses, IP options, and TCP flags to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 --scanflags SYN,ACK <target_ip>
      ```

132. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and TCP Options and Window Sizes**:
    - Use TCP SYN stealth scan with randomized source IP addresses, TCP options, and window sizes to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --tcp-option 7:1234 --window 1024-65535 <target_ip>
      ```

133. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options and TCP Flags and Window Sizes**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses, IP options, TCP flags, and window sizes to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 --scanflags SYN,ACK --window 1024-65535 <target_ip>
      ```

134. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options and TCP Flags and TCP Options**:
    - Use TCP SYN stealth scan with randomized source IP addresses, IP options, TCP flags, and TCP options to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 --scanflags SYN,ACK --tcp-option 7:1234 <target_ip>
      ```

135. **Use TCP SYN Stealth Scan with Randomized Source IP Addresses and IP Options and TCP Flags and TTL Values**:
    - Utilize TCP SYN stealth scan with randomized source IP addresses, IP options, TCP flags, and TTL values to evade detection by IDS/IPS and bypass firewall rules.
    - Example:
      ```
      nmap -sS --source-ip random --ip-options RECORD_ROUTE:4 --scanflags SYN,ACK --ttl 1-255 <target_ip>
      ```
