
apt-get install exuberant-ctags gawk git-core git-svn samba tftpd ssh subversion
apt-get install vim openssh-server


可以把定制好的ubuntu系统制作成一个安装盘，免得每次安装完以后需要apt-get install软件。


Ubuntu上面提供了一种加密目录的方式，采用的工具是ecryptfs-utils，
Linux内核提供了dm-crypt 工具来加密文件系统分区，加密后可以防止黑客将磁盘盗走后获取其中的数据。 

= 查看版本 =
- cat /etc/issue
- sudo lsb_release -a
- uname -a
- cat /proc/version
