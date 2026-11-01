## 防火墙

```sh
# 默认禁止所有外部主动连接
ufw default deny incoming

# 默认允许服务器主动向外连接
ufw default allow outgoing

# 放行ssh 22端口
ufw allow 22/tcp

# 开启防火墙
ufw enable

# 检测状态
ufw status verbose

# 放行443 tcp/udp
ufw allow 80/tcp
# hy2用
ufw allow 443/udp
# reality用
ufw allow 443/tcp
# xhttp用
ufw allow 8443/tcp
# 订阅链接用
ufw allow 2096/tcp
```

## 全局路由规则

https://github.com/hcloudlab/Hrules

