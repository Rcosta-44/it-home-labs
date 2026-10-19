# Linux System Monitoring and Network Troubleshooting

**Status: In progress.** Evidence captured through the SSH service check; the next planned action is to check `ssh.socket`.

## Objective

Practice routine server health checks and basic troubleshooting of connectivity, DNS, services, and logs.

## Work performed

- Inspected processes using `ps aux --sort=-%cpu | head -n 10` and interactive `top`.
- Checked filesystem space with `df -h /` (about 42% used in the captured output).
- Verified internet reachability with `ping -c 4 8.8.8.8` (4 replies, 0% packet loss at time of test).
- Resolved a domain with `getent hosts google.com`.
- Checked configured DNS with `resolvectl status` and inspected an HTTPS response with `curl -I https://www.google.com` (HTTP 200 observed).
- Verified `systemd-resolved` service status and reviewed recent logs using `journalctl`.
- Checked `systemctl --failed` (0 failed units at time of check).
- Checked `systemctl status ssh --no-pager`: SSH service was installed but inactive; `ssh.socket` was shown as a trigger, so socket activation needs verification.

## Key commands

```bash
ps aux --sort=-%cpu | head -n 10
top
df -h /
ping -c 4 8.8.8.8
getent hosts google.com
resolvectl status
curl -I https://www.google.com
systemctl status systemd-resolved --no-pager
journalctl -u systemd-resolved -n 15 --no-pager
systemctl --failed
systemctl status ssh --no-pager
```

## Interpretation

The DNS service was active, domain lookup worked, and the HTTPS endpoint returned success at the time tested. No systemd units were in a failed state. An inactive `ssh.service` does not by itself prove SSH is unavailable because `ssh.socket` can activate the service on demand.

## Next step

```bash
systemctl status ssh.socket --no-pager
```

Capture the output and determine whether the SSH socket is active/listening before making configuration changes.

## Evidence

See `screenshots/` for command outputs and service status checks.
