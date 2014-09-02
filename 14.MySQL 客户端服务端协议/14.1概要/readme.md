#14.1概要

######[传送门](http://dev.mysql.com/doc/internals/en/overview.html)
---
#####内容：
14.1.1.	基本类型
14.1.2. MySQL数据报文
14.1.3.	通用应答报文
14.1.4.	字符集
14.1.5.	连接生命周期
14.1.6. 命令行阶段


_ _ _


MySQL协议用于MySQL客户端和服务端之间，已经实现有：
- Connectors (Connector/C, Connector/J等等)
- MySQL 代理
- 主从服务器复制之间

协议支持如下属性：
- SSL（14.5 SSL）透明加密
- Compression（14.4压缩）透明压缩
- 连接阶段特性和认证数据交换
- 命令阶段支持预处理语句（14.7 预处理语句）和储存过程（14.8 储存过程）

文档基于MySQL服务端的源文件：
- sql/sql_parse.cc 用于基本协议
	- dispatch_command()
- sql/sql_prepare.cc 用于预处理语句
	- mysql_stmt_prepare()
	- mysql_stmt_execute()
	- mysql_stmt_close()
	- mysql_stmt_reset()
	- mysql_stmt_fetch()
	- mysql_stmt_get_longdata()
- sql/sql_repl.cc 用于binlog 协议
	- mysql_binlog_send()
- sql/protocol.cc 用于值和类型编码
