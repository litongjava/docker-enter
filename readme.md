## docker-enter
docker-enter 是一系列基于docker的命令
## install
download
```
https://github.com/litongjava/docker-enter/releases/download/v1.0/docker-enter.zip
```

uzip
```
sudo unzip docker-enter.zip -d /bin
```
提示选择N
```
Archive:  docker-enter.zip
  inflating: /bin/docker-ip
 extracting: /bin/docker-logpath
 extracting: /bin/docker-rmexited
  inflating: /bin/docker-volume
  inflating: /bin/get_docker-enter
  inflating: /bin/importenv
replace /bin/nsenter? [y]es, [n]o, [A]ll, [N]one, [r]ename: N
  inflating: /bin/docker-enter
```
添加执行权限
```
sudo chmod u+x /bin/docker-enter
sudo chmod u+x /bin/docker-ip
sudo chmod u+x /bin/docker-logpath
sudo chmod u+x /bin/docker-rmexited
sudo chmod u+x /bin/docker-volume
sudo chmod u+x /bin/importenv
sudo chmod u+x /bin/nsenter
```

## use
使用docker-enter 进入容器
```
docker run --name nodejs16 --network=host -dit -v /data:/data node:16.16.0-slim
docker ps -a
docker-enter nodejs16
```
