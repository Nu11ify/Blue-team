## SOC L1 Alert Reporting
### Alert funnel
Proceeding with an alert requires reporting. This should contain: 
- Alert comment - What is it about
- Investigation - Document steps taken, whats found and why you close/escalate/question the alert.

Flags## SOC L1 Alert Reporting
### Alert funnel
Proceeding with an alert requires reporting. This should contain: 
- Alert comment - What is it about
- Investigation - Document steps taken, whats found and why you close/escalate/question the alert.

Flags
1. What is the process of passing suspicious alerts to an L2 analyst for review?
   `Alert escalation`
2. What is the process of formally describing alert details and findings?
   `Alert reporting`

### Reporting guide
As an L1 its important to note:
- Context for escalation - Who, what, where // "Hvem, hva, hvor"
- Save the findings! - Important for evidence and escalation
Five W's:
1. Who - Who did it?
2. What - What happened?
3. When - When did it happen?
4. Where - Where did it happen? Device, ip, website etc
5. Why - Why are you taking the actions you are taking

Flag:
- According to the SOC dashboard, which user email leaked the sensitive document?
  `m.boslan@tryhackme.thm`
- Looking at the new alerts, who is the "sender" of the suspicious, likely phishing email?
  `support@microsoft.com`
- Open the phishing alert, read its details, and try to understand the activity.
  Using the Five Ws template, what flag did you receive after writing a good report? **Note**: Assign yourself, move the alert to In Progress, and fill in the Analyst Comment.
  Report:
  ```
  Who - Sent from support@microsoft.com to user Eddie Huffman, IT manager, e.huggman@tryhackme.thm
when - Mar 27th 2025, 19:25 CET
where - Email. Phishing email was sent but detected post delivery. SPF FAIL DKIM FAIL. File "REPORT.rar" attached. Email instructs user to open attached file.
why - Sender email looks legit and is sent to IT manager, which could classify it as a real email. Attached file "REPORT.rar". L1 finds it suspicious why microsoft support would need user to download and open a file, specifically .rar files which could contain encrypted/compressed malicious files.
  ```
Flag: `THM{nice_FLAG-VALUE_support}`


1. What is the process of passing suspicious alerts to an L2 analyst for review?
   `Alert escalation`
2. What is the process of formally describing alert details and findings?
   `Alert reporting`

### Reporting guide
As an L1 its important to note:
- Context for escalation - Who, what, where // "Hvem, hva, hvor"
- Save the findings! - Important for evidence and escalation
Five W's:
1. Who - Who did it?
2. What - What happened?
3. When - When did it happen?
4. Where - Where did it happen? Device, ip, website etc
5. Why - Why are you taking the actions you are taking

Flag:
- According to the SOC dashboard, which user email leaked the sensitive document?
  `m.boslan@tryhackme.thm`
- Looking at the new alerts, who is the "sender" of the suspicious, likely phishing email?
  `support@microsoft.com`
- Open the phishing alert, read its details, and try to understand the activity.
  Using the Five Ws template, what flag did you receive after writing a good report? **Note**: Assign yourself, move the alert to In Progress, and fill in the Analyst Comment.
  Report:
  ```
  Who - Sent from support@microsoft.com to user Eddie Huffman, IT manager, e.huggman@tryhackme.thm
when - Mar 27th 2025, 19:25 CET
where - Email. Phishing email was sent but detected post delivery. SPF FAIL DKIM FAIL. File "REPORT.rar" attached. Email instructs user to open attached file.
why - Sender email looks legit and is sent to IT manager, which could classify it as a real email. Attached file "REPORT.rar". L1 finds it suspicious why microsoft support would need user to download and open a file, specifically .rar files which could contain encrypted/compressed malicious files. Deemed suspicious and probably malicious.
  ```
Flag: `THM{nice_FLAG-VALUE_support}`
