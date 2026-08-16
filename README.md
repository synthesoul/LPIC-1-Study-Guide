# LPIC-1 Study Guide

This guide is a practical roadmap for preparing for **LPIC-1 (Linux Administrator)**, covering exam objectives for both:
- **101-500**
- **102-500**

Use this as a checklist and quick-reference while studying.

---

## 1) LPIC-1 Exam Overview

LPIC-1 validates junior Linux administration skills, including:
- Command-line usage
- Linux installation and package management
- GNU/Unix tools
- Filesystems and storage
- Shell scripting basics
- Administrative tasks
- Networking fundamentals
- Security basics

### Recommended prep approach
1. Study one objective block at a time.
2. Practice every command in a live Linux VM.
3. Build summary notes and flashcards.
4. Take timed practice tests weekly.

---

## 2) 101-500 Study Guide

## 101.1 Determine and configure hardware settings
- Identify hardware: `lspci`, `lsusb`, `lshw`, `dmidecode`
- Kernel modules: `lsmod`, `modprobe`, `/etc/modprobe.d/`
- Device files and udev basics

Practice:
- Find NIC, disk, and USB details.
- Load/unload a module and verify with `lsmod`.

## 101.2 Boot the system
- BIOS vs UEFI basics
- Boot process stages: firmware → bootloader → kernel → init/systemd
- Bootloader concepts (GRUB2)
- Troubleshooting boot issues

Practice:
- Inspect GRUB config files.
- Boot into rescue/single-user mode.

## 101.3 Change runlevels / boot targets and shutdown
- systemd targets and legacy runlevels mapping
- `systemctl isolate`, `systemctl get-default`, `systemctl set-default`
- Shutdown/reboot: `shutdown`, `reboot`, `poweroff`

Practice:
- Switch between multi-user and graphical targets.
- Schedule delayed shutdown and cancel it.

## 102.1 Design hard disk layout
- Partitions (MBR vs GPT)
- Mount points and Linux directory planning
- Swap planning

Practice:
- Plan a partition table for a server workload.

## 102.2 Install a boot manager
- GRUB2 install/update basics
- Kernel parameters at boot
- GRUB defaults and recovery entries

Practice:
- Change GRUB timeout/default entry.
- Rebuild GRUB config.

## 102.3 Manage shared libraries
- Library paths and dynamic linker basics
- `ldd`, `ldconfig`, `/etc/ld.so.conf`, `LD_LIBRARY_PATH`

Practice:
- Trace binary library dependencies with `ldd`.

## 102.4 Use Debian package management
- `dpkg`, `apt`, package queries
- Install/remove/upgrade packages
- Repository configuration basics

Practice:
- Install a package, inspect its files, and remove it cleanly.

## 102.5 Use RPM and YUM/DNF package management
- `rpm`, `yum`/`dnf` operations
- Query package ownership and metadata

Practice:
- Find which package owns a file.
- Install local RPM and verify dependencies.

## 103.1 Work on the command line
- Shell types and command syntax
- Variables, quoting, escaping
- Command history and completion

Practice:
- Write one-liners using pipes and redirection.

## 103.2 Process text streams using filters
- Core tools: `cat`, `grep`, `sed`, `awk`, `sort`, `uniq`, `cut`, `tr`, `wc`, `tee`
- Regex fundamentals

Practice:
- Parse logs and produce filtered reports.

## 103.3 Perform basic file management
- `cp`, `mv`, `rm`, `mkdir`, `rmdir`, `find`, `locate`
- Links: hard vs symbolic
- Globbing and path handling

Practice:
- Create symbolic and hard links and explain differences.

## 103.4 Use streams, pipes, and redirects
- `>`, `>>`, `<`, `2>`, `2>>`, `2>&1`, pipelines
- Here-documents basics

Practice:
- Combine stdout/stderr into a log file.

## 103.5 Create, monitor, and kill processes
- Process states and IDs
- `ps`, `top`, `htop`, `pgrep`, `pkill`, `kill`, `killall`, `nice`, `renice`
- Job control: `&`, `jobs`, `fg`, `bg`

Practice:
- Start background jobs and manage priority.

## 103.6 Modify process execution priorities
- Niceness values and scheduler basics

Practice:
- Compare process priority before/after `renice`.

## 103.7 Search text files using regular expressions
- Basic and extended regex
- `grep -E`, anchors, character classes, quantifiers

Practice:
- Build regex to match valid IPv4 and email-like patterns.

## 103.8 Perform basic file editing with vi
- Modes, navigation, search/replace, save/quit

Practice:
- Edit a config file and perform substitutions in `vi`.

## 104.1 Create partitions and filesystems
- `fdisk`, `gdisk`, `parted`
- Filesystems: ext4, xfs, vfat basics
- `mkfs`, `blkid`

Practice:
- Partition a test disk and create filesystems.

## 104.2 Maintain integrity of filesystems
- `fsck` usage and caution
- Tune/check tools (`tune2fs`, `xfs_repair` basics)

Practice:
- Simulate fsck checks on unmounted filesystem images.

## 104.3 Control mounting and unmounting of filesystems
- `mount`, `umount`, `/etc/fstab`
- Mount options and persistent mounts

Practice:
- Add an `/etc/fstab` entry and validate with `mount -a`.

## 104.4 Manage disk quotas
- User/group quotas
- `quota`, `edquota`, `repquota`, `quotacheck`

Practice:
- Configure quota limits for a test user.

## 104.5 Manage file permissions and ownership
- `chmod`, `chown`, `chgrp`, umask
- SUID, SGID, sticky bit

Practice:
- Secure a shared directory using sticky bit.

## 104.6 Create and change hard and symbolic links
- Link mechanics and limitations

Practice:
- Demonstrate inode sharing with hard links.

