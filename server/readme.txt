
这里面是服务端差分工具安装使用方法。
适用于LINUX 环境
二进制差量工具工具bsdiff 安装使用
wget http://www.daemonology.net/bsdiff/bsdiff-4.3.tar.gz
tar zxvf bsdiff-4.3.tar.gz
cd bsdiff-4.3
修改Makefile 在倒数第一行 第三行 加TAB
然后执行make
make 会报错，缺少zip库
执行下面命令安装(RHEL/CENTOS)
yum install bzip2-devel
编译完成后，会在目录下生成2个二进制文件：
bsdiff
bspatch
这2个二进制文件可以直接使用
也可以拷贝到/usr/local/sbin/下
cp bsdiff /usr/local/sbin/
cp bspatch /usr/local/sbin/
# bsdiff -h
bsdiff: usage: bsdiff oldfile newfile patchfile
注：./bsdiff oldfile newfile patchfile
# bspatch -h
bspatch: usage: bspatch oldfile newfile patchfile
注：./bspatch oldfile newfile patchfile
备注：bsdiff 生成差分包     bspatch合并差分包
