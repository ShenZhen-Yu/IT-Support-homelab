# Network Configuration

## Lab Network Design
The lab network is configured so the server and client can communicate consistently using static IP addresses.

## Virtual Machines
### Host
- Hostname: HOST
- Operating System: Windows 11 home 25H2
- IP Address: 192.168.50.1
- Subnet Mask: 255.255.255.0

### Server VM
- Hostname: SERVER
- Operating System: Windows Server 2025
- IP Address: 192.168.50.10
- Subnet Mask: 255.255.255.0

### Client VM
- Hostname: CLIENT1
- Operating System: Windows11 Enterprise 25H2
- IP Address: 192.168.50.20
- Subnet Mask: 255.255.255.0

## Network Type
- Hypervisor: VMware Workstation Pro
- Adapter Type: Host-Only
- Notes: VMs are connecting through Host-Only Network within the subnet 192.168.50.0/24

## Connectivity Testing
The first connectivity test was done using the `ping` command between the server and the client.

### Test Commands
- `ping 192.168.50.1
- `ping 192.168.50.10
- `ping 192.168.50.20

## Issue Found
The initial ping test failed even though the IP settings were correct.

## Resolution
After enabling **File and Printer Sharing** in Windows Firewall, the ping test succeeded.

## Final Result
Both systems are now able to communicate successfully over the lab network.
