# Linux User Management and Permissions

**Status:** Completed lab.

## Objective

Simulate a small IT department's access controls by creating users, managing Linux groups, and allowing only authorized employees into a shared directory.

## Environment

Ubuntu Server ARM64 virtual machine running in UTM.

## Actions performed

1. Created test accounts `employee1` and `employee2` and an `itdepartment` group.
2. Added `employee1` to `itdepartment` and verified group membership with `id` and `groups`.
3. Created a restricted directory, assigned the `itdepartment` group with `chgrp`, and set mode `770` with `chmod`.
4. Investigated why the group member could not enter a directory located inside `/home/labadmin`: the parent home directory prevented traversal.
5. Moved the shared directory to `/srv/it-files`, preserving its group and permission settings.
6. Verified that `employee1` could enter the directory and create a test file while `employee2` initially received `Permission denied`.
7. Temporarily added `employee2` to the group, verified access in a new session, then removed group membership and confirmed access was denied again.
8. Recorded a local text report at `~/lab-reports/linux-user-permissions.txt` in the Ubuntu VM.

## Commands used

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

## Troubleshooting and learning

File access depends on permissions on **every parent directory**. Moving the shared folder outside the administrator's private home directory resolved the traversal problem. Group membership changes should be tested in a **new login session**. Permission `770` gives owner and group read/write/execute permissions and no access to others.

## Outcome

Demonstrated controlled access, access provisioning, access revocation, and verification using separate test users.

## Evidence

See `screenshots/`. The curated screenshots focus on user/group setup, permission settings, troubleshooting, access granted/denied, and group access changes. The report's **content is reconstructed here from screenshots**; the original `.txt` file remains inside the user's Ubuntu VM unless separately exported.
