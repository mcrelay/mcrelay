# user

## user能力

作为host:
向center请求服务器列表
找到最佳服务器

作为client:
加入房间(指定服务器，房间)，通过房间号

共同能力:加密/解密mc流量

## 命令:

### host

`--max-players` `-N` \<N\>
设定最大玩家数(包括自己，所以要>=2)

`--discover-mode` <latency|distance|manual>（默认：latency）
从 center 获取节点列表后如何选择：
- latency：自动测试延迟后选延迟最低
- distance：按地理/机房距离选择
- manual：完全使用 --server-addr 指定的节点

`--server-addr` \<HOST:PORT\>
直接指定 server 节点。
- 当 --discover-mode=manual 时必填；
- 其他模式下若填写则优先使用它，不可用再退回自动发现。

### client

`--room-id` \<STRING\>
房间ID

### 

`--room-pass` \<STRING\>
房间密码

`--game-port` \<PORT\>
设定游戏的联机端口

`--center-addr` \<HOST:PORT\>
设定center的地址,默认为api.center.mcrelay.com
port不指定默认为48279

`--center-auth` <none|key|token>
指定是否使用密钥/令牌：
- none：默认公开连接
- key：本地密钥
- token：比如登录后发给你的 token

`--center-key` <PATH>
当 --center-auth=key 时使用的密钥文件路径

`--center-token` <STRING>
当 --center-auth=token 时使用的 token。


