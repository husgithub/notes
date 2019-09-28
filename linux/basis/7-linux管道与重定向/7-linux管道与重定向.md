### linux管道与重定向
命令通过STDIN接受参数或数据，通过STDOUT输出结果或通过STDERR输出错误
名称	|说明|编号|默认
:--|:--|:--|:--
STDIN|标准输入|0|键盘
STDOUT|标准输出|1|终端
STDERR|标准错误|2|终端
#### 管道
将一个程序的标准输出写到一个文件中去，再将这个文件作为另一个程序的输入。管道要解决的就是不需要临时文件就能将两条命令结合在一起<br>

<table>
    <tr>
        <th>分类</th>
        <th>关键字</th>
        <th>定义</th>
        <th>例子</th>
    </tr>
    <tr>
        <td rowspan="5">重定向</td>
        <td>></td>
        <td>将STDOUT重定向到文件（覆盖）</td>
        <td>
            echo "hello world" > out.txt <br>
            ls -l > out.txt
        </td>
    </tr>
    <tr>
        <td>>></td>
        <td>将STDOUT重定向到文件（追加）</td>
        <td>
            echo "hello world" >> out.txt <br>
            date >> out.txt
        </td>
    </tr>
    <tr>
        <td>2></td>
        <td>将STDERR重定向到文件（覆盖）</td>
        <td>
            hello 2> err.txt（不存在的命令）<br>
        </td>
    </tr>
    <tr>
        <td>2>&1</td>
        <td>将STDERR与STDOUT结合（覆盖）</td>
        <td>
        </td>
    </tr>
    <tr>
        <td><</td>
        <td>重定向STDIN</td>
        <td></td>
    </tr>
    <tr>
        <td rowspan="1">管道</td>
        <td>|</td>
        <td>将一个命令的STDOUT作为另一个命令的STDIN</td>
        <td>
            ls -l | grep "a"<br>
            find -user root | grep "zip"
        </td>
    </tr>
</table>
