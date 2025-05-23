## ArgoSB一键无交互脚本

### 1、脚本主打极简、轻便的体验

### 2、支持各种主流VPS系统、容器NIX系统

### 3、自动安装最新sing-box内核+最新Cloudflared-Argo内核，支持Argo临时/固定隧道

### 4、目前仅输出VMESS协议节点：13个端口节点及对应的优选不死IP全覆盖

----------------------------------------------------------

主流VPS脚本如下，默认安装为Argo临时隧道（uuid、vmess端口未设变量时，为随机生成）
```
bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)
```
----------------------------------------------------------

容器NIX脚本如下，默认安装为Argo临时隧道（uuid、vmess端口未设变量时，为随机生成）
```
nix=y bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)
```

----------------------------------------------------------

### 可自定义变量参数：

#### 1、Argo临时隧道：
#### 脚本前必须要有端口(vmpt)、uuid密码(uuid)，每次重装后临时域名都不相同，需重新复制节点信息

主流VPS脚本：
```
uuid=你的uuid vmpt=可使用的端口 bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)
```

容器NIX脚本：
```
nix=y uuid=你的uuid vmpt=可使用的端口 bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)
```

#### 2、Argo固定隧道：
#### 脚本前必须要有端口(vmpt)、uuid密码(uuid)、固定域名(agn)、token(agk)，每次重装后固定域名不变，一键复活原Argo固定隧道分享

主流VPS脚本：
```
uuid=你的uuid vmpt=可使用的端口 agn=固定域名 agk=ey开头的token bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)
```

容器NIX脚本：
```
nix=y uuid=你的uuid vmpt=可使用的端口 agn=固定域名 agk=ey开头的token bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)
```


#### 注：如果服务器支持任意端口，临时隧道端口变量(vmpt)可以不用设置

---------------------------------------------------------

### 相关快捷方式：

1、查看Argo的固定域名、固定隧道的token、临时域名、当前节点信息：

主流VPS脚本：```agsb``` 或者 ```bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)```

容器NIX脚本：```nix=y bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh)```

2、升级ArgoSB脚本：

主流VPS脚本：```agsb up``` 或者 ```bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh) up```

3、卸载ArgoSB脚本：

主流VPS脚本：```agsb del``` 或者 ```bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh) del```

容器NIX脚本：```nix=y bash <(curl -Ls https://raw.githubusercontent.com/aa336818/argosb/main/a.sh) del```

----------------------------------------------------------



----------------------------------------------------------
