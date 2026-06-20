# Linux Log Reporting

## Objective
Monitor and review linux logs for understanding events and activities in server.

## Tools Used
- Oracle VirtualBox
- Ubuntu Linux
- Linux authentication logs
- Wazuh Dashboard

## Investigation
Utilized linux log monitoring to monitor the authentication in linux. Used the auth.log file to monitor the logs. In other terminal used <code>sudo whoami</code> to monitor whether the event is being logged or not.

## Local Log Review
The sudo event was confirmed directly on the Linux system using authentication/system logs. The log showed that a user executed a command with elevated privileges.

## Wazuh Review
The event was then searched in the Wazuh dashboard to verify whether the SIEM collected and displayed the Linux activity. The Wazuh event details were reviewed, including timestamp, agent name, rule description, and full log content.

## Analysis
This sudo activity was expected because it was intentionally created as part of the lab. In a real SOC environment, sudo activity is important to monitor because it can show privilege escalation, administrative actions, or suspicious command execution.

## Conclusion
This was a benign test event. The activity confirmed that Linux privilege-related events can be reviewed through system logs and investigated using Wazuh.

## Skills Practiced
- Linux log review
- sudo activity monitoring
- Wazuh event searching
- SIEM-based log investigation
- Basic SOC documentation