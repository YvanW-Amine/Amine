cd aliyunpan-v0.2.6-linux-amd64
./aliyunpan login
59bc649b0f8a4338ad19b3ebbb10959e
upload  /影视

zip -r x.zip x
unzip aliyunpan-v0.2.6-linux-amd64.zip
1、把/home目录下面的mydata目录压缩为mydata.zip
cd /home    #进入/home目录
zip -r mydata.zip mydata    #压缩mydata目录
2、把/home目录下面的mydata.zip解压到mydatabak目录里面
unzip mydata.zip -d mydatabak
3、把/home目录下面的abc文件夹和123.txt压缩成为abc123.zip
zip -r abc123.zip abc 123.txt
4、把/home目录下面的wwwroot.zip直接解压到/home目录里面
nzip wwwroot.zip
5、把/home目录下面的abc12.zip、abc23.zip、abc34.zip同时解压到/home目录里面
unzip abc\*.zip
6、查看把/home目录下面的wwwroot.zip里面的内容
unzip -v wwwroot.zip
7、验证/home目录下面的wwwroot.zip是否完整
unzip -t wwwroot.zip
8、把/home目录下面wwwroot.zip里面的所有文件解压到第一级目录
unzip -j wwwroot.zip

aria2c
首先尝试update命令
sudo apt-get update
安装命令:
sudo apt install aria2
下载命令
rtorrent 1.torrent

1、直链下载
下载直链文件，只需在命令后附加地址，如：
aria2c http://xx.com/xx
如果需要重命名为yy的话加上--out或者-o参数，如：
aria2c --out=yy http://xx.com/xx
ria2c -o yy http://xx.com/xx
使用aria2的分段和多线程下载功能可以加快文件的下载速度，对于下载大文件时特别有用。-x 分段下载，-s 多线程下载，如：
aria2c -s 2 -x 2 http://xx.com/xx
这将使用2个连接和2个线程来下载该文件。
2、BT下载
种子和磁力下载：aria2c ‘xxx.torrnet‘
aria2c '磁力链接'
列出种子内容：
aria2c -S 1.torrent
下载种子内编号为1、4、5、6、7的文件，如：
aria2c --select-file=211-250 1.torrent --seed-time=0
设置bt端口：aria2c --listen-port=3653 ‘1.torrent’
3、限速下载
单个文件最大下载速度：
aria2c --max-download-limit=300K -s10 -x10 'http://xx.com/xx'
整体下载最大速度：
aria2c --max-overall-download-limit=300k -s10 -x10 'http://xx.com/xx'

使用 删除不再使用的包。
sudo apt autoremove
使用 清理 apt 缓存。
sudo apt clean
查看代码空间中最大的 10 个文件。
sudo find / -printf '%s %p\n'| sort -nr | head -10
使用 删除未使用的 Docker 映像、网络和容器（如果要删除所有映像，以及要删除所有卷，请追加）。
docker system prune-a--volumes
从工作树中删除未跟踪的文件：。
git clean -i
