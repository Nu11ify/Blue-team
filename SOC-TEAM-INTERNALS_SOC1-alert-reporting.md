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
  Using the Five Ws template, what flag did you receive after writing a good report? 
  Note: Assign yourself, move the alert to In Progress, and fill in the Analyst Comment.
  Report:
```
Who - Sent from support@microsoft.com to user Eddie Huffman, IT manager, e.huggman@tryhackme.thm
when - Mar 27th 2025, 19:25 CET
where - Email. Phishing email was sent but detected post delivery. SPF FAIL DKIM FAIL. File "REPORT.rar" attached. Email instructs user to open attached file.
why - Sender email looks legit and is sent to IT manager, which could classify it as a real email. Attached file "REPORT.rar". L1 finds it suspicious why microsoft support would need user to download and open a file, specifically .rar files which could contain encrypted/compressed malicious files.
```
Flag: `THM{nice_FLAG-VALUE_support}`

### Escalation guide
Escalate to L2? Depends on team setup.
Ex. Phishing -> L1 escalates to L2 -> L2 rotates user creds // L2 checks of "Phishing test for user".

Stuck on an alert? Request support from L2, include 5W's.

Flags:
2. Who is your current L2 in the SOC dashboard that you can assign (escalate) the alerts to?
  `E.Fleming`
3. What flag did you receive after correctly escalating the alert from the previous task to L2?  
   Note: Set the right assignee and add an intermediate verdict (TP or FP)
`THM{good_FLAG-VALUE_alert}`

4. Now, investigate the second new alert and provide a detailed alert comment.  
What flag did you get after escalating this alert according to the workflow?

Report:
```
Who - NT AUTHORITY\SYSTEM, 
What - Multiple AD discovery commands executed as SYSTEM. Possibly malicious. "dir hostname whoami /priv net group "Domain Admins" /domain nltest /dclist:tryhackme.thm"
When - Mar 27th 2025 at 19:56
Where - DMZ-MSEXCHANGE-2013
Why - revshell.exe seen as parent process. Source process is sys32 cmd.exe. L1 suspects malicious activity with AD discovery and breached system.  
```
Flag - `THM{looks_FLAG-VALUE_exchange}`


### SOC Communication
- Escalate to next emergency contact/L2 if L2 does not respond within specified time.
- Do not contact user via breached unit or communication platform.
- Flooded with alerts? Triage and prioritise. Inform L2 and potentially request support if flood is maintained over time.
- Missed an alert? Classified it wrong? Contact manager or L2, you might react before the threat actor initiates an attack or moves throughout the system(s)
- SIEM logs parsed incorrectly? Report to L2 or SOC engineer. Keep triaging and investigating.

Flags:
1. Should you first try to contact your manager in case of a critical threat (Yea/Nay)?
   `Nay`
2. Should you immediately contact your L2 if you think you missed the attack (Yea/Nay)?
   `Yea`
