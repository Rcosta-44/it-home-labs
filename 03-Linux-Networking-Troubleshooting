# Lab 03 – Linux Networking and Troubleshooting

## Project Overview

This hands-on lab demonstrates foundational Linux networking, network configuration analysis, connectivity testing, DNS resolution, and routing diagnostics.

The objective was to develop a structured approach to identifying and troubleshooting network connectivity issues using native Linux command-line tools.

## Lab Environment

| Component | Configuration |
|---|---|
| Host Hardware | Apple Silicon Mac |
| Virtualization | UTM |
| Operating System | Ubuntu Server |
| Architecture | ARM64 |
| Hostname | ubuntu-lab01 |
| Network Interface | enp0s1 |
| IPv4 Address | 192.168.64.2/24 |
| Default Gateway | 192.168.64.1 |
| IP Assignment | DHCP |

## Lab Objectives

- Identify active network interfaces.
- Examine IPv4 and IPv6 configurations.
- Verify external network connectivity.
- Test DNS resolution.
- Examine the system routing table.
- Identify and verify the default gateway.
- Analyze packet loss and network latency.
- Develop a structured network troubleshooting methodology.

## Lab Procedures

### 1. Identify Network Interfaces

Command:

`ip a`

Examined available network interfaces, interface status, MAC addresses, and assigned IPv4 and IPv6 addresses.

Results:

- Identified the loopback interface.
- Confirmed that the primary network interface was active.
- Verified the dynamically assigned IPv4 address.
- Identified the configured IPv6 addresses.

### 2. Test External IP Connectivity

Command:

`ping -c 4 8.8.8.8`

Tested connectivity to a public IP address without relying on DNS resolution.

Results:

- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Average latency: 48.223 ms

Successfully verified external IP connectivity.

### 3. Test DNS Resolution

Command:

`ping -c 4 google.com`

Tested hostname resolution and external network connectivity.

Results:

- Successfully resolved the hostname to an IPv4 address.
- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Average latency: 59.685 ms

Confirmed that DNS resolution and external connectivity were functioning during testing.

### 4. Examine the Routing Table

Command:

`ip route`

Reviewed the system routing table to identify the default gateway, local network, and active network interface.

Results:

- Default gateway: 192.168.64.1
- Local network: 192.168.64.0/24
- Network interface: enp0s1
- Routing configuration supplied through DHCP.

### 5. Verify Default Gateway Connectivity

Command:

`ping -c 4 192.168.64.1`

Tested communication between the Ubuntu virtual machine and its default gateway.

Results:

- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Average latency: 0.678 ms

Successfully verified local gateway connectivity.

## Network Troubleshooting Methodology

The following diagnostic workflow can be used to isolate common network connectivity issues:

1. Verify that the network interface is active.
2. Confirm that the device has a valid IP address.
3. Verify the routing table and default gateway.
4. Test connectivity to the default gateway.
5. Test connectivity to a public IP address.
6. Test DNS resolution using a hostname.
7. Analyze packet loss and response times.
8. Document findings and verify network functionality.

This approach helps distinguish between local network configuration issues, routing problems, external connectivity failures, and DNS-related issues.

## Test Results

| Diagnostic Test | Result |
|---|---|
| Network Interface Status | Passed |
| IPv4 Configuration | Passed |
| External IP Connectivity | Passed |
| DNS Resolution | Passed |
| Routing Table Verification | Passed |
| Default Gateway Connectivity | Passed |

All connectivity tests completed successfully with 0% packet loss.

## Technical Skills Demonstrated

- Linux command-line administration
- Network interface analysis
- IPv4 and IPv6 fundamentals
- DHCP configuration analysis
- DNS troubleshooting
- ICMP connectivity testing
- Routing table analysis
- Default gateway verification
- Network latency analysis
- Structured technical troubleshooting
- Technical documentation

## Tools and Commands

| Command | Purpose |
|---|---|
| `ip a` | Display network interfaces and IP addresses |
| `ip route` | Display the system routing table |
| `ping -c 4 8.8.8.8` | Verify external IP connectivity |
| `ping -c 4 google.com` | Verify DNS resolution and connectivity |
| `ping -c 4 192.168.64.1` | Verify default gateway connectivity |

## Screenshot Documentation

Supporting screenshots are available in the [screenshots directory](screenshots/).

The screenshots document:

1. Network interface configuration
2. Public IP connectivity testing
3. DNS resolution testing
4. Routing table and default gateway identification
5. Default gateway connectivity testing

## Conclusion

Successfully verified network configuration, external connectivity, DNS resolution, routing, and default gateway communication within an Ubuntu Server virtualized environment.

This lab demonstrates practical networking and diagnostic skills applicable to IT Support, Technical Support Engineering, Systems Administration, and Cybersecurity roles.

## Project Status

Completed
