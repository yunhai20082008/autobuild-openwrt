# 源码用于创建自动编译的精简openwrt
源码来自于lean的openwrt，eSirPlayground的自动编译脚本，tuanqing的n1工具，lisaac的dockerman
## 注意事项：
1.主分支只用于对源码进行说明
2.分支push后会自动触发对应分支的自动编译
3.x86为精简固件，集成了dockerman、iperf3、tcpdump以及其他一些常用luci-app，删除了无线相关的一些包
4.n1集成了dockerman、iperf3、tcpdump、写入emmc工具以及其他一些常用luci-app，固件直接写入u盘即可引导
  **使用方法：
  使用[Etcher](https://www.balena.io/etcher/)写入u盘
  启动后执行 n1-install 即可安装到 emmc
  将固件上传到 /tmp/upgrade( xxx.img )，之后执行 n1-update 即可从该固件升级
5.
