# OpenWRT Xiaomi Router 3G Lite Patch

小米路由器3G版的Openwrt与mirom双系统Patch

Openwrt官方的小米路由器3G版的源码中将Rootfs区直接从kernel1的区域拓展到Flash分区的末尾，虽然拓展了rootfs区，但是破坏了原有的分区格式，使小米自带的固件无法再使用，于是我对Openwrt的MiR3G部分的配置fork了一份，编译出的kernel和rootfs可以与mirom原有的kernel和rootfs共存。

需要在uboot(mirom env)中或使用ubootenv tool(openwrt env)切换双系统。


PS. 用了openwrt之后其实很少切回mirom了...

研究mirom分区内的shell script后发现上报的东西真不少,Remote还有所有Control权限.