## 104.7 Find system files and place files in the correct location
- FHS (Filesystem Hierarchy Standard) overview
- Typical paths (`/etc`, `/var`, `/usr`, `/opt`, `/home`, `/tmp`)

Practice:
- Classify common files by proper FHS location.

---

## 3) 102-500 Study Guide

## 105.1 Customize and use the shell environment
- Profile files: `/etc/profile`, `~/.bash_profile`, `~/.bashrc`
- Aliases and functions
- Environment variables

Practice:
- Build a custom prompt and persistent aliases.

## 105.2 Customize or write simple scripts
- Script structure and shebang
- Positional parameters, exit codes, conditionals, loops
- Basic automation tasks

Practice:
- Write a backup rotation script with logs.

## 105.3 SQL data management
- SQL basics: `SELECT`, `INSERT`, `UPDATE`, `DELETE`
- CLI database interactions (conceptual for LPIC-1 scope)

Practice:
- Query and filter a simple test table.

## 106.1 Install and configure X11
- X11 architecture basics
- Display manager/window manager concepts

Practice:
- Identify display server and troubleshoot basic startup issues.

## 106.2 Setup a display manager
- Display manager configuration basics (GDM/LightDM/SDDM concepts)

Practice:
- Change default display manager.

## 106.3 Accessibility
- Basic accessibility settings in Linux desktops

Practice:
- Enable keyboard and visual accessibility options.

## 107.1 Manage user and group accounts and related system files
- `useradd`, `usermod`, `userdel`, `groupadd`, `groupmod`, `groupdel`, `passwd`
- `/etc/passwd`, `/etc/shadow`, `/etc/group`, `/etc/gshadow`

Practice:
- Create users/groups and enforce password changes.

## 107.2 Automate system administration tasks by scheduling jobs
- `cron`, `crontab`, `/etc/cron.*`, `at`, `atq`, `atrm`

Practice:
- Schedule recurring and one-time admin jobs.

## 107.3 Localization and internationalization
- Locale variables and tools: `locale`, `localectl`
- Time zones: `timedatectl`

Practice:
- Change locale and timezone for a test system.

## 108.1 Maintain system time
- NTP/chrony basics
- `timedatectl`, `chronyc`

Practice:
- Verify sync status and source.

## 108.2 System logging
- rsyslog/syslog and systemd-journald concepts
- `journalctl` filters and persistence

Practice:
- Query logs by boot, service, and time.

## 108.3 Mail Transfer Agent (MTA) basics
- Local mail handling concepts
- Aliases and queue basics

Practice:
- Send local test mail and inspect queue/logs.

## 108.4 Manage printers and printing
- CUPS basics and queue controls
- Commands: `lp`, `lpq`, `lprm`

Practice:
- Add and test a printer queue in a lab setup.

## 109.1 Fundamentals of internet protocols
- IPv4/IPv6 basics, subnetting concepts
- Common protocols: TCP, UDP, ICMP, DNS, HTTP, SSH

Practice:
- Read routing table and explain packet path basics.

## 109.2 Basic network configuration
- `ip`, `ifconfig` (legacy), `nmcli`
- Interface configuration basics

Practice:
- Configure static IP in a test VM.

## 109.3 Basic network troubleshooting
- `ping`, `traceroute`, `ss`, `netstat` (legacy), `dig`, `host`, `nslookup`

Practice:
- Diagnose DNS and connectivity issues.

## 109.4 Configure client-side DNS
- `/etc/resolv.conf`, systemd-resolved basics

Practice:
- Change resolver settings and test lookup behavior.

## 110.1 Perform security administration tasks
- Account security, password policies
- File permissions and ACL awareness
- Basic host hardening

Practice:
- Audit world-writable files and unnecessary services.

## 110.2 Setup host security
- TCP wrappers (legacy awareness), packet filtering concepts
- OpenSSH server/client hardening basics

Practice:
- Harden SSH settings and validate access.

## 110.3 Securing data with encryption
- GPG basics
- SSH key authentication basics

Practice:
- Encrypt/decrypt files with GPG and test SSH keys.

---

## 4) High-Value Command Checklist

Know these thoroughly:
- System info: `uname`, `hostnamectl`, `lsb_release`, `cat /proc/*`
- Files/processes: `find`, `grep`, `sed`, `awk`, `ps`, `kill`, `top`
- Storage: `lsblk`, `fdisk`, `parted`, `mkfs`, `mount`, `fsck`
- Accounts: `id`, `passwd`, `useradd`, `usermod`, `groups`
- Networking: `ip`, `ss`, `ping`, `dig`, `traceroute`
- Logs/services: `journalctl`, `systemctl`

---

## 5) 6-Week Study Plan (Example)

### Week 1
- Linux basics, shell usage, text tools (`103.x`)

### Week 2
- Package management and boot process (`101.x`, `102.4`, `102.5`)

### Week 3
- Disks, filesystems, mounts, permissions (`104.x`)

### Week 4
- Scripting, users/groups, scheduling (`105.x`, `107.x`)

### Week 5
- Networking and services (`108.x`, `109.x`)

### Week 6
- Security review (`110.x`) + full practice exams

---

## 6) Practice Lab Ideas

- Build 2 Linux VMs (Debian-based + RPM-based distro).
- Simulate user onboarding/offboarding.
- Break and recover bootloader in a sandbox VM snapshot.
- Configure cron backup + log rotation checks.
- Mount extra virtual disks and enforce quotas.
- Run hardening checklist and document findings.

---

## 7) Exam-Day Tips

- Read every question carefully for command syntax details.
- Eliminate clearly wrong options first.
- Watch for distro-specific package manager commands.
- Manage time: mark tough questions and return later.

Good luck with your LPIC-1 preparation.