# 适用于 dnsmasq 的 gfwlist 域名列表
## 脚本依赖
- base64
- curl (https)
- Perl5 v5.10.0+

## 脚本用法
- `curl -4sSkL https://raw.github.com/zfl9/gfwlist2dnsmasq/master/gfwlist2dnsmasq -O`
- `-s <addr>`：用于解析 gfwlist 域名的 dns 服务器地址，参数可选，默认为 127.0.0.1
- `-p <port>`：用于解析 gfwlist 域名的 dns 服务器端口，参数可选，默认为 60053
- `-n <name>`：将解析到的 IP 地址存放至指定的 ipset，如果未指定，则不生成 ipset 选项
- `-l`：生成 gfwlist 域名列表，而非 dnsmasq 配置文件，指定此选项时其它选项将被忽略
- `-h`：查看 gfwlist2dnsmasq 脚本的帮助信息，然后退出脚本

## 成品下载
如果你没有运行 gfwlist2dnsmasq 脚本的条件，也可以从下面的 URL 获取它（6 小时更新一次）
- gfwlist domain lists：<a href="https://zfl9.github.io/gfwlist2dnsmasq/domain_list.txt" download>https://zfl9.github.io/gfwlist2dnsmasq/domain_list.txt</a>
- dnsmasq without ipset：<a href="https://zfl9.github.io/gfwlist2dnsmasq/dnsmasq_gfwlist.conf" download>https://zfl9.github.io/gfwlist2dnsmasq/dnsmasq_gfwlist.conf</a>
- dnsmasq with ipset：<a href="https://zfl9.github.io/gfwlist2dnsmasq/dnsmasq_gfwlist_ipset.conf" download>https://zfl9.github.io/gfwlist2dnsmasq/dnsmasq_gfwlist_ipset.conf</a>
