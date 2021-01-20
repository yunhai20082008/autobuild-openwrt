# 源码用于创建自动编译的精简openwrt

源码来自于lean的openwrt，eSirPlayground的自动编译脚本，tuanqing的n1工具，lisaac的dockerman

## 注意事项：

1. 主分支只用于对源码进行说明
2. 分支push后会自动触发对应分支的自动编译
3. x86为精简固件，集成了dockerman、iperf3、tcpdump以及其他一些常用luci-app，删除了无线相关的一些包，内部存储可能只有18M左右了
4. n1集成了dockerman、iperf3、tcpdump、写入emmc工具以及其他一些常用luci-app，固件直接写入u盘即可引导

    **写入方法**：

        - 使用Etcher写入u盘
        - 启动后执行 n1-install 即可安装到 emmc
        - 将固件上传到 /tmp/upgrade( xxx.img )，之后执行 n1-update 即可从该固件升级
5. n1在lean的编译为256M的rootfs，无论改多大，生成的gz似乎都只有80多M，然后用mknop的工具生成的固件rootfs最小只能是默认的512
6. n1分支默认上传的固件是tar.gz的，ext4，应该是没有引导的，包小适合小水管下载后自己在ubuntu下生成n1专用固件，另一个是自动生成的专用固件，直接写入u盘
7. 如果想支持其他固件，自己修改yml中build n1 firmware中./gen_openwrt 之后的参数
