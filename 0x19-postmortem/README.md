POSTMORTEM
Issue Summary:
•	Duration:
•	Start Time: February 20, 2024, 10:30 AM (EAT)
•	End Time: February 21, 2024, 1:45 PM (EAT)
•	Impact:
•	The user authentication service experienced a complete outage, affecting 80% of users.
•	Users, unfortunately, felt like they'd been given a temporary ban from the digital realm.
Timeline:
•	Issue Detected:
•	February 20, 2024, 10:30 AM (EAT) - A sudden spike in error rates triggered automated monitoring alerts.
•	Actions Taken:
•	The engineering team initiated an investigation into the authentication service.
•	Initial hunch: the database was misbehaving, but it turned out the database was innocent – just trying to mind its own business.
•	Misleading Paths:
•	Initial focus on the database proved misleading; no anomalies were found.
•	Even Sherlock takes a wrong turn now and then; our initial assumptions led us on a wild goose chase.
•	Escalation:
•	After unsuccessful attempts to resolve the issue, the incident was escalated to the senior engineering team at 11:45 AM (EAT).
•	Resolution:
•	Identified a misconfiguration in the load balancer settings, causing uneven distribution of authentication requests.
•	Adjusted the load balancer settings, reminding it that fairness is a virtue, and evenly distributed traffic once more resolving the issue by 1:45 PM (EAT).
Root Cause and Resolution:
•	Root Cause:
•	Turns out our load balancer had a secret preference for certain servers, causing a digital popularity contest.
•	Resolution:
•	Adjusted the load balancer configuration to evenly distribute traffic among authentication servers.
•	Conducted load testing to ensure the issue was fully resolved.
Corrective and Preventative Measures:
•	Improvements/Fixes:
•	Enhance monitoring capabilities to detect load balancer misconfigurations promptly.
•	Conduct regular load testing to simulate various traffic scenarios and identify potential issues.
•	Tasks to Address the Issue:
•	Implement automated alerts for load balancer configuration changes.
•	Develop a comprehensive load testing schedule and integrate it into the deployment pipeline.
•	Conduct a thorough review of the incident response process to streamline escalations.
Conclusion:
In conclusion, our authentication service momentarily embraced invisibility, causing confusion among users.
The mystery was solved when we found our load balancer playing favourites.
Lessons learned: even in the digital world, fairness matters, and load balancers need a gentle reminder to treat all servers equally. Now, let's raise a toast to fewer mysteries and more smooth sailing in the vast sea of IT adventures!
