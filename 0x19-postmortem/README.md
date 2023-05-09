# 0x19. Postmortem

## Issue Summary:
Duration: 2 hours, from 10:00 AM to 12:00 PM (PST)
Impact: The website's login functionality was down. Users attempting to log in were met with an error message, preventing them from accessing their accounts. 100% of users were affected. It's safe to say that the login feature had a case of the Mondays.
Root Cause: An issue with the authentication server caused the login functionality to fail. It turns out the server forgot its own password.

## Timeline:
- 10:00 AM: An engineer received an alert from the monitoring system indicating that the authentication server was not responding.
- 10:05 AM: The engineer tried to log in to the authentication server manually to see what was going on, but was met with the same error message as the users.
- 10:10 AM: The engineer began investigating the authentication server and found that it had indeed forgotten its password. They attempted to reset the password, but were unable to do so due to a bug in the password reset functionality.
- 11:00 AM: The engineer escalated the issue to the senior engineering team, who continued the investigation.
- 11:30 AM: The senior engineering team identified the bug in the password reset functionality and deployed a patch to fix it.
- 11:45 AM: The senior engineering team was able to reset the authentication server's password and verify that the login functionality was working again.
- 12:00 PM: The issue was resolved and the login feature was back up and running.

## Root cause and resolution:
The root cause of the issue was a bug in the password reset functionality of the authentication server, which prevented the engineer from resetting the server's password. The senior engineering team identified and patched the bug, and was able to reset the server's password, allowing the login functionality to work again.

## Corrective and preventative measures:
To prevent similar issues from occurring in the future, the engineering team will implement additional monitoring and alerting for the authentication server. They will also conduct a thorough review of the password reset functionality and update it as necessary to ensure it works properly. Finally, they will implement regular password rotations for the authentication server to prevent it from forgetting its password again.

In conclusion, while the login functionality was out for a while, the engineering team was able to get to the root cause of the issue and fix it. Hopefully, the corrective and preventative measures will prevent similar issues from occurring in the future, and we can all log in without any hiccups.
