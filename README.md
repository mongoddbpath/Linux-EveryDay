# Linux-EveryDay
### Linux是什么 ： <https://zh.wikipedia.org/wiki/Linux>
#### 每天一个实用的Linux基础命令【常用】，结合老师课件以及网上资料，轻轻松松让你掌握Linux的基础使用...
#### 命令演示的效果来自**Ubuntu 14.04.5**
***
### 第一天
```
 ls命令
-a：显示所有档案及目录（ls内定将档案名或目录名称为“.”的视为影藏，不会列出）； 
-A：显示除影藏文件“.”和“..”以外的所有文件列表；
-C：多列显示输出结果。这是默认选项； 
-l：与“-C”选项功能相反，所有输出信息用单列格式输出，不输出为多列；
-F：在每个输出项后追加文件的类型标识符，具体含义：“*”表示具有可执行权限的普通文件，“/”表示目录，“@”表示符号链接，“|”表示命令管道FIFO，“=”表示sockets套接字。当文件为普通文件时，不输出任何标识符； 
-b：将文件中的不可输出的字符以反斜线“”加字符编码的方式输出；
-c：与“-lt”选项连用时，按照文件状态时间排序输出目录内容，排序的依据是文件的索引节点中的ctime字段。与“-l”选项连用时，则排序的一句是文件的状态改变时间； 
-d：仅显示目录名，而不显示目录下的内容列表。显示符号链接文件本身，而不显示其所指向的目录列表；
-f：此参数的效果和同时指定“aU”参数相同，并关闭“lst”参数的效果； 
-i：显示文件索引节点号（inode）。一个索引节点代表一个文件； --file-type：与“-F”选项的功能相同，但是不显示“*”；
-k：以KB（千字节）为单位显示文件大小； 
-l：以长格式显示目录下的内容列表。输出的信息从左到右依次包括文件名，文件类型、权限模式、硬连接数、所有者、组、文件大小和文件的最后修改时间等；
-m：用“,”号区隔每个文件和目录的名称；
-n：以用户识别码和群组识别码替代其名称；
-r：以文件名反序排列并输出目录内容列表； 
-s：显示文件和目录的大小，以区块为单位； 
-t：用文件和目录的更改时间排序； 
-L：如果遇到性质为符号链接的文件或目录，直接列出该链接所指向的原始文件或目录； 
-R：递归处理，将指定目录下的所有文件及子目录一并处理； 
--full-time：列出完整的日期与时间； 
--color[=WHEN]：使用不同的颜色高亮显示不同类型的。
```

```
ls 命令-查看文件列表
ls	# 查看当前目录的文件列表
ls -a	# 查看当前目录所有文件列表
ls -l	# 查看当前目录的文件详细信息   
ls -la	# 查看当前目录所有文件详细信息 
ls -ld	# 查看当前目录本身的详细信息   
ls -Rm /boot # 以递归紧凑方式查看/boot 目录 
ls -lt	# 按时间排序 (从新到旧)
ls -ltr	# 按时间反向排序 (从旧到新)
ls -lS	# 按文件大小排序 (从大到小)
ls -i #显示文件的软链接
```
![](http://or30iz1wj.bkt.clouddn.com/ls.gif)
***
### 第二天
```
cd 命令-随处逛逛【小技巧，按Tab键自动补全目录】
cd /home/andy/Desktop	# 进入andy用户桌面目录
cd	# 返回我的主目录
cd ~	# 返回我的主目录
cd -	# 回到上次去的目录
cd .. #回到上级目录
pwd  命令：我到哪儿了？
pwd
```
![](http://or30iz1wj.bkt.clouddn.com/cdok.jpg)
***
### 第三天
```
mkdir 命令-创建文件夹
mkdir ** #在当前目录创建文件夹
mkdir -p **/** #在文件夹下创建文件夹，用于逐层创建文件夹
```
![](http://or30iz1wj.bkt.clouddn.com/mkdir.jpg)
***
### 第四天
```
who 命令 - 我是谁
查看用户
whoami	# 我是谁？  
who am i	# 我究竟是谁？ 
who	# 都有谁在呀？
w	# 都有谁在呀？
```
![](http://or30iz1wj.bkt.clouddn.com/whoami.jpg)
***
### 第五天
```
rm 命令 - 删除文件
删除文件
rm f8 f9  # 删除f8,f9
rm -i f7 # 删除前确认
rm -f f* # 强行删除
```
```
rmdir 命令 - 删除目录
rmdir d7 d8 # 删除空目录
rmdir -p dir1/dir2/dir3 # 删除多层空目录
rm -r d6 dir1 # 删除目录
rm -rf / # 删除所有文件!!! （Linux自杀命令）
```
![](http://or30iz1wj.bkt.clouddn.com/rmdir.jpg)
***
### 第六天
```
mv 命令 - 移动命令
移动文件
mv f4 f4.1	# 将 f4 移动 (重命名) 为 f4.1
mv f5 d3	# 将文件移动到目录
mv -i f5 f6	# 覆盖时提示
mv -b f6 f666 #做简单备份
mv -f f666 ../d6/  #强制移动
mv f6 c/f6.1	# 移动并改名
mv	*.1 d4	# 将文件移动到目录
移动目录
mv d4 dir1/dir2 #移动目录
mv d5 d05 #目录改名
```
![](http://or30iz1wj.bkt.clouddn.com/6a1.jpg)
![](http://or30iz1wj.bkt.clouddn.com/66aa6.jpg)
***
### 第七天
```
cp 命令 - 复制命令
cp test1 test2 #复制单个文件到目标目录，文件在目标文件中不存在
cp -a test3 test5 #复制整个目录
cp -s test6 test7 #建立一个连结档
```
![](http://or30iz1wj.bkt.clouddn.com/Cp61.jpg)
***
### 第八天
```
touch 命令 - 创建文件命令
touch hello.js
vim hello.js
```
![](http://or30iz1wj.bkt.clouddn.com/touch61.jpg)
***
### 第九天
```
cat命令 - 标准打印命令
cat hello.js #打印查看hello.js的信息
cat -n hello.js #打印查看的同时看见行号
cat hello.js world.js > helloLinux.js #合并文件
cat hello.js > hello2.js #相当于复制
```
![](http://or30iz1wj.bkt.clouddn.com/cat61.jpg)
***
### 第十天
```
more命令 - 逐页阅读信息命令
常用操作命令：
Enter    向下n行，需要定义。默认为1行
Ctrl+F   向下滚动一屏
空格键  向下滚动一屏
Ctrl+B  返回上一屏
=       输出当前行的行号
：f     输出文件名和当前行的行号
V      调用vi编辑器
!命令   调用Shell，并执行命令 
q       退出more

man cat | more
```
![](http://or30iz1wj.bkt.clouddn.com/more61.jpg)




