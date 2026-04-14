# Safe Filesystem Reduction (ext4 only)

lvcreate -n lv_data -L 10G vg_data
mkfs.ext4 /dev/vg_data/lv_data
mkdir /data
mount /dev/vg_data/lv_data /data

umount /data
e2fsck -f /dev/vg_data/lv_data
resize2fs /dev/vg_data/lv_data 8G
lvreduce -L 8G /dev/vg_data/lv_data
mount /data
