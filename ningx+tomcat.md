ningx

高性能的 **HTTP 服务器**、**反向代理服务器** 和 **负载均衡器**

- **高性能**：采用异步非阻塞的事件驱动模型（epoll/kqueue），能高效处理数万并发连接（远超 Apache 的同步多进程模型）。
- **轻量级**：内存占用低，启动速度快，适合高并发场景（如电商秒杀、直播平台）。
- **多功能**：支持静态资源托管、反向代理、负载均衡、URL 重写、SSL 加密等。
- **高可靠性**：稳定性强，可通过热部署（不停止服务更新配置）保障持续运行。

#### 1.**HTTP 服务器（静态资源托管）**

- 直接处理 HTML、CSS、JS、图片等静态文件，效率远高于动态服务器（如 Tomcat）。
- 示例场景：搭建静态网站（如企业官网、博客）时，用 Nginx 直接返回静态文件。

#### 2. **反向代理**

- **正向代理**：客户端通过代理访问外部服务器（如 VPN）。

- 反向代理

  ：服务器通过代理接收客户端请求，隐藏真实服务器地址。

  - 用途：负载均衡、动静分离（Nginx 处理静态资源，后端服务器处理动态请求）。

#### 3. **负载均衡**

- 当多个后端服务器（如 Tomcat 集群）时，Nginx 按规则分发请求，避免单服务器过载。

- 常见策略：

  - **轮询**：默认方式，依次分配请求。
  - **weight**：权重越高，接收请求越多（如 `server 192.168.1.1 weight=5;`）。
  - **ip_hash**：同一 IP 固定访问同一服务器（解决会话保持问题）。

  #### 4. **其他功能**

  - **URL 重写**：通过 `rewrite` 指令修改请求 URL（如 SEO 优化、跳转）。
  - **SSL 加密**：配置 HTTPS，保护数据传输安全。
  - **缓存**：缓存静态资源，减少后端服务器压力

![image-20250810105504652](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810105504652.png)

![](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810105550753.png)![image-20250810110245388](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810110245388.png)

![image-20250810105618755](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810110421108.png)

![image-20250810105737383](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810105737383.png)

![image-20250810105805572](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810105805572.png)

![image-20250810105925088](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810105925088.png)

lsof -i:80  pid![image-20250810110528139](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250810110528139.png)

nginx -v

nginx.conf

![image-20250813170251493](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250813170251493.png)

![image-20250813170522166](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250813170522166.png)

![image-20250814172323978](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250814172323978.png)

hexo

tomcat

![image-20250819113514893](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819113514893.png)

![image-20250819161402124](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819161402124.png)

ss -nulpt

`ss -nulpt` 是 Linux 系统中用于查询网络连接状态的命令，结合了多个选项的功能，主要用于查看 **UDP 协议相关的网络连接、监听端口及其关联的进程信息**。以下是具体解析：

### 命令选项拆解

- **`ss`**：Socket Statistics 的缩写，用于查询系统的 socket 连接状态，功能类似 `netstat`，但效率更高，支持更多过滤选项。
- **`-n`**：`--numeric`，显示 IP 地址和端口号的数字形式（而非域名或服务名，如直接显示 `192.168.1.1:80` 而非 `example.com:http`）。
- **`-u`**：`--udp`，仅显示 UDP 协议的连接（UDP 是无连接的传输层协议，常用于 DNS、DHCP、视频流等场景）。
- **`-l`**：`--listening`，仅显示处于 **监听状态** 的 socket（即程序正在等待接收连接的端口）。
- **`-p`**：`--processes`，显示与 socket 关联的进程信息（如进程 ID、进程名，需要 root 权限才能完整显示所有进程）。
- **`-t`**：`--tcp`，通常用于显示 TCP 协议连接，但此处与 `-u` 同时使用时，实际效果可能被 `-u` 覆盖（主要显示 UDP 相关）。

localhost 8080

![image-20250819163402131](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819163402131.png)

![image-20250819170207572](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819170207572.png)

![image-20250819170325300](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819170325300.png)

![image-20250819170707556](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819170707556.png)

![image-20250819170813378](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819170813378.png)

![image-20250819171154491](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819171747342.png)

![image-20250819171831353](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819171831353.png)

![image-20250819172542528](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819172542528.png)

### 1. 修改 Tomcat 默认访问端口为 8088

Tomcat 的默认端口配置在`server.xml`文件中，该文件位于 Tomcat 安装目录的`conf`文件夹下。

