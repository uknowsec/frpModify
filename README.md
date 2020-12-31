# frpModify

### 域前置与自删除

详情：
[FRP改造计划续](https://uknowsec.cn/posts/notes/FRP%E6%94%B9%E9%80%A0%E8%AE%A1%E5%88%92%E7%BB%AD.html)

注：不管frpc用websocket还是wss，cdn配置都为回源http。

frps
```
[common]
bind_port = 23333
token = uknowsec
```

frpc
```
[common]
server_addr = test.com.w.cdngslb.com
server_port = 443
token = uknowsec
protocol = wss
#protocol = websocket
tls_enable = true
del_enable = true
websocket_domain = test.com

[http_proxy]
type = tcp
remote_port = 10002
plugin = socks5
```

### 指定参数
```
>frpc.exe -t 1.1.1.1 -p 2333
Modify by Uknow
Configure frps.ini As follows

        [common]
        bind_port = 2333
        token = uknowsec

2020/06/21 10:25:57 [I] [service.go:282] [08156671a10a3d42] login to server success, get run id [08156671a10a3d42], server udp port [0]
2020/06/21 10:25:57 [I] [proxy_manager.go:144] [08156671a10a3d42] proxy added: [http_proxy]
2020/06/21 10:25:57 [I] [control.go:179] [08156671a10a3d42] [http_proxy] start proxy success
```

详情：
[FRP改造计划](https://uknowsec.cn/posts/notes/FRP%E6%94%B9%E9%80%A0%E8%AE%A1%E5%88%92.html)

frpc.ini
```
[common]
server_addr = 0.0.0.0
server_port = 2333
token = uknowsec
tls_enable = true
[http_proxy]
type = tcp
remote_port = 23333
plugin = socks5
```


frps.ini
```
[common]
bind_port = 2333
token = uknowsec
```
