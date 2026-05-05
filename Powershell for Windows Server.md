# PowerShell for Windows Server – Core Fundamentals

This document captures my foundational learning and practical experience using PowerShell for Windows Server administration, automation, and system management. PowerShell is a critical tool in enterprise environments for managing services, users, networking, and Active Directory through command-line automation.

PowerShell is built on a simple Verb-Noun command structure, where commands (cmdlets) such as Get-Service or Set-ExecutionPolicy allow administrators to interact directly with the system.

In system administration, I learned how to retrieve system information using commands such as Get-ComputerInfo and Get-CimInstance Win32_OperatingSystem, which provide detailed operating system and hardware information. For monitoring active system activity, I used Get-Process to view running processes and Get-Service to inspect system services.

Service management is a core function of PowerShell administration. I practiced starting, stopping, and restarting services using commands like Start-Service -Name "Spooler", Stop-Service -Name "Spooler", and Restart-Service -Name "DNS". These commands are essential when managing system services in real environments where uptime and troubleshooting are critical.

Networking is another key area of Windows Server administration. I learned how to view and verify network configurations using Get-NetIPConfiguration and Get-NetAdapter. For connectivity testing, Test-NetConnection google.com was used to diagnose network reachability and troubleshoot DNS or routing issues.

File and directory management was also part of my learning. I used PowerShell to create directories with New-Item -Path "C:\Lab" -ItemType Directory, create files with New-Item -Path "C:\Lab\test.txt" -ItemType File, copy files using Copy-Item, and remove files using Remove-Item. These operations are important for system organization and automation tasks.

In local system administration, I explored user and group management. I created local users using New-LocalUser, assigned them passwords securely using ConvertTo-SecureString, and added users to administrative groups using Add-LocalGroupMember -Group "Administrators". I also listed existing users with Get-LocalUser to understand system account structure.

For enterprise environments, I learned Active Directory administration using PowerShell. After importing the ActiveDirectory module with Import-Module ActiveDirectory, I was able to create domain users using New-ADUser, retrieve users using Get-ADUser -Filter *, and manage group membership using Add-ADGroupMember. These skills are essential for managing centralized identity systems in organizations.

System administration tasks such as restarting or shutting down servers were also covered using Restart-Computer and Stop-Computer. To check system uptime, I used a combination of Get-Date and CIM system queries to determine how long the system has been running.

PowerShell scripting introduced automation concepts, where logic can be applied to system tasks. I used conditional statements such as if (Get-Service -Name "Spooler") { "Service is running" } to build basic decision-making scripts. I also learned how to filter processes using Get-Process | Where-Object {$_.CPU -gt 100}, which is useful for performance monitoring and troubleshooting.

From a security and operations perspective, PowerShell plays a major role in automation, auditing, and incident response. It allows administrators to monitor system activity, manage users at scale, detect anomalies, and automate repetitive tasks that would otherwise be time-consuming.

Overall, PowerShell has proven to be an essential skill for Windows Server administration and cybersecurity operations. It bridges system management, automation, and security, making it a core tool for enterprise IT environments.

My next learning focus includes PowerShell remoting (WinRM), advanced scripting, Active Directory automation at scale, logging and audit automation, and integration with security monitoring tools such as SIEM platforms.