1. **进入 Tomcat 配置目录**
   打开终端，使用`cd`命令进入 Tomcat 安装目录下的`conf`文件夹。假设 Tomcat 安装在`/usr/local/tomcat`，则执行：

bash

```bash
cd /usr/local/tomcat/conf
```

1. **编辑 server.xml 文件**
   使用文本编辑器（如`vi`或`nano`）打开`server.xml`文件：

bash

```bash
vi server.xml  # 或使用 nano server.xml
```

在文件中找到以下配置片段：

xml

```xml
<Connector port="8080" protocol="HTTP/1.1"
           connectionTimeout="20000"
           redirectPort="8443" />
```

将其中的`port="8080"`修改为`port="8088"`，修改后的片段如下：

xml

```xml
<Connector port="8088" protocol="HTTP/1.1"
           connectionTimeout="20000"
           redirectPort="8443" />
```

1. **保存并退出文件**
   在`vi`编辑器中，按下`Esc`键，输入`:wq`并回车保存修改并退出；在`nano`编辑器中，按下`Ctrl + X`，然后按`Y`确认保存，最后回车退出。
2. **重启 Tomcat**
   进入 Tomcat 安装目录的`bin`文件夹，执行`startup.sh`脚本启动 Tomcat：

bash

```bash
cd /usr/local/tomcat/bin
./startup.sh
```

如果 Tomcat 之前已经启动，需要先执行`shutdown.sh`脚本关闭它，再重新启动。

### 2. 配置一个虚拟主机：域名`www.test.com`，项目目录`/opt/testapp`

1. **编辑 server.xml 文件**
   再次打开`/usr/local/tomcat/conf/server.xml`文件：

bash

```bash
vi /usr/local/tomcat/conf/server.xml
```

1. **添加虚拟主机配置**
   在`server.xml`文件中，找到`<Host>`标签部分（通常在文件末尾附近），或者在`<Engine>`标签内添加以下内容：

xml

```xml
<Host name="www.test.com"  appBase="/opt/testapp"
      unpackWARs="true" autoDeploy="true">
    <Context path="" docBase="/opt/testapp" debug="0" reloadable="true" />
</Host>
```

上述配置中，`name`指定了虚拟主机的域名，`appBase`指定了项目所在的目录，`<Context>`标签定义了应用的上下文路径和文档基础目录。

3. **保存并退出文件**

按照前面介绍的方法，保存并退出`server.xml`文件。

4. **配置本地域名解析（测试用）**

如果是在本地测试，需要修改系统的`hosts`文件来模拟域名解析。在 Linux 系统中，`hosts`文件路径为`/etc/hosts`，使用文本编辑器打开它：

ba

```bash
sudo vi /etc/hosts
```

在文件末尾添加一行：

plaintext

```plaintext
127.0.0.1 www.test.com
```

保存并退出文件。这样在本地访问`www.test.com`时，会被解析到`127.0.0.1`，即本地 Tomcat 服务器。

### 3. 添加管理员用户，能访问 Tomcat 管理后台

Tomcat 的管理员用户配置在`tomcat-users.xml`文件中，该文件也位于`conf`文件夹下。

1. **编辑 tomcat-users.xml 文件**
   打开终端，进入 Tomcat 的`conf`目录：

bash



```bash
cd /usr/local/tomcat/conf
vi tomcat-users.xml
```





