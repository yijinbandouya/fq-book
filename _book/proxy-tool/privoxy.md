# privoxy

[privoxy](https://www.privoxy.org/)是一个http/https协议代理工具，通过它将sock协议转换为http/https协议，以便访问互联网，这也是v2rayGUI与ss自带的协议转发软件。

打开`option`选择`edit main configuration`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-05-06_200606.png)

在配置文件中末尾处添加`forward-socks5 / 127.0.0.1:1080 .`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-05-06_200824%20%281%29.png)

到`代理`中设置privoxy的默认地址与监听端口

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-05-06_201359.png)

测试

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-05-06_203158.png)

