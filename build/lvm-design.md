# LVM Design

## Commands

pvcreate /dev/sdb
vgcreate vg_data /dev/sdb

lvcreate -n lv_app -L 10G vg_data
lvcreate -n lv_var_log -L 20G vg_data

## Rationale

- Flexibility for resizing
- Separation of workloads
- Supports snapshots and scaling
