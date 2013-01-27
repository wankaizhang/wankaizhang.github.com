---
layout: post
---

# golang的flag包详解

我们编写工具时，经常要处理命令行参数，C程序员应该知道这是一件很繁琐的事情。幸好golang很贴心，下面我举个例子，展示golang怎样处理命令行参数。

假设我们要写个mysql数据库的客户端，能用它连接Mysql服务器，使用方法如下
>mysql -i 10.2.5.101 -p 3306

工具mysql连接本机上的3306端口，我们要通过解析命令行参数，得到IP和端口，用法如下

	package main
	import (
		"flag"
		"fmt"
	)

	var ip *string = flag.String("i", "127.0.0.1", "ip address of mysql server")
	var port *int = flag.Int("p", 3306, "port of mysql server")
	func main() {
		flag.Parse()
        fmt.Println("ip=%v, port=%v", *ip, *port)
	}

结果是

	ip=10.2.5.101, port=3306
