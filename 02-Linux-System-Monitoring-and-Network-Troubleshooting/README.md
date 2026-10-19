# Linux System Monitoring and Network Troubleshooting

## Project Overview

**Status:** Completed

Performed system health checks and network troubleshooting exercises on an Ubuntu Server virtual machine.

This project demonstrates foundational IT support skills, including monitoring system resources, testing network connectivity, verifying DNS resolution, investigating system services, and interpreting diagnostic results.

## Lab Environment

- **Operating System:** Ubuntu Server ARM64
- **Virtualization:** UTM on an Apple Silicon Mac
- **Hostname:** `ubuntu-lab01`
- **Interface:** Linux command-line terminal
- **Networking:** UTM virtual NAT network

## Objectives

1. Monitor CPU, memory, and disk utilization.
2. Verify network connectivity and DNS resolution.
3. Test communication with an external HTTPS service.
4. Check the status of Linux system services.
5. Review system logs and investigate potential service issues.

## Implementation and Testing

### 1. System Resource Monitoring

Inspected active processes and system resource usage using Linux command-line tools.

**Commands practiced:**

```bash
ps aux --sort=-%cpu | head -n 10
top
free -h
df -h /
```

**Results:**
- Viewed running processes and CPU utilization.
- Inspected system memory and swap usage.
- Confirmed that the root filesystem was approximately 42% utilized at the time of testing.

### 2. Network Connectivity Testing

Tested connectivity to an external IP address.

```bash
ping -c 4 8.8.8.8
```

**Result:** Received four successful replies with 0% packet loss.

This confirmed IP connectivity from the virtual machine at the time of testing.

### 3. DNS and HTTPS Verification

Used Linux networking tools to investigate hostname resolution and external web connectivity.

```bash
getent hosts google.com
resolvectl status
curl -I https://www.google.com
```

**Results:**
- Successfully resolved a domain name.
- Inspected the configured DNS resolver.
- Received an HTTP 200 response from the HTTPS endpoint.

These tests helped distinguish IP connectivity, DNS resolution, and application-level connectivity.

### 4. Linux Service Monitoring

Checked the status of Ubuntu's DNS resolution service.

```bash
systemctl status systemd-resolved --no-pager
```

**Result:** The service was active and running.

Reviewed recent service logs:

```bash
journalctl -u systemd-resolved -n 15 --no-pager
```

The logs showed normal service activity, including stop and start events associated with a virtual machine restart.

### 5. Failed Service Checks

Checked whether systemd reported any failed units.

```bash
systemctl --failed
```

**Result:** No failed units were reported at the time of testing.

### 6. SSH Service Investigation

Inspected the SSH service:

```bash
systemctl status ssh --no-pager
```

**Observation:** The SSH service appeared inactive, but its status referenced `ssh.socket` as a possible activation trigger.

**Interpretation:** An inactive SSH service does not necessarily indicate a failure because systemd can activate certain services on demand through socket activation.

Further verification of `ssh.socket` would be required to confirm its listening state and activation behavior.

## Troubleshooting Summary

| Check | Observation | Interpretation |
|---|---|---|
| CPU and process monitoring | Process information displayed successfully | System activity could be inspected |
| Disk utilization | Approximately 42% used | Available filesystem capacity remained |
| Network connectivity | 4 successful ping replies, 0% packet loss | IP connectivity was functioning |
| DNS resolution | Domain resolved successfully | Hostname resolution was functioning |
| HTTPS connectivity | HTTP 200 response | External HTTPS endpoint responded successfully |
| DNS service | Active and running | DNS resolution service was operational |
| Failed systemd units | 0 failed units | No failed units reported |
| SSH service | Inactive with socket activation referenced | Additional socket verification recommended |

## Screenshots

Supporting evidence is available in the [screenshots folder](screenshots/).

The screenshots document process monitoring, disk utilization, network connectivity, DNS testing, systemd service checks, and SSH service investigation.

## Skills Demonstrated

- Linux system administration
- CPU, memory, and disk monitoring
- Network connectivity testing
- DNS troubleshooting
- HTTP and HTTPS diagnostics
- systemd service monitoring
- Log analysis using `journalctl`
- SSH service investigation
- Interpreting command-line diagnostic results

## Outcome

Successfully performed a series of Linux system health checks and network diagnostic tests.

Verified that network connectivity, DNS resolution, and HTTPS communication were functioning during testing. Confirmed that the DNS service was running and no failed systemd units were reported.

Investigated SSH service behavior and identified socket activation as a possible explanation for the inactive service status, with further verification identified as a future troubleshooting exercise.

This project demonstrates a structured approach to **system monitoring, troubleshooting, interpreting diagnostic information, and documenting results**.
