# IT Home Lab Portfolio

Hands-on IT home lab projects using **Ubuntu Server on an Apple Silicon Mac with UTM and a Windows 11 environment**.

This portfolio documents practical experience with Linux and Windows system administration, user account management, access controls, endpoint security, system monitoring, network diagnostics, and technical troubleshooting.

These projects demonstrate foundational technical skills relevant to **IT Support, Technical Support Engineering, Service Desk, Systems Administration, and Cybersecurity** roles.

## Projects

| Project | Status | Skills Demonstrated |
|---|---|---|
| [00 - Ubuntu VM Setup](00-Ubuntu-VM-Setup/README.md) | Completed | Virtual machines, Ubuntu Server installation, UTM configuration, Linux CLI |
| [01 - Linux User Management and Permissions](01-Linux-User-Management-and-Permissions/README.md) | Completed | User accounts, groups, chmod, chgrp, access controls, troubleshooting |
| [02 - Linux System Monitoring and Network Troubleshooting](02-Linux-System-Monitoring-and-Network-Troubleshooting/README.md) | Completed | CPU and memory monitoring, disk usage, DNS, systemd, logs, SSH diagnostics |
| [03 - Windows System Administration and Security](03-Windows-System-Administration/README.md) | Completed | Windows administration, endpoint security, Group Policy, Event Viewer, file sharing, remote access |
| [04 - Linux Networking and Troubleshooting](04-Linux-Networking-Troubleshooting/README.md) | Completed | Network interfaces, IPv4 and IPv6, ICMP, DNS resolution, routing, default gateway verification |

## Technical Skills

- **Operating Systems:** Windows 11, Ubuntu Server, Linux CLI
- **Virtualization:** UTM, ARM64 virtual machines
- **User Administration:** Local users and groups, account management, Linux file permissions, access controls
- **Windows Administration:** Microsoft Management Console (MMC), Group Policy, Device Manager, Windows Services, Event Viewer
- **Endpoint Security:** Microsoft Defender, security scans, BitLocker verification, Windows Update
- **Networking:** IPv4, IPv6, DHCP, DNS, ICMP, routing tables, default gateways, HTTP/HTTPS connectivity testing
- **Remote Access:** Remote Desktop Protocol (RDP), SSH diagnostics
- **System Diagnostics:** Process monitoring, memory and disk usage, system services, journal logs, Sysinternals
- **Troubleshooting:** Root cause investigation, command-line diagnostics, testing solutions, and verifying results
- **Technical Documentation:** GitHub, Markdown, screenshot documentation, troubleshooting procedures

## Troubleshooting Highlights

### Linux File Permissions
Investigated an access-denied issue caused by restricted parent directory permissions. Relocated the shared directory to `/srv/it-files` and verified authorized access.

### User Access Control
Tested file access for authorized and unauthorized users, modified group membership, and confirmed that removing permissions revoked access.

### Network Connectivity and DNS
Verified external network connectivity using public IP addresses and domain names. Examined network interfaces, routing tables, DHCP-assigned addresses, and default gateway connectivity.

Successfully verified local and external connectivity with 0% packet loss during controlled ICMP tests.

### Linux System Services
Investigated systemd service status, reviewed system logs, monitored resource utilization, and checked for failed services.

### Windows System Administration
Created and managed local user accounts, investigated system events, reviewed Windows services, configured remote access, and tested file-sharing functionality.

### Windows Endpoint Security
Performed Microsoft Defender security scans, reviewed Windows Update settings, examined local security configurations, and verified BitLocker status.

## Tools and Technologies

- Ubuntu Server
- Windows 11
- UTM Virtualization
- Bash and Linux Command Line
- Microsoft Management Console (MMC)
- Microsoft Defender
- Windows Event Viewer
- Group Policy Editor
- Sysinternals
- Remote Desktop Protocol (RDP)
- GitHub and Markdown

## Project Documentation

Each project includes a dedicated README explaining its objectives, tools, procedures, troubleshooting steps, and results.

Selected screenshots provide evidence of hands-on lab activities, including:

- Linux command execution
- User account and access-control testing
- System performance monitoring
- Network connectivity verification
- Windows administration
- Endpoint security configuration
- Technical troubleshooting

All projects were completed in a personal home lab environment for practical learning and professional skill development.

## Ongoing Development

This portfolio will continue to expand with additional hands-on projects focused on:

- Technical support and troubleshooting
- Windows Server and Active Directory
- Networking and infrastructure
- API testing and monitoring
- Cloud computing and administration
- Cybersecurity and system hardening
- IT automation

The goal of this portfolio is to demonstrate practical technical abilities, structured troubleshooting, continuous learning, and the ability to document and communicate technical solutions effectively.
