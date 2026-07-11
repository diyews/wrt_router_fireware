# wrt_router_fireware
- AX3600
f5b523bc

- AX6 9c653e74

## telnet 恢复ssh
```
sed -i 's/channel=.*/channel="debug"/g' /etc/init.d/dropbear
/etc/init.d/dropbear start
```

## 切换分区
手动在末尾添加目标分区：0 = /mtd12, 1 = /mtd13
```
nvram set flag_last_success=
nvram set flag_boot_rootfs=
nvram commit
reboot
```
