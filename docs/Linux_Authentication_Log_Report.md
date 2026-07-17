# Linux Authentication Log Investigation Report

## Objective

Investigate Linux authentication logs to identify suspicious login activity and reconstruct the attack timeline.

## Lab Environment

- Ubuntu Linux
- SSH
- Nmap
- Hydra
- VMware Lab

## Attack Simulation

- User creation
- SSH service verification
- Port scanning
- SSH brute-force attack
- Successful authentication
- Privilege escalation attempt
- Session termination

## Investigation Steps

- Review failed logins
- Review successful logins
- Analyze SSH events
- Identify attacker IP
- Verify sudo activity
- Review session history
- Check privilege escalation attempts

## Evidence

Screenshots are available in the **evidence/** directory.

## Findings

- 5 failed SSH authentication attempts.
- 2 successful logins.
- Single attacker IP identified.
- Failed `su` privilege escalation.
- No successful root compromise.

## Conclusion

Authentication log analysis successfully identified the attack sequence and confirmed that administrative privileges were never obtained.
