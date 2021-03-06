#### HTTP报文
* 用于HTTP协议交互的信息被称为报文。
* 请求端的报文称为请求报文，响应端（Server）的报文称为响应报文
* 报文是由多行（CR+LF作换行符）数据构成的字符串文本。
* 报文分为报文首部和报文主体组成，以第一次出现的空行（CR+LF）来区分首部和主体。一份报文里一定有报文首部，不一定有报文主体。

#### 请求报文及响应报文的结构
##### 请求报文
###### 报文首部
* 请求行
* 请求首部字段
* 通用首部字段
* 实体首部字段
* 其他


###### 空行（CR+LF）
###### 报文主体

##### 响应报文
###### 报文首部
* 状态行
* 响应首部字段
* 通用首部字段
* 实体首部字段
* 其他

###### 空行（CR+LF）
###### 报文主体
#### 编码提升传输速率
##### 报文主体和实体主体的差异
* **报文**（message）：HTTP通信中的基本单位，由8位组字节流（octet sequence，其中octet表示8个比特），通过HTTP通信传输。
* **实体**（entity）：作为请求或响应的有效载荷数据（补充项）被传输，起内容由实体首部和实体主体组成。

##### 压缩传输的内容编码
* 内容编码指明应用在实体内容上的编码格式，并保持实体信息原样压缩。内容编码后的实体由客户端接收并负责解码。
* 常用内容编码：gzip（CNU zip）、compress（UNIX系统的标准压缩）、deflate（zlib）、identity（不进行编码）

##### 分割发送的分块传输编码
* 把实体主体分块的功能称为分块传输编码（Chunked Transfer Coding）
