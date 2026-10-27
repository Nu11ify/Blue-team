## Alert properties
Alert - Notification of an event

Triaging alerts
1. L1 - Reviews alerts and escalates real alerts and threats
2. L2 - Analytics and remediation
3. Engineer
4. Manager

Alert information
- Timestamp
- Name - What rule is triggered?
- Severity - Low, medium, high critical
- Status - New/Unassigned, in progress, closed/resolved
- Verdict - True positive, false positive
- Assignee - Alert owner
- Dscription
- Fields - Comments, hostname, alert information

Flags:
1. What was the verdict for the "Unusual VPN Login Location" alert?
   `False Positive`
2. What user was mentioned in the "Unusual VPN Login Location" alert?
   `M.Clark`


### Alert prioritization
To correctly prioritize alerts, it is important to have pre-filtered alerts and sorting by severity and time.

Flags:
1. Should you first prioritise medium over low severity alerts? (**Yea**/Nay)
2. Should you first take the newest alerts and then the older ones? (Yea/**Nay**)
3. Assign yourself to the first-priority alert and change its status to **In Progress**.
   The name of your selected alert will be the answer to the question.
   `Potential Data Exfiltration`

### Alert triage
Triage alerts based on the following information:
- SIEM alert
- Alert information
- Criticality
- False positive / True positive
- Need for escalation?
- Analytics comment

Flags:
1. Which flag did you receive after you correctly triaged the first-priority alert?
   `THM{looks_FLAG-VALUE_meetings}`
2. Which flag did you receive after you correctly triaged the second-priority alert?
   `THM{how_FLAG-VALUE_it?}`
3. Which flag did you receive after you correctly triaged the third-priority alert?
   `THM{should_FLAG-VALUE_devs?}`
