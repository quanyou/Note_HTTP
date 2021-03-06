#### 通过请求和响应的交换达成通信
* 请求报文是由请求方法、请求URI、协议版本、可选的请求首部字段和内容实体构成。
* 响应报文基本由协议版本、状态码（表示请求成功或失败的数字代码）、用以解释状态码的原因短语、可选的响应首部字段以及实体主体构成。

#### HTTP方法
* **GET**（获取资源）：请求访问已经被URI标识的资源
* **POST**（传输实体主体）：传输实体主体和GET类似，但是POST主要是为了发送而不是为了获取实体主体
* **PUT**（传输文件）：想URI标识的指定的资源位置传输文件，传输的文件放在实体主体中。一般不使用，因为PUT不存在验证机制，有安全隐患。当使用Web的验证机制或使用**REST**（Representational Status Transfier, 表征状态转移）时有可能使用
* **HEAD**（获取报文首部）：和GET方式差不多，但不获取实体主体，主要目的是为了获取报文头部的协议版本，日期时间等
* **DELETE**：删除URI标识的指定位置的资源，和PUT正好相反，同样不经常再使用，原因同样存在安全隐患。如果使用Web的验证机制，或使用REST，有可能被使用
* **OPTIONS**（询问支持的方法）：询问URI标识的指定位置的资源支持的访问方法。
* **TRACE**（追踪路径）：让Web服务器端将之前的请求通信返回给客户端的方法。使用在MAX-Forwords首部字段填入数值，没经过一个服务器，数值减一，当数值为0时停止传输。
* **CONNECT**（用隧道协议连接代理）：在与代理服务器通讯时建立隧道，实现用隧道协议进行TCP通信。主要使用SSL（Secure Sockets Layer, 安全套接层）和TLS（Transport Layer Security, 传输层安全）协议把通信内容加密后经网络隧道传输。