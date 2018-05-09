# NAT类型科普及一些简单提升NAT类型的方法

> 转载自：[http://www.right.com.cn/forum/thread-199299-1-1.html](http://www.right.com.cn/forum/thread-199299-1-1.html)

首先可以在百度百科了解到什么是“[**NAT**](http://baike.baidu.com/item/nat)”，传送门→“[**NAT科普**”](http://baike.baidu.com/item/nat)  
然后呢，看了那么多我们大概就知道了一些关于NAT的基本知识，比如说[**定义**](http://baike.baidu.com/item/nat)、[**功能**](http://baike.baidu.com/item/nat#1)、[**实现方式**](http://baike.baidu.com/item/nat#2)及[**类型**](http://baike.baidu.com/item/nat#7)
  
  
提升NAT类型的好处：  
浏览网页、观看视频、游戏等更顺畅，下载速度更稳定快速，  
特别是对那些玩ED2K/PT下载、PS4/XBox主机游戏的，  
提升NAT类型后更有可能获取到HigtID、更容易进入游戏房间连线等。  
  
好了，废话有点多了。  
要提升NAT类型，我们必须知道NAT的4个类型：NAT1、NAT2、NAT3、NAT4。  
它们分别对应（详情见[百度百科](http://baike.baidu.com/item/nat#7)）：  
**NAT1 **→ **Full Cone** NAT  
**NAT2 **→ **Address-Restricted Cone** NAT  
**NAT3 **→ **Port-Restricted Cone** NAT  
**NAT4 **→ **Symmetric** NAT  
  
说些比较重要的前话：路由器少一层是一层，这样越有可能得到NAT1和NAT2这两类NAT类型。  
一般建议家里的网路是以下两种拓扑类型：  
1、光猫桥接→主路由（拨号连接外网用）→副路由（纯AP模式，扩展信号）  
2、光猫拨号（直接充当主路由）→副路由（纯AP模式，扩展信号）  
这样的好处是桥接和纯AP是不进行NAT的，而是SWitch，所以不会导致多一层NAT。  
  
如果你的网络是NAT1，那这是最宽松的网络环境，你想做什么，基本没啥限制；  
如果是NAT4的话，这是最严格的网络环境，可能会玩不了游戏、下载都没速度；  
一般，我们家里的设备都是通过光猫桥接+无线路由器拨号的形式连接到外网的，  
此时，基本是NAT2和NAT3，正常情况对看网页、游戏及下载都没有过多的限制。  
  
  
但是，现在个别网络游戏严格要求你的网络环境必须是“**NAT2**”以上（NAT2和NAT1），才能进行游戏。  
而你的网络环境又是"NAT3”及“NAT4",那到底该怎么办呢？  
下面我们介绍一些简单提升NAT类型的方法，其实就是进行[**NAT穿透**](http://baike.baidu.com/item/nat#3_3)（[NAT Traversal](http://baike.baidu.com/item/nat#3_3)）：  
1、如果你的路由器有启用“**Full Cone”、“STUN”、“TURN”、“ICE”、“uPnP”**等功能，果断都启用了。  
如果没有的话，你的路由器差不多可以扔了，因为现在的路由器**“uPnP”**基本是标配，连这都没有，那你的路由器是有多古董。  
2、如果你的路由器没有以上功能，那可以找下有没有**“**[DMZ](http://baike.baidu.com/item/dmz)**”**功能（什么是“DMZ”，请问度娘 → [DMZ](http://baike.baidu.com/item/dmz) ）,  
有的话，可以启用它，并把你要提升NAT类型的主机IP地址设置好。  
（一般建议有“Full Cone”、“uPnP”等，就不要开"DMZ”了，除非你是PS4/XBox这类游戏主机要提升NAT类型）  
3、在Windows上把以下三个服务设置为自动启动，并启动该服务：  
一般这三个服务都会被奇虎360等带启动项优化的软件当做无用启动项**被“优化”**成禁止启动。  
怎么手动设置为自动启动，并启动，详情问 → [**度娘**](https://zhidao.baidu.com/question/209154882.html)  
  
Function Discovery Provider Host  
Function Discovery Resource Publication  
SSDP Discovery  
  
4、在 Windows 防火墙，放行你需要提升NAT类型的软件或者游戏程序（EXE程序或者UWP程序），  
如果你不会放行，也可以直接关闭 Windows 防火墙。（一般不推荐这样做，还是老话，不懂问“[**度娘**](https://zhidao.baidu.com/question/1735570524535246787.html)”）  
第4步很重要，这步没做，等于其它的全是在做无用功。  
5、如果你的设备是通过电脑共享网络的形式上网的，建议把这个服务也打开：UPnP Device Host  
以上，能弄的都弄了，这样你的网络环境就会越好，甚至NAT1都没有问题。  
  
这是我通过以上设置，进行NAT穿透+公网IP一枚，测得的结果：  
![](http://www.right.com.cn/forum/data/attachment/forum/201611/10/132059dd4rfiilqz4e4s4p.jpg)   
妥妥的NAT1  
  
最后附上NAT类型测试工具：  
![](http://www.right.com.cn/forum/static/image/filetype/zip.gif) [NAT类型测试.zip](http://www.right.com.cn/forum/plugin.php?id=imc_attachad:ad&aid=MTQzODYzfDQxMGQxODFmfDE1MjU4MzkxMjZ8MHwxOTkyOTk%3D) 
  
P.S.:  
1、如果能找运营商要到外网IP，这是最好的，没有公网IP的话可以打电话给客服，  
说“我家的宽带怎么没有公网IP啊，我需要在家里安装远程监控，没有公网IP的话不行，如果不给我公网IP，我只好退宽带换别家的了。”  
态度强硬点，最好一开始就把客服的工号也要了，说完上面的，再补上“不给就投诉你。”；  
2、还有一种最笨的就是直接电脑拨号上网，Windows 直接把防火墙关了，只要你的是公网IP，妥妥的基本都是NAT1；  
3、如果要不到公网IP，能提升到NAT2，这样也很不错了；  
4、如果你是要提升PS4/XBox这类游戏主机的NAT类型，建议以上能做的都做了。    
  


