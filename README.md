# frp_bypass

frpc.ini
```
[common]
server_addr = 0.0.0.0
server_port = 2333
privilege_token = pentest999
tls_enable = true
[http_proxy]
type = tcp
remote_port = 23333
plugin = socks5
```


frps/ini
```
[common]
bind_port = 2333
token = uknowsec
```
