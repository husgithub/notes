### linux系统常用命令
#### 日期时间
- **date** (查看/设置系统时间)<br>
![](pic/20190913162305.png)<br>
- **hwclock/clock** (显示硬件时钟时间)<br>
![](pic/20190913162919.png)<br>
- **cal** (查看日历) <br>
![](pic/20190913163024.png)
- **uptime** (查看系统运行时间)<br>
![](pic/20190913163417.png)
#### 输出查看命令
- **echo** (显示输入的内容)<br>
![](pic/20190913163803.png)
- **cat** (显示文件内容)<br>
![](pic/20190913164543.png)
- **head** (显示文件的头几行，默认为10)<br>
![](pic/20190913164916.png)
- **tail** (显示文件末尾几行,默认10)<br>
-n 指定显示行数<br>
-f (follow) 追踪显示文件(可用于查看日志) <br>
- **more** (翻页显示文件内容,只可向下翻页)<br>
- **less** (可上下翻页文件内容)<br>
#### 关机重启
- **shutdown** (关闭/重启计算机)<br>
-h 关闭计算机<br>
-r 重启<br>
![](pic/20190913171746.png)
- **poweroff** (立即关闭计算机)<br>
- **reboot** (立即重启)<br>
![](pic/20190913171944.png)
#### 归档，压缩
- **zip** （压缩文件，需安装压缩解压工具）<br>
![](pic/20190913172925.png)<br>
- **upzip** （解压文件，需安装压缩解压工具）<br>
![](pic/20190913173212.png)
- **tar** (使用tar命令进行文件归档)<br>
**tar -cvf** （添加一个归档）<br>
![](pic/20190913201714.png)<br>
**tar -xvf** （释放一个归档）<br>
![](pic/20190913202026.png)<br>
**tar -zcvf** （添加一个归档并使用gzip压缩）<br>
![](pic/20190913202657.png)<br>
**tar -zxvf** （解压缩并释放归档）<br>
![](pic/20190913203102.png)<br>
#### 查找
> **find / -name " &#42;ab&#42; "** （查找 / 目录下名字包含字符串ab的文件）<br>
>**find / -name "*.txt"**（查找 / 目录下所有txt文件）<br>
>**find / -type d** （查找 / 目录下所有文件夹）<br>
>**find /usr/local/ -user test** （查找 /usr/local/ 目录下用户为 test 的文件）<br>
![](pic/20191008214758.png)<br>
>**find / -size +100M** （查找 / 目录下大小大于100M的文件）<br>
![](pic/20191008220245.png)
>**find / -type f -size +160M -size -180M** （查找 / 目录下大小大于160M并且小于180M的文件）<br>
![](pic/20191008222735.png)<br>
