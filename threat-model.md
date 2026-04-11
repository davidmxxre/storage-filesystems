# Threat Model

## Risks

- Disk exhaustion (Denial of service)
- Log flooding
- Misconfigured mounts causing boot failure
- SeLinux mislabeling

## Mitigations

- XFS quotas
- Separate /var/log filesystem
- UUID-based mounts
- SELinux context restoration
- Validation before reboot
