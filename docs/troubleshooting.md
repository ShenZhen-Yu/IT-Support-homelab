```markdown
# Troubleshooting Notes

## Issue: Ping test failed between Server VM and Client VM

### Symptoms
- Both machines had static IP addresses configured
- Ping requests between the Server VM and Client VM failed

### Checks Performed
- Verified both VMs were powered on
- Confirmed IP addresses were in the same subnet
- Confirmed subnet mask matched
- Retested connectivity using `ping`

### Root Cause
The Windows Firewall settings were preventing ping traffic from being allowed.

### Fix
Enabled **File and Printer Sharing** in Windows Firewall settings.

### Result
After enabling the firewall setting, the ping test succeeded and network connectivity between the VMs worked.

### Lesson Learned
Even if IP addressing is configured correctly, firewall settings can still block connectivity tests such as ping. Basic firewall troubleshooting is an important first step in Windows network diagnostics.


# Troubleshooting Notes

## Issue 1: Could not promote the local Administrator account
### Symptoms
The server could not proceed with promotion because the local Administrator account had a blank password.

### Cause
Windows Server requires the Administrator account to have a valid password before certain administrative tasks can be completed.

### Fix
Used Command Prompt to set a password for the local Administrator account:

```cmd
net user administrator [NewPassword]
```

### Result
The account was updated with a valid password, and the setup could continue.

## Issue 2: CLIENT1 could not connect to the corp.local domain
### Symptoms
CLIENT1 was unable to join the domain.

### Cause
The client machine was not using the domain controller’s IPv4 address as its DNS server.

### Fix
Changed the preferred DNS server on CLIENT1 to the IPv4 address of the domain controller.

### Result
After correcting DNS, CLIENT1 was able to connect to and join the corp.local domain.

### Lesson Learned
When joining a Windows client to a domain, DNS must point to the domain controller, not a public DNS server.

## Issue 3: Unable to create a new domain user
### Symptoms
A new user account could not be created because the password was rejected.

### Cause
The password did not meet Windows password complexity requirements.

### Fix
Reviewed the Windows password policy and created a password that met the required standards.

### Result
The user account was created successfully.

### Lesson Learned
Active Directory user creation depends on password complexity rules, so password policy should always be checked when account creation fails.
