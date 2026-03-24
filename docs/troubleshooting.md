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
