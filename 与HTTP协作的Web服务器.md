#### 单台虚拟主机实现多个域名
* 域名通过DNS（Domain Name System）服务映射到IP地址（域名解析）之后访问目标网站。当请求发送到服务器时，已经是以IP地址形式访问了。
* 在相同的IP地址下，由于虚拟主机可以寄存多个不同主机名和域名的Web网站，因此在发送HTTP请求时，必须在Host首部内完整指定主机名或域名的URI。

#### 通信数据转发程序：代理、网关、隧道
##### 代理
* 是一种联系Client和Server，作为“中间人”的应用程序。既可以接收客户端的请求并转发给服务器，同时也可以接受服务器返回的响应并转发给客户端。
* 缓存代理（Caching Proxy）：预先将资源的副本（缓存）保存在代理服务器上。当请求再次请求同意资源时，会优先使用缓存
* 透明代理（Transparent Proxy）：不对报文做任何加工的代理类型。

##### 网关
* 中间代理服务器的作用，和源服务器作用相似。
* 可使通信线路上的服务器提供非HTTP协议服务。
* 能提高通信的安全性，因为可以在客户端与网关之间的通信线路上加密以确保连接的安全。

##### 隧道
* 在客户端和服务器端进行中转，并保持双方通信连接的应用程序。
* 按要求建立起一条与其他服务器的通信线路，可使用类似SSL（Secure Sockets Layer）等加密手段进行通信。
* 保证了通信的安全。