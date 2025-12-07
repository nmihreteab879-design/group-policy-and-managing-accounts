<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

# Active Directory – Account Lockouts, Disabled Accounts & Security Logging

## Environments and Technologies Used
- Microsoft Azure (Virtual Machines)
- Remote Desktop Protocol (RDP)
- Active Directory Users and Computers (ADUC)
- Local Security Policy / Group Policy
- Event Viewer (Security Logs)

## Operating Systems Used
- Windows Server (Domain Controller)
- Windows 10 (Client Machine)

## Objectives
- Configure account lockout threshold and duration  
- Trigger, identify, and resolve account lockouts  
- Reset passwords and restore user access  
- Disable and re-enable domain accounts  
- Analyze security logs for authentication events  
- Understand how AD detects and tracks failed logins  

# Core Security Operations Overview

What I did:

Configured the account lockout threshold, duration, and reset timers through Group Policy, applied the policy to the domain, and verified the settings on the Domain Controller.

## Configuring Account Lockout Threshold via Group Policy  

 <img width="1147" height="566" alt="image" src="https://github.com/user-attachments/assets/07420315-c61c-4d5c-b22e-7b65eedcccab" />

Why this matters:

Account lockout policies are a fundamental security control. Setting thresholds prevents password-guessing attacks and helps enforce organizational security standards.

 Skills demonstrated
- Editing Group Policy Objects  
- Navigating Account Policies → Account Lockout Policy  
- Applying GPO settings to the domain  
- Understanding authentication security controls
  

 ## Account Lockout Testing  

 What I did:

Intentionally failed login attempts to trigger an account lockout, then observed how the lockout was enforced on the client and reflected in Active Directory.

<img width="450" height="485" alt="image" src="https://github.com/user-attachments/assets/8ba40e2d-593e-4f29-8ad9-6ac13235c304" />

<img width="552" height="145" alt="image" src="https://github.com/user-attachments/assets/9f547a28-9d17-4f71-865c-0f8120c40a82" />

 Why this matters:
 
Account lockouts happen constantly in real organizations—users forget passwords, fat-finger credentials, or get locked out because of mapped drives or mobile devices.  
Understanding how lockouts occur and how to fix them is one of the most common help desk responsibilities.

Skills demonstrated
- Identifying account lockout conditions  
- Testing authentication failures  
- Understanding how domain passwords are validated  
- Using ADUC to monitor and manage account state  


 ## Unlocking & Resetting Locked Accounts  
 
 What I did:

Unlocked the locked-out account in ADUC, reset the password, and tested authentication to ensure the user could sign in again.

<img width="700" src="(insert screenshot of user properties showing 'Unlock Account')"/>
<img width="411" height="540" alt="image" src="https://github.com/user-attachments/assets/e63fb430-fed5-4aff-9d4d-8c7d3a4258c4" />
<img width="517" height="513" alt="image" src="https://github.com/user-attachments/assets/7c78767b-f813-4bde-9103-432c6c1f7e85" />

 Why this matters:
 
Unlocking accounts is a daily task for help desk and system administrators.  
Knowing how to quickly unlock and reset a password keeps users productive and prevents unnecessary escalation.

  Skills demonstrated
- Unlocking accounts in ADUC  
- Resetting passwords securely  
- Verifying successful authentication after remediation  


## Enabling & Disabling Accounts  

What I did:

Disabled a user account in ADUC, attempted authentication to confirm the lockout behavior, then re-enabled the account and verified restored access.

<img width="700" src="(insert screenshot of disabled account icon)"/>
<img width="516" height="511" alt="image" src="https://github.com/user-attachments/assets/62e0415e-0734-4823-a7d9-061d84a31604" />
<img width="517" height="513" alt="image" src="https://github.com/user-attachments/assets/42679b33-2902-4a4f-9f67-3b0ea5d817b2" /> 


 Why this matters:
 
Disabling accounts is a critical step in employee offboarding, incident response, and security protection.  
Knowing how to disable/enable accounts is basic operational security.

  Skills demonstrated
- Disabling user accounts  
- Re-enabling accounts  
- Diagnosing login failures caused by account status  


 ## Observing Security Logs  
 
 What I did:

Opened Event Viewer on both the Domain Controller and the client machine, located authentication event logs, and reviewed failed login and lockout events.

<img width="700" src="(insert screenshot of Event Viewer logs)"/>
<img width="1536" height="988" alt="image" src="https://github.com/user-attachments/assets/0bcd1590-e1d8-4441-82ca-edd60496f6ad" />

 Why this matters:
 
Security logs are the beginning of all real cybersecurity work.  
Failed logins, lockouts, and authentication attempts are valuable indicators for SOC analysts and system administrators.

 Skills demonstrated
- Reviewing Windows Event Viewer logs  
- Identifying failed logon events  
- Understanding where authentication logs live on DCs and clients  
- Recognizing security-related event IDs  
