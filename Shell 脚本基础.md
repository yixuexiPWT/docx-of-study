### Shell 脚本基础

Shell 脚本是一种为 Shell 编写的脚本程序，常见的 Shell 有 Bash（Bourne Again SHell），它是许多 Linux 系统默认的 Shell。

#### 脚本格式

1. 脚本开头需指定解释器，格式为`#!/bin/bash`，这行代码告诉系统用 Bash 来执行该脚本。
2. 脚本中的注释以`#`开头，注释内容不会被执行，用于解释脚本功能或步骤。
3. 脚本中的命令和语法遵循相应 Shell 的规范。

一个简单的 Shell 脚本示例：

bash

vim esc !wq  

./ xxx.sh

chmod +x xxx.sh   sh xxx.sh

![image-20250815105849159](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815105849159.png)





```bash
#!/bin/bash
# 这是一个简单的Shell脚本示例
echo "Hello, World!"  # 输出Hello, World!
```

human alh![image-20250815112841062](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815112841062.png)

![img](data:image/png;base64,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)

### 常用 Shell 命令

1. 文件和目录操作
   - `ls`：列出目录内容。`ls -l`以长格式显示，`ls -a`显示所有文件（包括隐藏文件）。
   - `cd`：切换目录。`cd /home`切换到 /home 目录，`cd ..`回到上一级目录。
   - `pwd`：显示当前工作目录的路径。
   - `mkdir`：创建目录。`mkdir new_dir`创建名为 new_dir 的目录，`mkdir -p dir1/dir2`创建嵌套目录。
   - `rm`：删除文件或目录。`rm file.txt`删除 file.txt，`rm -r dir`删除 dir 目录及其内容（需谨慎使用）。
   - `cp`：复制文件或目录。`cp file1.txt file2.txt`复制 file1.txt 为 file2.txt，`cp -r dir1 dir2`复制目录。
   - `mv`：移动或重命名文件 / 目录。`mv file.txt dir/`将 file.txt 移动到 dir 目录，`mv oldname.txt newname.txt`重命名文件。
2. 文件内容查看
   - `cat`：显示文件内容。`cat file.txt`直接显示，`cat -n file.txt`显示行号。
   - `more`：分页显示文件内容，按空格键翻页，按 q 退出。
   - `less`：与 more 类似，但支持向前翻页等更多操作。
   - `head`：显示文件开头部分内容，默认显示前 10 行。`head -n 5 file.txt`显示前 5 行。
   - `tail`：显示文件结尾部分内容，默认显示后 10 行。`tail -n 5 file.txt`显示后 5 行，`tail -f log.txt`实时查看日志文件更新。
3. 文本处理
   - `grep`：在文件中搜索匹配的字符串。`grep "pattern" file.txt`搜索 file.txt 中含 pattern 的行，`grep -r "pattern" dir/`递归搜索 dir 目录下的文件。
   - `sed`：流编辑器，用于对文本进行处理。`sed 's/old/new/' file.txt`将 file.txt 中每行第一个 old 替换为 new。
   - `awk`：用于文本分析和处理，适合处理结构化数据。`awk '{print $1}' file.txt`打印 file.txt 中每行的第一个字段。
4. 系统信息相关
   - `ps`：显示进程状态。`ps aux`显示所有进程的详细信息。
   - `top`：动态显示系统中进程的资源占用情况，按 q 退出。
   - `df`：显示磁盘空间使用情况。`df -h`以人类可读的格式显示。
   - `free`：显示系统内存使用情况。`free -h`以人类可读的格式显示。
   - `uname`：显示系统信息。`uname -a`显示所有系统信息。
5. 权限管理
   - `chmod`：修改文件或目录的权限。`chmod 755 file.sh`设置 file.sh 的权限为所有者可读可写可执行，组和其他用户可读可执行。
   - `chown`：修改文件或目录的所有者和所属组。`chown user:group file.txt`将 file.txt 的所有者改为 user，所属组改为 group。

### Shell 脚本的执行

1. 先给脚本添加执行权限：`chmod +x script.sh`
2. 执行脚本：`./script.sh`（在脚本所在目录）或使用绝对路径`/path/to/script.sh`
3. ps -ef | grep mysql | grep -vc grep

![image-20250815101340775](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815101340775.png)

grep  (查找)   sed  （替换）  awk（提取） 文本处理

netstat nltp | 80

![image-20250815102318057](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815102318057.png)

 [Shell编程入门(1).pdf](D:\xwechat_files\wxid_7qv6t8yjv7ea22_55ef\msg\file\2025-08\Shell编程入门(1).pdf) ![image-20250815102545850](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815102545850.png)

[]()

![image-20250815143820515](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815143820515.png)

![image-20250815153136764](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815153136764.png)

![image-20250815153606343](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815153606343.png)

local

