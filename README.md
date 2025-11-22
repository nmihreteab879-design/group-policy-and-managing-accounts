<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" width="150"/>
</p>

 Active Directory – Account Lockouts, Disabling Accounts & Security Logging

This lab focuses on real-world identity security tasks: account lockouts, unlocking/resetting accounts, enabling/disabling user accounts, and reviewing authentication logs on both the Domain Controller and a client machine.


 Account Lockout Testing  
<img width="700" src="(insert screenshot of failed logins + lockout)"/>

 Why this matters
Account lockouts happen constantly in real organizations—users forget passwords, fat-finger credentials, or get locked out because of mapped drives or mobile devices.  
Understanding how lockouts occur and how to fix them is one of the most common help desk responsibilities.

Skills demonstrated
- Identifying account lockout conditions  
- Testing authentication failures  
- Understanding how domain passwords are validated  
- Using ADUC to monitor and manage account state  


 Configuring Account Lockout Threshold via Group Policy  
<img width="700" src="(insert screenshot of GPO settings)"/>

Why this matters
Account lockout policies are a fundamental security control. Setting thresholds prevents password-guessing attacks and helps enforce organizational security standards.

 Skills demonstrated
- Editing Group Policy Objects  
- Navigating Account Policies → Account Lockout Policy  
- Applying GPO settings to the domain  
- Understanding authentication security controls  


 Unlocking & Resetting Locked Accounts  
<img width="700" src="(insert screenshot of user properties showing 'Unlock Account')"/>

 Why this matters  
Unlocking accounts is a daily task for help desk and system administrators.  
Knowing how to quickly unlock and reset a password keeps users productive and prevents unnecessary escalation.

  Skills demonstrated
- Unlocking accounts in ADUC  
- Resetting passwords securely  
- Verifying successful authentication after remediation  


 Enabling & Disabling Accounts  
<img width="700" src="(insert screenshot of disabled account icon)"/>

 Why this matters  
Disabling accounts is a critical step in employee offboarding, incident response, and security protection.  
Knowing how to disable/enable accounts is basic operational security.

  Skills demonstrated
- Disabling user accounts  
- Re-enabling accounts  
- Diagnosing login failures caused by account status  


 Observing Security Logs  
<img width="700" src="(insert screenshot of Event Viewer logs)"/>

 Why this matters 
Security logs are the beginning of all real cybersecurity work.  
Failed logins, lockouts, and authentication attempts are valuable indicators for SOC analysts and system administrators.

 Skills demonstrated
- Reviewing Windows Event Viewer logs  
- Identifying failed logon events  
- Understanding where authentication logs live on DCs and clients  
- Recognizing security-related event IDs  
