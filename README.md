# dns-server
A DNS server app written by pure Nodejs for develop and test use. Only support IPv4 now.

纯Nodejs写的本地DNS服务器，供开发测试使用。前端做网站时，一般本地调试时的url是IP地址。但有些功能需要有域名才能工作，那么用这个工具来做本地解析就好了。

效果

https://tools.ietf.org/html/rfc1035

## 使用方法How to use

按照图示，找到原来的DNS服务器地址，并改成`127.0.0.1`

### Mac

![mac](image/mac-before.jpg)
![mac](image/mac-after.jpg)

### Windows

![win](image/win-view-dns.jpg)
![win](image/win-before.jpg)
![win](image/win-after.jpg)

打开`index.js`:

![code](image/code.jpg)

- 把fallbackServer改成原来的DNS服务器地址
- 把domain改成你想解析的域名关键字。
- 把targetIp改成你想解析到的IP地址


然后用node运行`index.js`。mac上需要`sudo node index.js`。


## 可以做更多You can do more

- 把关键字做成正则匹配 use expression to match keyword
- 加入配置文件，可匹配多个关键字 use configuration file to match multiple keywords
- 增加命令行参数，不用在源码修改关键字 add command line args support to avoid modify the keyword in source code
