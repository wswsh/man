@20151202
Iptables是绝大多数linux发行版内建的防火墙
在CentOS<7的版本中可以使用一下命令

#### 基本概念
```
Chain: INPUT, OUTPUT, FORWARD 等等
target: DROP, ACCEPT 等等
rule：具体一条规则
```

#### iptables -L -n 没有任何规则

因为没有启动防火墙

#### 查看 iptables 当前配置

```
iptables -L -n 或者 iptables -nL， 注意 iptables -Ln 不行
```

#### 禁止某个ip

```
iptables -I INPUT -s 114.32.207.47 -j DROP
```
#### 清除rule

``` 
# 清除某条Chain上的所有rule
iptables -F OUTPUT
```

#### 查看Iptables的状态
    # service iptables status
    # service ipv6tables status

#### 关闭iptables
    # service iptables stop
    # service ipv6tables stop

#### 启动iptables
    # service iptables start
    # service ipv6tables start

#### 从系统自启动列表中删除iptables
    # chkconfig iptables off
    # chkconfig ipv6tables off

#### 将iptables添加进系统自启动列表
    # chkconfig iptables on
    # chkconfig ipv6tables on

在CentOS7之后的版本统一用systemctl命令:  

    # systemctl [status|start|stop|restart] iptables
    # systemctl [status|start|stop|restart] ipv6tables
