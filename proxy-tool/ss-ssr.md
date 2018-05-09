# SS/SSR

## Shadowsocks

### 入门操作

访问ss站点，右键扫描二维码

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-30_105508.png)

 此时已经可以连接互联网了，如果你的系统不是自动设置的，请看服务器配置说明

WiFi局域网共享手机

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-05-05_032022.png)

`网络和共享中心`-&gt;`wlan`-&gt;`详细信息`查看本机网卡IP地址

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-05-05_032400.png)

`高级`设置`代理`选择`手动`，按照如下信息设置

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/qq-tu-pian-20180505033638.jpg)

测试

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/qq-tu-pian-20180505a.jpg)



### 服务器配置说明

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-28_224352.png)

PAC模式即脚本配置模式，收录的网址走代理路线，没有收录的地址则不走代理路线即正常访问。例如将Google加入代理访问列表，配置规则如下：

```text
 ".google.com",
"||google.com",
```

在`pac`选项中-&gt;`编辑本地pac文件`即可

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-28_230423.png)

## ShadowsocksR

### 订阅功能

如图设置

![1](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-28_235146.png)

![2](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-28_235317.png)

![3](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-28_235337.png)

![4](https://raw.githubusercontent.com/loremwalker/fq-book/master/.gitbook/assets/2018-04-28_235358.png)

订阅的好处：

* 一键导入多条服务器地址
* 不需要经常打开站点网址即可更新服务器配置（取决于订阅源）

### 补充说明

ss与ssr的二维码不能通用，否则会出现未扫码二维码的窗口提示

ss与ssr都做了socks代理端口对http协议的兼容，所以浏览器也是能访问站点的

全局模式即被的代理软件所有网络均走代理路线，直连模式即正常访问不走任何代理

