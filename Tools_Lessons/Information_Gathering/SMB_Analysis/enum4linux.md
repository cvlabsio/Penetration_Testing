### Basic Usage:
```bash
enum4linux <target_ip>
```

### Options:

1. `-U`: Get user list.
    - Example: `enum4linux -U <target_ip>`

2. `-M`: Get machine list.
    - Example: `enum4linux -M <target_ip>`

3. `-S`: Get share list.
    - Example: `enum4linux -S <target_ip>`

4. `-P`: Get password policy information.
    - Example: `enum4linux -P <target_ip>`

5. `-G`: Get group and member list.
    - Example: `enum4linux -G <target_ip>`

6. `-d`: Detailed output for users and shares.
    - Example: `enum4linux -d <target_ip>`

7. `-u <user>`: Specify username.
    - Example: `enum4linux -u <username> <target_ip>`

8. `-p <pass>`: Specify password.
    - Example: `enum4linux -p <password> <target_ip>`

9. `-r`: Enumerate users via RID cycling.
    - Example: `enum4linux -r <target_ip>`

10. `-R <range>`: RID ranges to enumerate.
    - Example: `enum4linux -R 500-550,1000-1050 <target_ip>`

11. `-K <n>`: Keep searching RIDs until n consecutive RIDs don't correspond to a username.
    - Example: `enum4linux -K <n> <target_ip>`

12. `-l`: Get limited info via LDAP 389/TCP (for DCs only).
    - Example: `enum4linux -l <target_ip>`

13. `-s <file>`: Brute force guessing for share names.
    - Example: `enum4linux -s <file> <target_ip>`

14. `-k <user>`: User(s) that exist on the remote system.
    - Example: `enum4linux -k <user> <target_ip>`

15. `-o`: Get OS information.
    - Example: `enum4linux -o <target_ip>`

16. `-i`: Get printer information.
    - Example: `enum4linux -i <target_ip>`

17. `-w <wrkg>`: Specify workgroup manually.
    - Example: `enum4linux -w <workgroup> <target_ip>`

18. `-n`: Do an nmblookup (similar to nbtstat).
    - Example: `enum4linux -n <target_ip>`

19. `-v`: Verbose mode. Shows full commands being run.
    - Example: `enum4linux -v <target_ip>`

20. `-A`: Aggressive mode. Do write checks on shares etc.
    - Example: `enum4linux -A <target_ip>`

### Additional options:

- `-a`: Do all simple enumeration.
    - Example: `enum4linux -a <target_ip>`

- `-h`: Display help message and exit.
    - Example: `enum4linux -h`

### More Example:
```bash
enum4linux -a 192.168.1.100
```
### Examples:

1. **Enumerate Users and Shares with Detailed Output:**
```bash
enum4linux -d <target_ip>
```

2. **Enumerate Users via RID Cycling:**
```bash
enum4linux -r <target_ip>
```

3. **Specify RID Ranges to Enumerate:**
```bash
enum4linux -R 500-550,1000-1050 <target_ip>
```

4. **Keep Searching RIDs Until n Consecutive RIDs Don't Correspond to a Username:**
```bash
enum4linux -K <n> <target_ip>
```

5. **Get Limited Info via LDAP (for Domain Controllers Only):**
```bash
enum4linux -l <target_ip>
```

6. **Brute Force Guessing for Share Names from a File:**
```bash
enum4linux -s <filename> <target_ip>
```

7. **Specify Users that Exist on the Remote System:**
```bash
enum4linux -k <user1,user2> <target_ip>
```

8. **Get OS Information:**
```bash
enum4linux -o <target_ip>
```

9. **Get Printer Information:**
```bash
enum4linux -i <target_ip>
```

10. **Specify Workgroup Manually:**
```bash
enum4linux -w <workgroup> <target_ip>
```

11. **Do an Nmblookup (Similar to Nbtstat):**
```bash
enum4linux -n <target_ip>
```

12. **Verbose Mode (Shows Full Commands Being Run):**
```bash
enum4linux -v <target_ip>
```

13. **Aggressive Mode (Do Write Checks on Shares, etc.):**
```bash
enum4linux -A <target_ip>
```

14. **Do All Simple Enumeration:**
```bash
enum4linux -a <target_ip>
```

15. **Display Help Message and Exit:**
```bash
enum4linux -h
```

16. **Enumerate Users and Shares with Detailed Output:**
```bash
enum4linux -d <target_ip>
```

17. **Enumerate Users via RID Cycling:**
```bash
enum4linux -r <target_ip>
```

18. **Specify RID Ranges to Enumerate:**
```bash
enum4linux -R 500-550,1000-1050 <target_ip>
```

19. **Keep Searching RIDs Until n Consecutive RIDs Don't Correspond to a Username:**
```bash
enum4linux -K <n> <target_ip>
```

20. **Get Limited Info via LDAP (for Domain Controllers Only):**
```bash
enum4linux -l <target_ip>
```

21. **Brute Force Guessing for Share Names from a File:**
```bash
enum4linux -s <filename> <target_ip>
```

22. **Specify Users that Exist on the Remote System:**
```bash
enum4linux -k <user1,user2> <target_ip>
```

21. **Get OS Information:**
```bash
enum4linux -o <target_ip>
```

22. **Get Printer Information:**
```bash
enum4linux -i <target_ip>
```

23. **Specify Workgroup Manually:**
```bash
enum4linux -w <workgroup> <target_ip>
```

24. **Do an Nmblookup (Similar to Nbtstat):**
```bash
enum4linux -n <target_ip>
```

25. **Verbose Mode (Shows Full Commands Being Run):**
```bash
enum4linux -v <target_ip>
```

26. **Aggressive Mode (Do Write Checks on Shares, etc.):**
```bash
enum4linux -A <target_ip>
```

27. **Do All Simple Enumeration:**
```bash
enum4linux -a <target_ip>
```

28. **Display Help Message and Exit:**
```bash
enum4linux -h
```
