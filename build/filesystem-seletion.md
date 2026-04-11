# Filesystem Selection

## XFS

- Default for RHEL 9.5
- Supports online grouwth
- Supports quotas

## ext4

- Used only when shrinkingis required

## Decision

- XFS for production workloads
- ext4 only for shrink demonstrations
