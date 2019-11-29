# 介绍
基于 Ansible 安装 elasticsearch 单机或集群。

# Role 介绍

| role | 功能 | 默认端口 | 
| :---- | ---- | ---- | 
| init | 环境初始化，包括：<br>- 关闭Selinux<br>- 关闭防火墙<br>- 更换yum源为阿里源<br>- 设置时区为 Asia/Shanghai<br>- 安装NTP<br>- 设置ntp时钟同步<br>- 增加文件描述符<br>- 禁用交换<br>- 调整虚拟内存<br>- 调整最大并发连接<br>- 配置线程数<br>- 设置 ip 转发<br>- 安装 vim | - | 
| jdk | 安装jdk（1.8） | - | 
| nodejs | - 安装node.js（12.13.1）<br>- 更换npm源为阿里源 | - | 
| elasticsearch6.x | 安装 elasticsearch（6.8.5）单机或集群 | 9200 | 
| elasticsearch-head | 安装 elasticsearch-head 插件 | 9100 | 
| kibana | 安装 kabana（7.4.2）插件 | 5601 | 