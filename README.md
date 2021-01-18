# 源码用于创建自动编译的精简的openwrt
源码来自于lean的openwrt，eSirPlayground的自动编译脚本，tuanqing的n1工具，lisaac的dockerman

主分支只用于对源码进行说明，分支push后会自动触发对应分支的自动编译

x86为精简自lean的源码编译的x86固件，集成了dockerman已经其他一些常用luci-app，删除了无线相关的一些包，含有iperf3 tcpdump

n1为精简自lean的源码编译的n1固件，并将写入emmc的包进行了集成
使用[Etcher](https://www.balena.io/etcher/)写入u盘
启动后执行 n1-install 即可安装到 emmc
将固件上传到 /tmp/upgrade( xxx.img )，之后执行 n1-update 即可从该固件升级
集成了dockerman已经其他一些常用luci-app，删除了无线相关>的一些包，含有iperf3 tcpdump
