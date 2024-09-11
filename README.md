محمد عبد الجليل علي الذبحاني.  // 
امن سيبراني مجموعه (1) سنه ثانيه
1. **Display the current working directory:**
   
```bash

   pwd

   ```

2. **List all the contents of your current directory, including hidden files:**
   
```bash
   
ls -a
   
```

3. **Change your directory to the `Desktop`:**
  
 ```bash
   cd ~/Desktop
   ```

4. **Create two directories named `dir1` and `dir2` on the Desktop:**
   ```bash
   mkdir dir1 dir2
   ```

5. **Inside `dir1`, create a file named `file1.txt`:**
   ```bash
   touch dir1/file1.txt
   ```

6. **Inside `dir2`, create a file named `file2.txt`:**
   ```bash
   touch dir2/file2.txt
   ```

7. **Using nano or vim, write the numbers 1 to 9 into `file1.txt`:**
   ```bash
   nano dir1/file1.txt
   ```
   (ثم اكتب الأرقام واحفظ الملف.)

8. **From the home directory, copy the contents of `file1.txt` into `file2.txt`:**
   ```bash
   cp dir1/file1.txt dir2/file2.txt
   ```

9. **From the home directory, delete `file1.txt` inside `dir1`:**
   ```bash
   rm dir1/file1.txt
   ```

10. **Remove the directory `dir1` from the Desktop:**
    ```bash
    rmdir dir1
    ```

11. **Redirect the output of the network configuration command to a file named `network_info.txt` on the Desktop:**
    ```bash
    ifconfig > ~/Desktop/network_info.txt
    ```

### Section 2: Users and Groups Management

12. **Create a new user with your name:**
    ```bash
    sudo adduser yourname
    ```

13. **Set a password for your user:**
    ```bash
    sudo passwd yourname
    ```

14. **Open the file that contains user information:**
    ```bash
    cat /etc/passwd
    ```

15. **Add your user to the file that gives administrative privileges:**
    ```bash
    sudo usermod -aG sudo yourname
    ```

16. **Create a new group named `testgroup`:**
    ```bash
    sudo groupadd testgroup
    ```

17. **Add your user to `testgroup`:**
    ```bash
    sudo usermod -aG testgroup yourname
    ```

18. **Remove your user from the file that gives administrative privileges:**
    ```bash
    sudo deluser yourname sudo
    ```

19. **Check if your user still has administrative privileges:**
    ```bash
    groups yourname
    ```

20. **Check which groups your user belongs to:**
    ```bash
    groups yourname
    ```

### Section 3: Permissions and Ownership

21. **Set the permissions of `file2.txt` to allow the owner to read, write, and execute; the group to read and execute; and others to read:**
    ```bash
    chmod 755 dir2/file2.txt
    ```

22. **Check the permissions of `file2.txt`:**
    ```bash
    ls -l dir2/file2.txt
    ```

23. **Change the ownership of `file2.txt` to your user:**
    ```bash
    sudo chown yourname:yourname dir2/file2.txt
    ```

24. **Verify the ownership of `file2.txt`:**
    ```bash
    ls -l dir2/file2.txt
    ```

25. **Change back the ownership of a file `file2.txt`:**
    ```bash
    sudo chown previous_owner:previous_group dir2/file2.txt
    ```

26. **Grant write permission to everyone for `file2.txt`:**
    ```bash
    chmod a+w dir2/file2.txt
    ```

27. **Remove the write permission for the group and others for `file2.txt`:**
    ```bash
    chmod go-w dir2/file2.txt
    ```

28. **Delete `file2.txt` after making the necessary ownership and permission changes:**
    ```bash
    rm dir2/file2.txt
    ```

29. **Change the permissions of all files and directories inside a folder named `project` to `755`:**
    ```bash
    chmod -R 755 project/
    ```

### Section 4: Process Management

30. **Install a system monitor tool that provides an interactive process viewer (htop):**
    ```bash
    sudo apt install htop
    ```

31. **Display all running processes:**
    ```bash
    ps aux
    ```

32. **Display a tree of all running processes:**
    ```bash
    pstree
    ```

33. **Open the interactive process viewer and identify a process by its PID:**
    ```bash
    htop
    ```

34. **Kill a process with a specific PID:**
    ```bash
    kill PID_NUMBER
    ```

35. **Start an application and stop it using a command that kills processes by name:**
    ```bash
    pkill application_name
    ```

36. **Restart the application, then stop it using the interactive process viewer:**
    (قم بتشغيل التطبيق ثم استخدم `htop` لايقافه.)

37. **Run a command in the background, then bring it to the foreground:**
    ```bash
    command & 
    fg
    ```

38. **Check how long the system has been running:**
    ```bash
    uptime
    ```

39. **List all jobs running in the background:**
    ```bash
    jobs
    ```

### Section 5: Networking Commands

40. **Display the network configuration:**
    ```bash
    ifconfig
    ```

41. **Check the IP address of your machine:**
    ```bash
    hostname -I
    ```

42. **Test connectivity to an external server:**
    ```bash
    ping external_server_ip_or_domain
    ```

43. **Display the routing table:**
    ```bash
    route -n
    ```

44. **Check the open ports and active connections:**
    ```bash
    netstat -tuln
    ```

45. **Show the IP address of the host machine and the VM:**
    ```bash
    ifconfig
    ```

46. **Trace the route to an external server:**
    ```bash
    traceroute external_server_ip_or_domain
    ```

47. **Find the default gateway:**
    ```bash
    ip route | grep default
    ```

48. **Check the MAC address of your network interface:**
    ```bash
    ip link show
    ```
### Section 6: UFW Firewall

53. **Enable the firewall:**
   ```bash
   sudo ufw enable
   ```

54. **Allow SSH connections through the firewall:**
   ```bash
   sudo ufw allow ssh
   ```

55. **Deny all incoming traffic by default:**
   ```bash
   sudo ufw default deny incoming
   ```

56. **Allow HTTP and HTTPS traffic:**
   ```bash
   sudo ufw allow http
   sudo ufw allow https
   ```

57. **Allow port 20:**
   ```bash
   sudo ufw allow 20
   ```

58. **Reset the firewall settings:**
   ```bash
   sudo ufw reset
   ```

59. **Delete a rule from the firewall:**
   ```bash
   sudo ufw delete allow http
   ```

60. **Disable the firewall:**
   ```bash
   sudo ufw disable
   ```

61. **View the status of the firewall:**
   ```bash
   sudo ufw status
   ```

62. **Log firewall activity and view it:**
   ```bash
   sudo ufw logging on
   sudo less /var/log/ufw.log
   ```

### Section 7: Searching and System Information

63. **Delete the command history:**
   ```bash
   history -c
   ```

64. **Search for a kali in the `/etc/passwd` file:**
   ```bash
   grep "kali" /etc/passwd
   ```

65. **Search for a kali in the `/etc/group` file:**
   ```bash
   grep "kali" /etc/group
   ```

66. **Locate the `passwd` file:**
   ```bash
   locate passwd
   ```

67. **Locate the shadow file and open it:**
   ```bash
   sudo less /etc/shadow
   ```

68. **Search for all configuration files in the `/etc` directory:**
   ```bash
   ls /etc/*.conf
   ```

69. **Search recursively for a specific word in the `/var/log` directory:**
   ```bash
   grep -r "specific_word" /var/log/
   ```

70. **View the system’s kernel version:**
   ```bash
   uname -r
   ```

71. **Display the system’s memory usage:**
   ```bash
   free -h
   ```
