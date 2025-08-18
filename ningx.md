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