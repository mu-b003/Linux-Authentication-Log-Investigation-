# Incident Summary

## Scenario

An SSH brute-force attack was simulated against a Linux system in an isolated lab environment. Authentication logs were analyzed to identify failed logins, successful authentication, user activity, and privilege escalation attempts.

## Findings

- Multiple failed SSH login attempts were detected.
- The attacker successfully authenticated after several failed attempts.
- All suspicious activity originated from a single source IP.
- A privilege escalation attempt using `su` failed.
- No unauthorized root access was observed.
- Administrative actions were performed only by the legitimate administrator.

## Conclusion

The investigation successfully reconstructed the attack timeline using Linux authentication logs and confirmed that no root compromise occurred.
