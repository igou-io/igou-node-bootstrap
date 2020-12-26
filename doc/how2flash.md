```
[igou@igou]$ sudo flash -d /dev/sdd -u ../cloud-init/k3s/worker-4.yaml ubuntu-20.04.1-preinstalled-server-arm64+raspi.img
Is /dev/sdd correct? yes
Unmounting /dev/sdd ...
Flashing ubuntu-20.04.1-preinstalled-server-arm64+raspi.img to /dev/sdd ...
2.85GiB 0:01:35 [30.3MiB/s] [====================================================================================================================================>         ] 94% ETA 0:00:06
0+49604 records in
0+49604 records out
3250824192 bytes (3.3 GB, 3.0 GiB) copied, 131.593 s, 24.7 MB/s
Waiting for device /dev/sdd

/dev/sdd:
 re-reading partition table
Mounting Disk
Mounting /dev/sdd to customize...
total 60159
drwxr-xr-x. 3 root root     2560 Dec 31  1969 .
drwxr-xr-x. 3 root root       60 Dec 12 17:48 ..
-rwxr-xr-x. 1 root root    26516 Jul 31 12:48 bcm2710-rpi-2-b.dtb
-rwxr-xr-x. 1 root root    27557 Jul 31 12:48 bcm2710-rpi-3-b.dtb
-rwxr-xr-x. 1 root root    28176 Jul 31 12:48 bcm2710-rpi-3-b-plus.dtb
-rwxr-xr-x. 1 root root    26371 Jul 31 12:48 bcm2710-rpi-cm3.dtb
-rwxr-xr-x. 1 root root    46612 Jul 31 12:48 bcm2711-rpi-4-b.dtb
-rwxr-xr-x. 1 root root    19924 Jul 31 12:48 bcm2837-rpi-3-a-plus.dtb
-rwxr-xr-x. 1 root root    20373 Jul 31 12:48 bcm2837-rpi-3-b.dtb
-rwxr-xr-x. 1 root root    20793 Jul 31 12:48 bcm2837-rpi-3-b-plus.dtb
-rwxr-xr-x. 1 root root    19700 Jul 31 12:48 bcm2837-rpi-cm3-io3.dtb
-rwxr-xr-x. 1 root root    52480 Jul 31 12:48 bootcode.bin
-rwxr-xr-x. 1 root root     2569 Jul 31 12:48 boot.scr
-rwxr-xr-x. 1 root root      141 Jul 31 12:48 cmdline.txt
-rwxr-xr-x. 1 root root     1117 Jul 31 12:48 config.txt
-rwxr-xr-x. 1 root root     3146 Jul 31 12:48 fixup4cd.dat
-rwxr-xr-x. 1 root root     5405 Jul 31 12:48 fixup4.dat
-rwxr-xr-x. 1 root root     8417 Jul 31 12:48 fixup4db.dat
-rwxr-xr-x. 1 root root     8419 Jul 31 12:48 fixup4x.dat
-rwxr-xr-x. 1 root root     3146 Jul 31 12:48 fixup_cd.dat
-rwxr-xr-x. 1 root root     7276 Jul 31 12:48 fixup.dat
-rwxr-xr-x. 1 root root    10265 Jul 31 12:48 fixup_db.dat
-rwxr-xr-x. 1 root root    10265 Jul 31 12:48 fixup_x.dat
-rwxr-xr-x. 1 root root 29530201 Jul 31 12:48 initrd.img
-rwxr-xr-x. 1 root root      240 Jul 31 12:48 meta-data
-rwxr-xr-x. 1 root root      770 Jul 31 12:48 network-config
-rwxr-xr-x. 1 root root     1371 Jul 31 12:48 overlay_map.dtb
drwxr-xr-x. 2 root root    16384 Jul 31 12:48 overlays
-rwxr-xr-x. 1 root root     1514 Jul 31 12:48 README
-rwxr-xr-x. 1 root root   816124 Jul 31 12:48 start4cd.elf
-rwxr-xr-x. 1 root root  3774532 Jul 31 12:48 start4db.elf
-rwxr-xr-x. 1 root root  2272992 Jul 31 12:48 start4.elf
-rwxr-xr-x. 1 root root  3031652 Jul 31 12:48 start4x.elf
-rwxr-xr-x. 1 root root   816124 Jul 31 12:48 start_cd.elf
-rwxr-xr-x. 1 root root  4846308 Jul 31 12:48 start_db.elf
-rwxr-xr-x. 1 root root  2997088 Jul 31 12:48 start.elf
-rwxr-xr-x. 1 root root  3755236 Jul 31 12:48 start_x.elf
-rwxr-xr-x. 1 root root      327 Jul 31 12:48 syscfg.txt
-rwxr-xr-x. 1 root root   493528 Jul 31 12:48 uboot_rpi_3.bin
-rwxr-xr-x. 1 root root   492824 Jul 31 12:48 uboot_rpi_4.bin
-rwxr-xr-x. 1 root root      200 Jul 31 12:48 usercfg.txt
-rwxr-xr-x. 1 root root     2114 Jul 31 12:48 user-data
-rwxr-xr-x. 1 root root  8390521 Jul 31 12:48 vmlinuz
Copying cloud-init ../cloud-init/k3s/worker-4.yaml to /tmp/0/mnt.694170/user-data ...
Unmounting /dev/sdd ...
Finished.
```

Append `cgroup_enable=cpuset cgroup_enable=memory cgroup_memory=1` to `/boot/firmware/cmdline.txt` if needed
