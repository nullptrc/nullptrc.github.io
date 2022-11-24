---
layout: post
title:  "Kernel pitfalls"
date:   2022-11-24 18:55:00 +0800
categories: pitfalls linux kernel
---

## Linux Kernel pitfalls

## Build related

编译内核用的脚本./scripts/mk_p_builtin.sh
我用的是之前的./scripts/mk_p_gx32.sh编的.

所以kernel panic导致的重启,这和load时, 
 usb start;fatload usb 0 0x1080000 Image;
fatload usb 0 0x20000000 rootfs.cpio.uboot_64;
fatload usb 0 0x30000000 t3_t982_ar301.dtb
booti 0x1080000 0x20000000 0x30000000
启动地址设置有关系(Image大小不一样)
因为:
(./scripts/mk_p_gx32.sh编的Image) 28457KB
(./scripts/mk_p_builtin.sh编的Image) 20269KB