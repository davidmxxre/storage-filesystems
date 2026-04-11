# Architecture

## Volume Layout

- VG: vg_data
- LV:
  - lv_app -> /app
  - lv_var_log -> /var/log

## Filesystems

- XFS for all production mounts

## Mount Points

- /app -> application data
- /var/log -> logs and variable data

## Design Principles

- Separation of OS and application data
- Independent scaling of storage
- Prevention of root filesystem exhaustion
