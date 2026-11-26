
# IT Home Lab Portfolio

Hands-on IT home lab projects focused on Linux and Windows system administration, network troubleshooting, endpoint management, access controls, and system diagnostics.

This portfolio documents practical technical experience through independent lab exercises, structured troubleshooting, configuration testing, and technical documentation.

## Lab Environment

| Component | Configuration |
|---|---|
| Linux Host | Apple Silicon Mac |
| Virtualization | UTM |
| Linux Operating System | Ubuntu Server (ARM64) |
| Windows Hardware | Dell Laptop |
| Windows Operating System | Windows 11 |
| Environment | Personal IT Home Lab |

## Projects

| Project | Status | Skills Demonstrated |
|---|---|---|
| [00 - Ubuntu VM Setup](00-Ubuntu-VM-Setup/README.md) | Completed | Virtualization, Ubuntu Server installation, UTM configuration, Linux CLI |
| [01 - Linux User Management and Permissions](01-Linux-User-Management-and-Permissions/README.md) | Completed | User accounts, groups, permissions, access controls |
| [02 - Linux System Monitoring and Network Troubleshooting](02-Linux-System-Monitoring-and-Network-Troubleshooting/README.md) | Completed | CPU, memory, disk usage, systemd, logs, SSH diagnostics |
| [03 - Linux Networking and Troubleshooting](03-Linux-Networking-Troubleshooting/README.md) | Completed | IPv4, IPv6, DHCP, DNS, ICMP, routing, gateway diagnostics |
| [20 - Windows System Administration](20-Windows-System-Administration/README.md) | Completed | Endpoint management, user administration, Windows services, system diagnostics |

## Technical Skills

### Operating Systems and Virtualization
- Windows 11
- Ubuntu Server
- Linux command-line administration
- UTM virtualization
- ARM64 virtual machines

### Networking
- IPv4 and IPv6 fundamentals
- DHCP configuration analysis
- DNS resolution and troubleshooting
- ICMP connectivity testing
- Routing table analysis
- Default gateway verification
- HTTP and HTTPS connectivity testing
- Packet loss and latency analysis

### System Administration
- Linux user and group management
- Windows local account administration
- File and directory permissions
- Administrator and standard user accounts
- Windows Device Manager
- Windows Services
- Windows Update
- Microsoft Management Console (MMC)

### Security and Access Controls
- Role-based access control fundamentals
- Least privilege principles
- Linux file permissions
- Microsoft Defender
- Endpoint security fundamentals
- User access verification

### System Monitoring and Troubleshooting
- Windows Event Viewer
- Linux systemd and journal logs
- CPU and memory utilization
- Disk usage analysis
- System service diagnostics
- Network connectivity troubleshooting
- Structured problem identification and resolution

## Troubleshooting Highlights

### Linux File Permissions
Investigated an access-denied issue caused by restricted parent directory permissions. Relocated the shared directory to `/srv/it-files` and verified authorized access.

### User Access Control
Tested file access for authorized and unauthorized users, modified group membership, and confirmed that removing permissions revoked access.

### Network Connectivity and DNS
Verified network interface configuration, public IP connectivity, DNS resolution, routing tables, and default gateway communication. All ICMP connectivity tests in the dedicated networking lab completed with 0% packet loss.

### Linux System Services
Investigated systemd service status, reviewed system logs, and checked for failed services.

### Windows Endpoint Administration
Practiced workstation administration using native Windows tools, including user account configuration, system services, Device Manager, Windows Update, Microsoft Defender, and Event Viewer.

## Troubleshooting Methodology

Each lab emphasizes a structured approach to technical problem-solving:

1. Identify the issue or technical objective.
2. Gather relevant system information.
3. Investigate potential causes.
4. Implement or test an appropriate solution.
5. Verify system functionality.
6. Document procedures, findings, and results.

## Project Documentation

Each project includes a dedicated README documenting its objectives, environment, tools, procedures, and results.

Supporting screenshots are included where available to demonstrate hands-on technical activities, configuration changes, command execution, and diagnostic results.

All projects were conducted in a personal lab environment for technical learning and professional development.

## Professional Development

This portfolio supports ongoing skill development in:

- IT Support and Technical Support Engineering
- Windows and Linux System Administration
- Network Administration
- Endpoint Security
- Cybersecurity
- Cloud Infrastructure and Security

## Ongoing Development

This repository will continue to expand with additional hands-on projects covering operating system administration, networking, security, automation, and cloud technologies.

## Author

Robert Costa

[GitHub Profile](https://github.com/Rcosta-44)
