1 mac地址和arp协议
2 k8s flannel vxlan网络抓包实践

- k8s网络架构
- 容器网络的优缺点
- vxlan overlay网络

arp报文格式

![ARP帧格式](https://img-blog.csdn.net/20170512131909950?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMTc4NDQ5NQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

arp欺骗

托管：从IaaS到PaaS

![image-20220613084828457](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613084828457.png)

虚拟化和容器的区别

- 容器没有硬件虚拟化层、guest OS层，只是一个通过参数clone namespace的进程

k8s架构和组件通信方式

![image-20220613085259646](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613085259646.png)

flannel L2和L3通讯方式

![image-20220613085610803](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613085610803.png)

flannel通讯

![image-20220613090823123](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613090823123.png)

关于k8s网络的衍生阅读
https://xie.infoq.cn/article/1a45c8eca65710ed8c4ca331f

3层可达的网络

![image-20220613090907238](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613090907238.png)

iptables

![image-20220613090929371](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613090929371.png)

测试环境的ip地址声明

![image-20220613091021238](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613091021238.png)

veth pair与bridge

![image-20220613091206179](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613091206179.png)

同主通讯：cni0与veth pair

![image-20220613091319656](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613091319656.png)

跨主通讯1

![image-20220613091437684](C:\Users\xjshen\AppData\Roaming\Typora\typora-user-images\image-20220613091437684.png)

vxlan报文格式

![VXLAN 报文格式_VXLAN 报文格式_02](https://s9.51cto.com/images/blog/202010/23/8b59c6a027f7dc752a2e01f75a5b45aa.png?x-oss-process=image/watermark,size_16,text_QDUxQ1RP5Y2a5a6i,color_FFFFFF,t_30,g_se,x_10,y_10,shadow_20,type_ZmFuZ3poZW5naGVpdGk=)