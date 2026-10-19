# Ubuntu Server Virtual Machine Setup

## Project Overview

Created and configured an Ubuntu Server ARM64 virtual machine using UTM on an Apple Silicon Mac to establish an isolated environment for practicing Linux administration, networking, and IT troubleshooting.

This virtual machine serves as the foundation for subsequent hands-on IT home lab projects.

## Lab Environment

| Component | Configuration |
|---|---|
| Host Computer | Apple Silicon Mac (M3) |
| Virtualization Software | UTM |
| Guest Operating System | Ubuntu Server ARM64 |
| Virtual CPU | 2 cores |
| Allocated Memory | 2 GB RAM |
| Virtual Disk | 20 GB |
| Networking | NAT (Network Address Translation) |
| Hostname | `ubuntu-lab01` |
| Administrative Account | `labadmin` |

## Implementation

1. Created a virtual machine in UTM configured for Ubuntu Server ARM64.
2. Allocated virtual CPU, memory, and disk resources.
3. Installed Ubuntu Server and created an administrative user account.
4. Configured networking through UTM's virtual network.
5. Logged into Ubuntu Server and accessed the Linux command-line interface.
6. Verified system resources, storage availability, and network connectivity.

## Verification and Testing

Used Linux commands to inspect and verify the virtual machine environment:

| Command | Purpose |
|---|---|
| `hostname` | Verify the virtual machine hostname |
| `free -h` | Inspect available and allocated memory |
| `df -h /` | Verify root filesystem capacity and usage |
| `ip a` | Inspect network interfaces and IP addressing |
| `ping -c 4 8.8.8.8` | Test network connectivity |

The Ubuntu Server environment was successfully configured and used for subsequent user administration and troubleshooting labs.

## Screenshots

Selected evidence from the setup process is available in the [screenshots folder](screenshots/).

Screenshots document UTM virtual hardware configuration, VM settings, and Ubuntu Server system verification.

## Skills Demonstrated

- Virtual machine creation and configuration
- Ubuntu Server installation
- ARM64 virtualization
- Linux command-line navigation
- System resource verification
- Basic virtual networking
- Technical documentation

## Outcome

Successfully established a functioning Ubuntu Server home lab environment for practicing Linux administration, user permissions, system monitoring, and network troubleshooting.
