1. **Enumerate Shares on a Host with Verbose Output:**
```bash
smbmap -H <host> -v
```
This command will provide verbose output, giving more detailed information about the discovered shares on the target host.

2. **Authenticate Using a Specific Domain:**
```bash
smbmap -H <host> -u <username> -p <password> -d <domain>
```
Replace `<domain>` with the appropriate domain name for authentication.

3. **Enumerate Files and Directories within a Specific Share:**
```bash
smbmap -H <host> -u <username> -p <password> -s <share>
```
Replace `<share>` with the name of the specific share you want to enumerate. This command will list the files and directories within the specified share.

4. **Enumerate Shares on Multiple Hosts from a File:**
```bash
for host in $(cat hosts.txt); do smbmap -H $host; done
```
Assuming you have a file named `hosts.txt` containing a list of target hosts, this command will iterate over each host in the file and enumerate the shares on each one.

5. **Enumerate Shares and Attempt Access with Null Session:**
```bash
smbmap -H <host> --null
```
This command will attempt to connect to the target host using a null session, which means it will not provide any credentials. It's useful for checking if anonymous access is allowed on the SMB shares.

6. **Enumerate Shares and List Files with Verbose Output:**
```bash
smbmap -H <host> -u <username> -p <password> -s <share> -v
```
This command combines authentication with verbose output to list files and directories within a specific share on the target host.

7. **Enumerate Shares on a Host with Default Credentials:**
```bash
smbmap -H <host> -u guest
```
This command attempts to enumerate shares on the target host using the default guest credentials. It's useful for quickly checking if anonymous access is allowed.

8. **Enumerate Shares and Save Output to a File:**
```bash
smbmap -H <host> -u <username> -p <password> > smbmap_output.txt
```
