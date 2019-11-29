# 介绍
基于 Ansible 自动安装 elasticsearch 单机或集群。

# 支持操作系统

- CentOS 7.x

# Role 说明
| role | 功能 | 端口 | 
| :---- | ---- | ---- | 
| init | 环境初始化，包括：<br>- 关闭Selinux<br>- 关闭防火墙<br>- 更换yum源为阿里源<br>- 设置时区为Asia/Shanghai<br>- 安装NTP<br>- 设置ntp时钟同步<br>- 修改文件限制<br>- 调整虚拟内存<br>- 调整最大并发连接<br>- 设置 ip 转发<br>- 开启BBR（未实现） | - | 
| jdk | 安装jdk（1.8） | - | 
| nodejs | 安装node.js（12.13.1） | - | 
| elasticsearch | 安装 elasticsearch（7.4.2）单机或集群 | 9200 | 
| elasticsearch-head | 安装 elasticsearch-head 插件 | 9100 | 
| kibana | 安装 kabana（7.4.2）插件 | 5601 | 

# 使用
```bash
# 配置主机列表
$ vim hosts

# 配置变量
$ vim group_vars/main.yml

# 安装
$ ansible-playbook -i hosts site.yml
```
