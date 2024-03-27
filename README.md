#### 2024年1月10日开始，LEDE源码存在bug会导致编译不成功，因此本项目可能无生成固件

## 使用 Github 云端编译 Openwrt固件
本项目用于编译打包 `电犀牛 r68s` 使用的 `openwrt` 固件。(公开仓库不占用Actions分钟数限制）

## 说明
- 刷机方法：将下载的文件解压后，得到img格式文件，在使用原厂或者其他同类系统的情况下，通过网页或者ssh将固件上传至 /tmp 目录下，然后通过dd写入磁盘。在写入完成后几秒钟后立即断电，重启后就是新系统
  例如 dd if=/tmp/f.img of=/dev/mmcblk0
- 升级固件：可以直接通过网页管理界面的 `系统` -> `备份/升级` -> `刷写新的固件` 将下载的img.gz文件上传后，按照提示升级。也可以通过scp上传固件到设备的/tmp下，在ssh中运行sysupgrade 固件名称，升级固件。
- 登录信息：默认网关地址：192.168.1.1 用户名 root 密码 password
- 备注：内含passwall组件，已测试IPv6代理不存在任何问题（若需要全局代理IPv6流量，除了应将网页中对应选项勾选，且设置支持的服务器节点外，还应将路由器自身代理设置为无）

## 引用
- 固件编译方法来自于 [P3TERX](https://p3terx.com) 的 [Actions-OpenWrt](https://github.com/P3TERX/Actions-OpenWrt) 项目。
- 固件源代码来源于 [LEDE](https://github.com/coolsnowwolf/lede) 项目。

## 如何下载
- 前往release页面，找到所需对应日期的版本
- 在assests中，找到squashfs efi img.gz字样的文件
- 单击即可下载

####  [点击这里前往版本页面](https://github.com/mdaylight/actions-openwrt-fastrhino-r68s/releases)
