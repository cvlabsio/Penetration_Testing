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

