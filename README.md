# IT Support Homelab: Windows Server + Client Lab

## Project Overview
This homelab is a hands-on IT support and system administration project built to practice Windows Server administration, client configuration, network troubleshooting, and later Active Directory management and ServiceNow-related support workflows.

The lab currently includes:
- 1 Windows Server VM
- 1 Windows Client VM
- Static IP address configuration on both machines
- Basic connectivity testing and troubleshooting

## Goal
The goal of this lab is to simulate a small real-world IT environment and document the setup, troubleshooting steps, and administrative tasks in a structured way that can be shared on GitHub as a portfolio project.

## Lab Environment
### Host Machine
- Laptop with 32 GB RAM
- 6 CPU cores

### Virtual Machines
#### Server VM
- Role: Windows 2025 Server for future Active Directory and DNS setup
- Configuration: Static IP assigned

#### Client VM
- Role: Domain-join client for future administration testing
- Configuration: Static IP assigned

## Network Setup
Both virtual machines were configured with static IP addresses so they could communicate consistently inside the lab environment.

Structure:
- Server: `192.168.50.10`
- Client: `192.168.50.20`
- Subnet Mask: `255.255.255.0`

## Progress So Far
### Completed
- Created the Server VM
- Created the Client VM
- Assigned static IP addresses to both systems
- Tested connectivity between machines using `ping`
- Install AD DS + DNS on Server VM

### Issue Encountered
The initial ping test failed even though the IP settings were configured.

### Troubleshooting
I investigated the connectivity issue and found that the Windows Firewall settings were blocking the ping response. After enabling **File and Printer Sharing** in the firewall settings, the ping test worked successfully.

### What I Learned
This issue showed that successful IP configuration alone does not guarantee connectivity. Host firewall settings can prevent network testing tools such as ping from working, so basic firewall checks are an important troubleshooting step in a Windows environment.

## Skills Practiced
- Virtual machine setup
- Static IP configuration
- Basic Windows networking
- Connectivity testing with ping
- Firewall troubleshooting
- Documentation of lab steps and issues

## Next Steps
The next phase of this lab will include:
- Promoting the server to a Domain Controller
- Configuring DNS
- Joining the client machine to the domain
- Creating users, groups, and organizational units
- Practicing help desk style administrative tasks
- Building a separate ServiceNow practice workflow using a Personal Developer Instance

## Repository Structure
```text
it-support-homelab/
├─ README.md
├─ docs/
│  ├─ lab-overview.md
│  ├─ network-config.md
│  ├─ build-log.md
│  ├─ troubleshooting.md
│  └─ next-steps.md
├─ screenshots/
│  ├─ server/
│  ├─ client/
│  └─ networking/
└─ scripts/
   └─ command-prompt/
