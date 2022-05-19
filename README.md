# RHEL9.0-and-baidunetdisk4.3
RHEL9.0 and baidunetdisk4.3
RHEL9.0安装百度网盘4.3后无法启动
dnf install baidunetdisk-4.3.0.x86_64.rpm
安装更新版补丁文件：
http://fulongx.com/repo/baidunetdisk/
dnf install baidunetdisk-patch-1.0.1-1.x86_64.rpm

运行：
'/opt/baidunetdisk/baidunetdisk'
/opt/baidunetdisk/baidunetdisk: error while loading shared libraries: libcloudproviders.so.0: cannot open shared object file: No such file or directory


下载缺少文件
https://altlinux.pkgs.org/p10/classic-x86_64/libcloudproviders-0.3.1-alt1.x86_64.rpm.html
复制文件
cp -r '/home/xude/Downloads/libcloudproviders-0.3.1/usr/lib64/libcloudproviders.so.0' '/home/xude/Downloads/libcloudproviders-0.3.1/usr/lib64/libcloudproviders.so.0.3.1' '/opt/baidunetdisk'
再运行
# '/opt/baidunetdisk/baidunetdisk'
# '/opt/baidunetdisk/baidunetdisk' /opt/baidunetdisk/baidunetdisk: symbol lookup error: /opt/baidunetdisk/libgtk-3.so.0: undefined symbol: gdk_broadway_window_get_type
RHEL9还是无法运行百度网盘4.3。
