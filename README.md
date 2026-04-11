# Storage & Filesystem Operations (RHEL 9.5)

## Overview
This lab demonstrates enterprise-grade storage management using LVM and XFS on RHEL 9.5. It simulates  real-world disk pressure scenarios, live expansion, quota enforcement and filesystem migration.

## Skills Demonstrated
- LVM creation and management
- Online logical volume expansion
- Safe filesystem reduction (ext4 only)
- XFS user and group quotas
- Persistent mounting via UUID
- Migration of /var/log to a dedicated filesystem
- Recovery and validation procedures

## Enterprise Scenario
A production system experiences disk pressure due to log growth. Storage must be expanded live, and '/va/log' migrated to prevent root filesystem exhaustion.

## Key Takeaways
- LVM (Logical Volume Manager)
- XFS filesystem
- SELinux
- systemd
