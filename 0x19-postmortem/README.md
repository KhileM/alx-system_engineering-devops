Issue Summary
Duration of the outage: The outage started at 10:00 AM GMT on October 11, 2023, and ended at 12:30 PM GMT on the same day.
Impact: The main website was down, causing an inability for users to access our services. Approximately 60% of our users were affected.
Root cause: A misconfiguration in the Nginx server led to the outage.

Timeline
10:00 AM: The issue was detected through our monitoring alert system which showed a spike in 5xx HTTP status codes.
10:15 AM: Initial investigation began, focusing on recent deployments and database integrity.
10:45 AM: The issue was escalated to the site reliability team after initial checks found no issues with recent deployments or database integrity.
11:30 AM: A misleading path was taken when investigating potential DDoS attacks.
12:00 PM: The root cause was identified as a misconfiguration in the Nginx server.
12:30 PM: The incident was resolved after reconfiguring the Nginx server.
Root Cause and Resolution
Root cause: An incorrect rewrite rule in the Nginx configuration was causing requests to be incorrectly routed, leading to “404 Not Found” errors being returned to users.
Resolution: The incorrect rewrite rule in the Nginx configuration file was identified and corrected, and the Nginx server was restarted.

Corrective and Preventative Measures
Improvements/Fixes: Improve monitoring of server configurations and implement automated checks for configuration files before deployment.

Tasks:
Patch Nginx server with correct configuration (Done)
Add monitoring on Nginx server configuration (To Do)
Implement automated checks for configuration files (To Do)
