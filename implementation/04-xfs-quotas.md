# XFS Quotas

## Enable in fstab
UUID=xxxx /app xfs defaults,uquota,gquota 0 0
mount -a
systemctl daemon-reload

## Set user quota

xfs_quota -x -c ‘limit bsoft=3G bhard=4G app_user1’ /app
xfs_quota -x -c ‘limit bsoft=2G bhard=3G app_user2’ /app

## Set group quota

## YOU ONLY NEED GROUP QUOTAS FOR SHARED DIRECTORIES ##

xfs_quota -x -c ‘limit -g bsoft=3G bhard=4G app_ops’ /app

## Verify

xfs_quota -x -c 'report -u' /app
xfs_quota -x -c 'report -g' /app
