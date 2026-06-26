# Authentication Analysis

## Objective

Analyze authentication-related events from Windows and Linux systems using Wazuh. The goal is to compare the failed login activity, successful login activity and Linux privilege activity from a SOC analyst perspective.## Events Reviewed

| Event Type | Platform | Event ID / Indicator | Description | Status |
|---|---|---|---|---|
| Failed Logon | Windows | 4625 | Failed authentication attempt on Windows endpoint | Expected test event |
| Successful Logon | Windows | 4624 | Successful authentication on Windows endpoint | Expected test event |
| Sudo Command Execution | Linux | COMMAND=/usr/bin/whoami | User executed a command with elevated privileges | Expected test event |

## Analysis

The windows failed login event showed an unsuccessful authentication attempt on the monitored windows endpoint. Multiple failed login attempts can be indication of password guessing, brute force activity or unauthorized access attempts.

The windows successful login event showed a normal regular successful login authentication event. Successful login attempts are important to review because they help us to confirm whether access occured before or after any suspicious activity.

The linux sudo command execution event showed that a user executed a command with elevated priviliges. The command observed was 'COMMAND=/usr/bin/whoami'. In real world environment, sudo activity is important because it can indicate administrative behaviour, privilege escalation or suspicious command execution.

In this lab, all three events were expected because they were intentionally generated for testing and learning purposes.

## Conclusion

The authentication events were a intentionally generated test events. The investigation confirmed that Wazuh can collect and display Windows authentication events and Linux privilege-related activity.