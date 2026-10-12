# Windows-Security-Log-
Windows Security Log Analysis

1. Project Overview

This project demonstrates hands-on practice in Windows security log analysis using Windows Event Viewer in a TryHackMe Windows Threat Detection lab.

The goal is to understand Windows authentication events, investigate successful and failed logons, and identify activity that may require further security investigation.

2. Objectives

- Analyze Windows Security Event IDs 4624 and 4625.
- Understand successful and failed authentication attempts.
- Learn about Windows Logon Types 3 and 10.
- Review account and authentication details.
- Document findings and recommend security improvements.

3. Tools Used

- TryHackMe – Windows Threat Detection
- Windows Event Viewer
- Windows Security Audit Logs

4. Security Events Investigated

Event ID 4624 – Successful Logon

Event ID 4624 indicates that a logon was successful.

During the lab investigation, I reviewed authentication details, including the target account, logon type, authentication package, and logon process.

Observed lab details:

- Target account: Administrator
- Logon Type: 3
- Authentication Package: NTLM
- Logon Process: NtLmSsp

Analysis: A network logon was recorded for the Administrator account. Additional investigation would be required to determine whether the activity was expected or suspicious.

Event ID 4625 – Failed Logon

Event ID 4625 indicates that a logon attempt failed.

Failed logons can occur for legitimate reasons, such as an incorrect password. However, repeated failures may require further investigation.

Investigation approach:

- Review the number and timing of failed attempts.
- Identify the affected accounts and available source information.
- Check for successful logons following repeated failures.
- Determine whether the activity matches expected user behavior.

Logon Type 10 – Remote Interactive Logon

Logon Type 10 is associated with remote interactive logons, commonly through Remote Desktop Protocol (RDP).

Investigation approach:

- Review the source IP address and timestamp.
- Identify the account involved.
- Correlate related authentication events.
- Check whether the remote access was authorized.

5. Security Recommendations

- Monitor repeated failed logon attempts.
- Investigate unexpected logons involving privileged accounts.
- Restrict RDP access to authorized users and systems.
- Enable multi-factor authentication where supported.
- Correlate Windows authentication events in a SIEM platform.
- Escalate suspicious activity according to incident-response procedures.

6. Key Learning Outcomes

Through this practical lab, I developed my understanding of:

- Windows Security Event IDs.
- Authentication log analysis.
- Logon types and remote access activity.
- Initial security investigation techniques.
- Documenting evidence and security recommendations.

7. Evidence

Screenshots from the training lab can be added here to demonstrate the investigation process and relevant event details.

8. Disclaimer

This project was completed in a controlled cybersecurity training environment. The observations documented here are based on lab activities and do not, by themselves, establish that a real-world security incident occurred.

Author

Cybersecurity | SOC Analyst Skills | Windows Security Monitoring
