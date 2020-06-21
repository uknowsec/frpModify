# frpModify

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
