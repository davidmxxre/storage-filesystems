# Create LVM

pvcreate /dev/sdb
vgcreate vg_app /dev/sdb

lvcreate -n lv_app -L 10G vg_data
mkfs.xfs /dev/vg_data/lv_app

mkdir /app
mount /dev/vg_data/lv_app /app
