# IT Home Lab Portfolio

Hands-on IT home lab projects using **Ubuntu Server on an Apple Silicon Mac with UTM**. This portfolio documents practical experience with Linux system administration, user account management, access controls, system monitoring, and network troubleshooting.

These projects demonstrate foundational technical skills relevant to **IT Help Desk, Service Desk, and Technical Support** roles.

## Projects

| Project | Status | Skills Demonstrated |
|---|---|---|
| [Ubuntu VM Setup](00-Ubuntu-VM-Setup/README.md) | Completed | Virtual machines, Ubuntu Server installation, UTM configuration, Linux CLI |
| [Linux User Management and Permissions](01-Linux-User-Management-and-Permissions/README.md) | Completed | User accounts, groups, chmod, chgrp, access controls, troubleshooting |
| [Linux System Monitoring and Network Troubleshooting](02-Linux-System-Monitoring-and-Network-Troubleshooting/README.md) | Completed | CPU and memory monitoring, disk usage, connectivity testing, DNS, systemd, logs, SSH diagnostics |

## Technical Skills

- **Operating Systems:** Ubuntu Server, Linux CLI
- **Virtualization:** UTM, ARM64 virtual machines
- **User Administration:** Linux users, groups, and permissions
- **Networking:** Ping, DNS resolution, HTTP connectivity testing
- **System Diagnostics:** Process monitoring, memory and disk usage, system services, journal logs
- **Troubleshooting:** Identifying permission issues, testing solutions, and verifying results

## Troubleshooting Highlights

- **Linux File Permissions:** Investigated an access-denied issue caused by restricted parent directory permissions. Relocated the shared directory to `/srv/it-files` and verified authorized access.
- **User Access Control:** Tested file access for authorized and unauthorized users, modified group membership, and confirmed that removing permissions revoked access.
- **Network Diagnostics:** Verified network connectivity, DNS resolution, and HTTPS communication using Linux command-line tools.
- **System Services:** Investigated systemd service status, reviewed logs, and checked for failed services.
  
## Project Documentation

Each project includes a dedicated README explaining its objectives, tools, procedures, troubleshooting steps, and results.

Selected screenshots provide evidence of hands-on lab activities, including Linux command execution, access-control testing, and system diagnostics.

All projects were completed in a personal virtualized lab environment for learning and skill development.

## Ongoing Development

This portfolio will continue to expand with additional hands-on IT support, operating system administration, networking, and troubleshooting projects as new skills are developed.
