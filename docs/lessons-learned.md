# Lessons Learned

## Lesson 1: Networking problems are not always caused by IP settings
Even though both VMs had valid static IP addresses, the ping test still failed. This showed that correct addressing alone does not guarantee connectivity.

## Lesson 2: Firewall settings can affect basic network testing
The failed ping was caused by Windows Firewall blocking the traffic. After enabling File and Printer Sharing, connectivity worked.

## Lesson 3: Documentation is part of technical work
Keeping a written record of setup steps, errors, and fixes makes the lab easier to understand and easier to present as a portfolio project.

## Lesson 4: Small labs still reflect real IT skills
Even with only one server and one client, this lab already demonstrates VM setup, IP planning, troubleshooting, and environment organization.

## Lesson 5: GPO changes may not apply immediately
Even after creating and linking a Group Policy Object, the client machine may still behave as if nothing changed. In this lab, CLIENT1 could still access Control Panel until the GPO was enforced and the machine was restarted.

## Lesson 6: Help desk tasks rely heavily on account and access management
Common support tasks such as password resets, account unlocks, disabling users, changing group membership, and assigning shared folder permissions are core parts of Windows administration and are important to practice repeatedly.
