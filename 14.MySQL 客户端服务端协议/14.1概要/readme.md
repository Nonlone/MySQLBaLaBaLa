#14.1概要
MySQL协议用于MySQL客户端和服务端之间，已经实现有：
- Connectors (Connector/C, Connector/J等等)
- MySQL 代理
- 主从服务器复制之间

协议支持如下属性：
SSL（14.5 SSL）透明加密
Compression（14.4压缩）透明压缩
连接阶段特性和认证数据交换
命令阶段支持预处理语句（14.7 预处理语句）和储存过程（14.8 储存过程）
