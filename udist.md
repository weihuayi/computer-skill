# Manage USB Disk


## Linux 系统下

GUI 程序 `Disks`


命令行

```
 mkfs.vfat -n 'name_for_your_pendrive' -I /dev/sdb1
```
其中 `-n` 是命名你的 U 盘， `-I`

## 1. The volume lost problem 

在 Win 系统下

1. `win+R`
2. `diskpart` 
3. `list disk`
4. `select disk X`
5. `clean`
6. 我的电脑--> 管理 --> 磁盘管理 --> 对 U 盘重新分区 


