# Commands Used

This file contains the primary commands used during the Linux Authentication Log Investigation lab.

| Command | Purpose |
|---------|---------|
| `sudo adduser Afreen` | Create a test user. |
| `id Afreen` | Display user ID and group membership. |
| `sudo truncate -s 0 /var/log/auth.log` | Clear the authentication log. |
| `sudo journalctl --rotate` | Rotate systemd journal logs. |
| `sudo journalctl --vacuum-time=1s` | Remove old journal logs. |
| `sudo systemctl restart ssh` | Restart the SSH service. |
| `sudo systemctl status ssh` | Verify the SSH service status. |
| `ip a` | Display network interface information and IP address. |
| `nmap -sV <Target-IP>` | Scan the target for open ports and services. |
| `nano passwords.txt` | Create a password list for testing. |
| `hydra -l Afreen -P passwords.txt ssh://<Target-IP>` | Perform an SSH brute-force simulation. |
| `ssh Afreen@<Target-IP>` | Connect to the target using SSH. |
| `whoami` | Display the current user. |
| `hostname` | Display the system hostname. |
| `pwd` | Show the current working directory. |
| `id` | Display the current user's identity information. |
| `groups` | Show the current user's group memberships. |
| `sudo -l` | Check available sudo privileges. |
| `su root` | Attempt privilege escalation. |
| `passwd` | Attempt to change the user password. |
| `exit` | Close the SSH session. |
| `grep "Failed password" /var/log/auth.log` | Display failed login attempts. |
| `grep "Failed password" /var/log/auth.log \| wc -l` | Count failed login attempts. |
| `grep "Accepted password" /var/log/auth.log` | Display successful logins. |
| `grep "Accepted password" /var/log/auth.log \| wc -l` | Count successful logins. |
| `grep sshd /var/log/auth.log` | Show all SSH-related events. |
| `grep "Afreen" /var/log/auth.log` | Show all events related to the user. |
| `grep "192.168.81.128" /var/log/auth.log` | Filter events by source IP address. |
| `grep "sudo" /var/log/auth.log` | Review sudo activity. |
| `grep "COMMAND=" /var/log/auth.log` | Display commands executed through sudo. |
| `grep "su:" /var/log/auth.log` | Find privilege escalation attempts. |
| `grep "session opened for user root" /var/log/auth.log` | Check for root sessions. |
| `grep "passwd" /var/log/auth.log` | Review password change attempts. |
| `grep "session opened" /var/log/auth.log` | Display opened sessions. |
| `grep "session closed" /var/log/auth.log` | Display closed sessions. |
| `last` | Show login history. |
| `last Afreen` | Display login history for the Afreen account. |
| `grep "Afreen" /var/log/auth.log \| head -1` | Show the first event for the user. |
| `grep "Afreen" /var/log/auth.log \| tail -1` | Show the last event for the user. |
| `grep -oP '(?<=from )(\d{1,3}\.){3}\d{1,3}' /var/log/auth.log \| sort -u` | Extract unique source IP addresses. |
| `grep -E "Accepted\|Failed" /var/log/auth.log \| awk '{for(i=1;i<=NF;i++)if($i=="for")print $(i+1)}' \| sort -u` | Extract targeted usernames from authentication events. |

## Summary

These commands were used to:

- Generate authentication events.
- Simulate an SSH brute-force attack.
- Review authentication logs.
- Identify failed and successful logins.
- Investigate SSH activity.
- Verify privilege escalation attempts.
- Analyze user sessions.
- Correlate attacker IP addresses.
