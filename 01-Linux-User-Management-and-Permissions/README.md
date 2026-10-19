# Linux User Management and Permissions

## Project Overview

**Status:** Completed

Configured and tested Linux user accounts, group memberships, and directory permissions in an Ubuntu Server home lab. Simulated a small IT department where authorized employees require access to shared files while unauthorized users must be restricted.

This project demonstrates user administration, access control, permission troubleshooting, and verification of security settings.

## Lab Environment

- **Operating System:** Ubuntu Server ARM64
- **Virtualization:** UTM on an Apple Silicon Mac
- **Administrative Account:** `labadmin`
- **Test Accounts:** `employee1`, `employee2`
- **Security Group:** `itdepartment`
- **Shared Directory:** `/srv/it-files`

## Objectives

1. Create and manage Linux user accounts and groups.
2. Configure shared directory ownership and permissions.
3. Restrict access to authorized group members.
4. Investigate and resolve permission-related errors.
5. Test granting and revoking user access.

## Implementation

### 1. User and Group Configuration

Created two test user accounts and an IT department group.

Added `employee1` to `itdepartment` and verified group membership using Linux commands.

### 2. Directory Permissions

Created a shared directory, assigned group ownership to `itdepartment`, and configured permissions using `chmod 770`.

These permissions allow the directory owner and group members to read, write, and access the directory while denying access to other users.

### 3. Troubleshooting a Permission-Denied Error

**Problem:** Despite belonging to the authorized group, `employee1` could not access the shared directory.

**Investigation:** Determined that the directory was located inside `/home/labadmin`, where the parent directory's restrictive permissions prevented other users from traversing the path.

**Resolution:** Moved the shared directory to `/srv/it-files` while retaining the required group ownership and permissions.

**Verification:** Confirmed that `employee1` could enter the directory and create a test file.

### 4. Access Control Testing

Tested access using `employee2`, who was initially not a member of `itdepartment`.

- Confirmed that the unauthorized account received a permission-denied error.
- Added `employee2` to the authorized group.
- Started a new login session and verified access was granted.
- Removed `employee2` from the group.
- Verified that access was denied again in a new session.

## Commands Practiced

```bash
sudo adduser employee2
sudo usermod -aG itdepartment employee1
id employee1

sudo chgrp itdepartment /srv/it-files
sudo chmod 770 /srv/it-files
ls -ld /srv/it-files

sudo -iu employee1
cd /srv/it-files
touch employee1-report.txt
exit

sudo usermod -aG itdepartment employee2
sudo gpasswd -d employee2 itdepartment
```

These commands represent key activities performed during the lab.

## Troubleshooting Results

| Issue or Test | Result |
|---|---|
| Authorized user initially unable to access shared directory | Identified restrictive parent directory permissions |
| Shared directory moved to `/srv/it-files` | Authorized user successfully accessed the directory |
| Unauthorized user attempted access | Permission denied |
| Unauthorized user added to group | Access granted after starting a new session |
| Group membership revoked | Access denied again after starting a new session |

## Screenshots

Supporting evidence is available in the [screenshots folder](screenshots/).

The screenshots document user and group configuration, directory permissions, troubleshooting, authorized and unauthorized access testing, and group membership changes.

## Skills Demonstrated

- Linux user account administration
- Group membership management
- File and directory permissions
- `chmod`, `chgrp`, `usermod`, and `gpasswd`
- Least-privilege access controls
- Troubleshooting permission-denied errors
- Verifying access changes through user testing
- Technical documentation

## Outcome

Successfully configured a shared directory with restricted access, resolved a parent-directory permission issue, and verified that access could be granted and revoked through Linux group membership.

The project demonstrates a structured troubleshooting process: **identify the problem, investigate the cause, implement a solution, and verify the result.**
