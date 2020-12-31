详情：
[FRP改造计划续](https://uknowsec.cn/posts/notes/FRP%E6%94%B9%E9%80%A0%E8%AE%A1%E5%88%92%E7%BB%AD.html)

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
