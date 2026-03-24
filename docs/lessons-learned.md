# Lessons Learned

## Lesson 1: Networking problems are not always caused by IP settings
Even though both VMs had valid static IP addresses, the ping test still failed. This showed that correct addressing alone does not guarantee connectivity.

## Lesson 2: Firewall settings can affect basic network testing
The failed ping was caused by Windows Firewall blocking the traffic. After enabling File and Printer Sharing, connectivity worked.

## Lesson 3: Documentation is part of technical work
Keeping a written record of setup steps, errors, and fixes makes the lab easier to understand and easier to present as a portfolio project.

## Lesson 4: Small labs still reflect real IT skills
Even with only one server and one client, this lab already demonstrates VM setup, IP planning, troubleshooting, and environment organization.
