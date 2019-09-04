# FBCTF汉化版
FBCTF 简中汉化，基于Facebook官方FBCTF平台源码（Ubuntu 16.04）进行汉化


# 截图
![](https://i.imgur.com/YNv6tcQ.png)

![](https://i.imgur.com/ucigXw8.png)

![](https://i.imgur.com/sJdZXxr.png)

![](https://i.imgur.com/Hhj3DLS.png)

![](https://i.imgur.com/7pk3Gw6.png)

![](https://i.imgur.com/snKJ2Bb.png)

![](https://i.imgur.com/NEpdT3b.png)


# 使用说明
**按照以下**文件地址进行**替换**

| 文件名 | 文件位置 | 
| ------ | ------ |
| _gameboard.scss | /path/to/fbctf/src/static/css/scss |
| fb-ctf.css | /path/to/fbctf/src/static/css |
| AdminController.php| /var/www/fbctf/src/controllers |
| IndexController.php | /var/www/fbctf/src/controllers |
|Custombranding.php | /var/www/fbctf/src/xhp |
| lang_zh-cn.php | /var/www/fbctf/src/language |

其中`lang_zh-cn.php`为新增文件，使用简中时需要删除原有的`lang_zh-tw.php`

# 缓存更新

替换完成后在`shell`中更新缓存【重新编译】
```shell
rm /var/cache/hhvm/hhvm.hhbc
hhvm-repo-mode enable "/var/www/fbctf"
chown www-data:www-data /var/cache/hhvm/hhvm.hhbc
service hhvm start
service nginx restart
```

# 完整虚拟机

1. 虚拟机文件为ESXi6.5导出
2. 使用时需要重新设置虚拟机的IP地址
3. 虚拟机为Ubuntu Desktop 16.04

完整虚拟机下载地址【Ubuntu 16.04】
https://cloud.0x20h.com