![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHgAAAAwCAYAAADab77TAAAACXBIWXMAABYlAAAWJQFJUiTwAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAjBSURBVHgB7VxNUxNJGO7EoIIGygoHQi0HPbBWeWEN+LFlKRdvsHf9AXBf9y7eZe/wA5a7cPNg3LJ2VYjFxdLiwFatVcBBDhAENfjxPO3bY2cyM/maiYnOU5VMT0/PTE+/3+9Md0LViJWVla6PHz8OHB4e9h8/fjyNbQ+qu1SMVqCUSqX2Mea7KG8nk8mt0dHRUi0nJqo1AGF7cPHT79+/H1IxQdsJr0DoNRB6P6iRL4EpsZ8+ffoZv9NW9TZ+Wzs7O9unTp3ar5WLYjQH0uLDhw+9iUSiD7sD+GXMsaNHj65Dstf8aJHwuWAPuOOyqGGiJm6J0RqQPjCXwygOSdU+6POvF30qCHz//v2+TCYzSuKCaw729vaWr1+/vqNitB2E0L+i2I3fPsrLly5d2rXbJNwnWJJLqX0eq+H2hji/I+qL6q6Q5ITdEAevCnG3Lly4sKxidAyePn1KIlNlk8h/G8FMmgZ0qIxaRoNVFaOjQG2LzQF+jHqGnXr+UTUbb7mrq+ufWC13HkgzRDda6yKkPUOasqwJLB4Z8Sr2lDsX4gy/Ypm5C26TtL1K3G2GQipGR8PQkIkp7Vcx/SjHtmPp7XwIDZmQ0qnllPqaFdlSPyiWl5dvgPPTGJC1sbGxvIoAjx49Sh87duwuy/B3lhClLK6urg6XSqWb6XR69uzZs0UVHkjLDN8bkMBMf6k3b97squ8cUFmLGNyNI0eO5M+fP79g6pECvIn6LIpL+OVVRMB9ctyCmQpPnjwZBgH+Qp1CMin37NmzafRpQ4UAppL7+vpoh3tTCIt68MAKXBRZtorcizdQD7yO4QE3crncb0HngzA8N232QYwCJG1a1QFKCwY0i/tleb5qMa5cuVLEczj7Fy9eXEPsegfE/h27WdDhNrZ1PZMf+J4A2ojF7hSISylWUYZGSIiP+x3DYA++fPkyXUVFpVWTgCrMUVoEoRKYzAMCVe0jnlVvMfiDhUKB0ryB8gL6dYNqm3WgR3FkZKQpZ5e0BPOw2JVSLQA6PWEezgswD+PYLKoagQGp217hnElTxqBOwu5OWodPSpsc6mf8rvHu3bt5SGKFGoVmmMUmq2rvC8djQsq6DpJ8m2MERiTzhSLJROQEhm0ZxIDmgtrgwYb9jkG9D3q031P198G5BwfYp2k24Jjq7u4mE4ZiJ1uFyAkM7s6BO8vqMIgFECln7V/DZrbGS9YtwVCfU5Z63vRoYqSP162LeVzIv3379k+/g/BD5ngv+gDQBndUCxA5gT3Ucx6/h/g5BA6yw5CarFu910Ngkd4JuY+nc0bvWn0Z+Ic4PqMaBDWLlwq37sN+k5nSdrsafJCGkVQRgoNrSyqBwX54cHBQ4eSIHQ4duN+cKUOTzKtviw3px0lTwTFCmPQAtn+OZRUyIpVgqMZrlmokigzwWQA3U1U6jkmQHXajVgmGJ3nL3INeKrzLSMOjACctLwmUTemLQ0hjwniuTfiwEKkEM4Fg71MFWuWCq+01n8s05GQx9sZmnGVI8SY9YBU9tJPm/oFwmnmZZLH6p5+LJsz0sdnwyAuRSbBJLNh1eNBFq1wwoQJRYzysgcGo2oaJBQziNGLwOSTep5EmHEac6ekh494mTGKbKa821Bp29ssHRbRbs65bZp74IsD4E+wPVLKyIoxIGDAyAjPH6lbPsL2bVthT4Yz4xMMV8SUGqiYVLY6MjnehOqdshvLBcICp4LX8CKwZhBoKZmDGVK58TV1p1YznX4MnrSuokmHCxs0YgQkjMR+REdjkXS0wXXnP7HglPuqxw20GncUC4wXGyNQq0BAmRGRmzajupSDvuxlEQmCm3CR5XxfcKk3qKlKA1ASqTkj4M+N1zAqTluoNk8TWa9jOnytBYxOPksrndJg5Sv8gEieLqUDVAMjRtMN2nReB2wmI0x1Coa+O/T0JeLUHcy7Z+zhnPirpJSKRYA/1nEddhf0CI6RRf9euKxaLPDdvXatioPr7+yNJCjQCpkCNHcXW0Sz2y40TJ044hIdzVRYtQGNo6RWndBbXmzehZBgIncBwZsaVyzFi+s6PS93xsDBH3tpPu+11VFmfRmCYmWEOX0Xiee7Zx1lv+ou4fBJtbtnH+bEBiLwAhhjk+XzpAPVeCEuqo1DR4/YO1VZQZ93xsJcdbldI5mmcZebX8V6bz2IzH8MmnWNn+EXimQMkvJw3xeuYWJn1YarsUCWYDof7bQwIFhg7uuNhY4cN17ttMD8QUDVCJKZaaERk5drMRM0FNaQjhVDoD+nbhPUcWq0i9JlOpVK6zwyLaKN5TZtxQcQ7SHBsoI73Sks61cTioYZLoRLY68V+tfiOeWkTGxq47HDDThYGMVunRtBffAQ1MAxGZsa1tTNJqYPd1M/JLzVMW4m9nTdZbIf9W6YNjs+KynbuaSeDwgA/2TnkVx38xLLZrzrcb46ofqupGx6Xtyx2uGETuMzJMqqtFuDZNtGnUCXC3F9iWn7jxcyXZ5iD8GcBTD8JopGAC2B2esyOCqfthZZh2nXKtBE13xRkvhKLpQRuQK+uV+azxLMI6wRj/iCi8OM6quxqhGPcHJbtffHiRQZakLMOdxNQE7+AC3/CznOomXUVo+MBoT2DzTnFGaIg7mupH1Axvhc4kxmSXNCDdhg7GTNhKUbnQmiYYZm0TdKxgo3QE5bsD9NidCZcEwlLOtEBr9XY3qHHjx/3qhgdCZHesomEmsAyYWldDozJjMMYHQRZoeGy7K6biYROqlIormeIQ8zPqRgdBa7TYa3Q4CRbKhZhsVZt2eJSDvFs//aGJDUokEMkrqzQ4EwDLnvZwAOyDAAleQAnXo096/YFl7ziwjlKiMslr9xzvH0XQrMkmYgXQmsjuBdC85Jcg8ClDOUiZ6xqvZQhiM25xDux+m4NxOklURnfli1lCKyL8NW+lKHr4u5l82J8YzAxhdeQ/8Op+q/hxUjdMMsJqy/c0ycTx1sy/fRHh7zx08sJIyn1up7lhD8DfU3/IDqhNFQAAAAASUVORK5CYII=)

1. **添加管理员用户配置**
   在`<tomcat-users>`标签内添加以下内容：

xml

```xml
<role rolename="manager-gui"/>
<role rolename="admin-gui"/>
<user username="admin" password="admin123" roles="manager-gui,admin-gui"/>
```

![img](data:image/png;base64,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)

上述配置中，定义了两个角色`manager-gui`（用于访问 Tomcat 的 Web 应用管理界面）和`admin-gui`（用于访问 Tomcat 的服务器管理界面），并创建了一个名为`admin`，密码为`admin123`的用户，并赋予这两个角色。你可以根据实际需求修改用户名和密码。

3. **保存并退出文件**

按照前面介绍的方法，保存并退出`tomcat-users.xml`文件。

4. **重启 Tomcat**

进入 Tomcat 的`bin`目录，先关闭 Tomcat（如果已启动），再重新启动：

bash



```bash
cd /usr/local/tomcat/bin
./shutdown.sh
./startup.sh
```

![img](data:image/png;base64,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)

完成上述步骤后，你就可以通过`http://localhost:8088`（或者`http://www.test.com:8088`，前提是配置了域名解析）访问 Tomcat 服务，通过`http://localhost:8088/manager/html`（使用刚才配置的管理员用户名和密码登录）访问 Tomcat 管理后台。

sll加密 https tls

自签名   商业申请![image-20250819173556511](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819173556511.png)

![image-20250819173723630](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819173723630.png)

![image-20250819174901729](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819174901729.png)

![image-20250819174945238](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819174945238.png)

![image-20250819175155969](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819175155969.png)

![image-20250819175218843](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819175218843.png)

![image-20250819175256861](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819175256861.png)

![image-20250819175308351](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819175308351.png)

![image-20250819223819375](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819223819375.png)

![exported_image](C:\Users\ER\Downloads\exported_image.png)

![image-20250819224955171](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819224955171.png)

![image-20250819225315366](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819225315366.png)

![image-20250819225452816](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819225452816.png)

javaweb sevrlet

![image-20250819232830782](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819232830782.png)

![image-20250819232848801](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819232848801.png)

![image-20250819232908155](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819232908155.png)

![image-20250819232919512](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819232919512.png)

![image-20250819232934062](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819232934062.png)

![image-20250819232954426](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819232954426.png)

![image-20250819233024783](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819233024783.png)

![image-20250819233112558](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819233112558.png)

![image-20250819233256291](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250819233256291.png)

![image-20250820093512643](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250820093512643.png)

![image-20250820093529828](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250820093529828.png)

![image-20250820093540809](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250820093540809.png)

![image-20250820093552464](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250820093552464.png)

![image-20250820093611812](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250820093611812.png)

注解  映射 xml配置