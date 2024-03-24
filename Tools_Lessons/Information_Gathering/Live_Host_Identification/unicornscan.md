1. **TCP Port Scan**:
   ```
   unicornscan -mT <target_ip>
   ```

2. **UDP Port Scan**:
   ```
   unicornscan -mU <target_ip>
   ```

3. **Scan Specific Ports**:
   ```
   unicornscan -mT -p 80,443,8080 <target_ip>
   ```

4. **Scan Port Ranges**:
   ```
   unicornscan -mT -p 1-1000 <target_ip>
   ```

5. **Scan All Ports**:
   ```
   unicornscan -mT -p 1-65535 <target_ip>
   ```

6. **Output to XML**:
   ```
   unicornscan -mT -Iu <target_ip>
   ```

7. **Output to CSV**:
   ```
   unicornscan -mT -Ic <target_ip>
   ```

8. **Verbose Output**:
   ```
   unicornscan -mT -v <target_ip>
   ```

9. **Scan Multiple Targets**:
   ```
   unicornscan -mT <target1_ip> <target2_ip> <target3_ip>
   ```

10. **Scan Entire Subnet**:
    ```
    unicornscan -mT 192.168.1.0/24
    ```

11. **Scan using a Specific Network Interface**:
    ```
    unicornscan -mT -i eth0 <target_ip>
    ```

12. **Scan with Custom Packet Size**:
    ```
    unicornscan -mT -s 64 <target_ip>
    ```
