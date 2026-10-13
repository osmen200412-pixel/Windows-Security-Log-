Windows Security Log Analysis

1. Project Overview

This project demonstrates hands-on practice in Windows Security Log Analysis using Windows Event Viewer in a TryHackMe Windows Threat Detection lab.

The objective is to investigate Windows authentication events, understand successful and failed logons, and identify activity that may require further security investigation.

2. Objectives

- Analyze Windows Security Event IDs 4624 and 4625.
- Understand successful and failed logon attempts.
- Learn about Windows Logon Types 3 and 10.
- Review account and authentication details.
- Document investigation findings and security recommendations.

3. Tools Used

- TryHackMe — Windows Threat Detection
- Windows Event Viewer
- Windows Security Audit Logs

4. Security Event Analysis

Event ID 4624 — Successful Logon

Event ID 4624 indicates a successful logon.

During the lab, I examined authentication details, including the target account, logon type, authentication package, and logon process.

Observed lab details:

- Target Account: Administrator
- Logon Type: 3
- Authentication Package: NTLM
- Logon Process: NtLmSsp

Analysis: A network logon was recorded for the Administrator account. Additional investigation is needed to determine whether the activity was expected or suspicious.

Event ID 4625 — Failed Logon

Event ID 4625 indicates a failed logon attempt.

Failed logons may result from incorrect passwords or other legitimate causes. However, repeated failures may indicate suspicious activity and require further investigation.

Investigation steps:

- Review the number and timing of failed attempts.
- Identify affected accounts and available source IP information.
- Check for successful logons following repeated failures.
- Determine whether the activity is expected or suspicious.

Logon Type 10 — Remote Interactive Logon

Logon Type 10 is associated with remote interactive logons, commonly through Remote Desktop Protocol (RDP).

Investigation steps:

- Review the source IP address and timestamp.
- Identify the account involved.
- Correlate related authentication events.
- Verify whether the remote access was authorized.

5. Security Recommendations

- Monitor repeated failed logon attempts.
- Investigate unexpected privileged account logons.
- Restrict RDP access to authorized users and systems.
- Enable multi-factor authentication where supported.
- Use SIEM tools to correlate authentication events.
- Escalate suspicious activity according to incident-response procedures.

6. Key Learning Outcomes

This project strengthened my practical understanding of:

- Windows Security Event IDs.
- Authentication log analysis.
- Logon types and remote access activity.
- Initial security investigation techniques.
- Evidence documentation and security recommendations.

7. Evidence

Screenshots from the TryHackMe lab and Windows Event Viewer are included in this repository to demonstrate practical investigation activities.

8. Disclaimer

This project was completed in a controlled cybersecurity training environment. The findings represent lab observations and do not independently establish that a real-world security incident occurred.

Author

Cybersecurity | SOC Analyst Skills | Windows Security Monitoring
